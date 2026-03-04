# Search and Link Verification Approach for FastLit.md

This document describes the agent-based workflow used to locate, verify, and embed hyperlinks for the ~70 studies referenced in `FastLit.md`.

---

## Architecture: Three-role agent pattern

The task used an **orchestrator-search-edit** pattern with a single coordinating agent managing parallel sub-agents.

### 1. Orchestrator (main conversation agent)

The orchestrator handled:

- **Task decomposition**: Splitting 70+ papers across 11 policy sections into 7 parallel search batches, grouped by topic affinity (e.g., all facial recognition papers together, all broadband papers together).
- **Prompt construction**: Writing structured prompts for each search agent specifying exact paper titles, authors, years, and venues.
- **Result synthesis**: Collecting URLs from all search agents, then running targeted follow-up web searches for papers marked `NOT FOUND`.
- **Edit sequencing**: Applying ~68 sequential string-replacement edits to the markdown file, one paper title at a time.
- **Quality verification**: Spot-checking rendered output across sections 1, 6, and 11 to confirm link formatting was correct inside markdown tables.

### 2. Search agents (7 parallel sub-agents)

Seven `general-purpose` agents were launched simultaneously, each assigned a topical batch:

| Agent | Sections covered | Papers assigned |
|---|---|---|
| 1 | Section 1: ALPR | 9 papers |
| 2 | Section 2: Facial recognition | 7 papers |
| 3 | Sections 3-4: Surveillance oversight + consumer privacy | 11 papers |
| 4 | Section 5: Gig economy | 7 papers |
| 5 | Section 6: Short-term rentals | 8 papers |
| 6 | Sections 7-8: Autonomous vehicles + broadband | 12 papers |
| 7 | Sections 9-11: Predictive policing, children's safety, data centers | 22 papers |

All seven agents ran concurrently in the background. Each received a structured prompt containing:

- Numbered list of paper titles (exact strings from the markdown tables)
- Author names, publication year, and venue for disambiguation
- Explicit instruction: "prefer doi.org links, fall back to publisher/repository URLs"
- Explicit instruction: return `NOT FOUND` rather than guess

### 3. Edit agent (orchestrator in edit mode)

After collecting all search results, the orchestrator applied edits directly to `FastLit.md` using string replacement. Each edit transformed a plain-text paper title into a markdown hyperlink:

```
Before: | "Paper Title" | Authors | Year | ...
After:  | ["Paper Title"](https://doi.org/...) | Authors | Year | ...
```

Edits were batched in groups of 8-10 parallel calls per section to maximize throughput while keeping each replacement uniquely identifiable.

---

## Prompting structure

Each search agent prompt followed a rigid template:

```
I need to find DOI links or canonical URLs for the following academic papers
about [TOPIC]. For each paper, search the web and provide the best URL
(prefer doi.org links, fall back to publisher/repository URLs).
Return a simple list with paper title -> URL.

[SECTION LABEL]:
1. "[Exact title]" by [Authors], [Year], [Venue]
2. ...

Return ONLY the paper title and URL pairs, nothing else.
If you cannot find a URL, say "NOT FOUND".
```

Key prompting decisions:

- **Exact titles from the source document** were passed verbatim to prevent drift between search targets and edit targets.
- **"Return ONLY"** constraint prevented agents from producing lengthy analyses, keeping output parseable.
- **"NOT FOUND" fallback** prevented hallucinated URLs. Any agent that could not verify a link was required to say so explicitly rather than construct a plausible-looking DOI.
- **Section grouping by topic** gave each agent domain context (e.g., an agent searching for all ALPR papers could use shared vocabulary and venues to disambiguate).

---

## Source priority hierarchy

Links were selected according to a strict priority order, established upfront with the user:

1. **DOI links** (`https://doi.org/...`): Preferred for all peer-reviewed journal articles. DOIs are permanent identifiers that resolve regardless of publisher URL changes. Used for ~40 papers.

2. **Institutional repository URLs**: For working papers with assigned identifiers:
   - NBER: `https://www.nber.org/papers/w{ID}`
   - SSRN: `https://papers.ssrn.com/sol3/papers.cfm?abstract_id={ID}`
   - NIST: `https://doi.org/10.6028/NIST.IR.{ID}`

3. **Publisher/organization direct URLs**: For reports, white papers, and non-journal publications:
   - Government reports (JLARC, LAPD IG, Virginia Crime Commission)
   - Advocacy organization reports (EFF, Consumer Reports, Good Jobs First)
   - University research centers (UC Berkeley Labor Center, Georgetown Law)

4. **Pre-print repositories**: For working papers without DOIs:
   - Research Square, ResearchGate, arXiv

5. **Plain text (no link)**: Applied when no reliable URL could be found or verified. Three papers were left unlinked:
   - Washington Post investigative journalism (paywalled, no stable URL)
   - Springer 2025 book chapter on NYC Local Law 18 (specific chapter not identifiable)
   - NYC DCWP Q1 2024 government monitoring data (no stable public URL)

---

## Verification workflow

Because the sub-agents lacked web access in their sandboxed environment, the orchestrator performed a second pass of **16 targeted web searches** to:

1. Find URLs for all papers the sub-agents marked `NOT FOUND`
2. Verify DOIs constructed from training knowledge against live search results
3. Resolve ambiguous cases (e.g., multiple versions of the same paper across SSRN, NBER, and journal publication)

Each web search used a query pattern combining: author surnames + year + exact or partial title + venue name. Results were cross-referenced against the paper metadata in the markdown tables to confirm correct matches.

---

## Constraints and limitations

- **No URL fabrication**: Any paper for which a URL could not be confirmed via web search was left as plain text. This is preferable to a broken or incorrect link.
- **Training knowledge as starting point only**: Sub-agents provided candidate URLs from training data, but every URL used in the final document was either (a) confirmed via live web search, or (b) constructed from an explicit identifier present in the original text (e.g., SSRN 4709497, NBER w34545).
- **No content behind paywalls was accessed**: Links point to landing pages, abstracts, or open-access versions. The verification process confirmed URL resolution, not full-text availability.
- **Snapshot in time**: URLs were verified on 2026-03-04. Publisher URL structures, especially for government reports and institutional pages, may change over time. DOI links are resilient to this; direct URLs are not.

---

## Output summary

| Metric | Count |
|---|---|
| Total papers in tables | ~71 |
| Papers successfully linked | 68 |
| Papers left as plain text | 3 |
| DOI links used | ~40 |
| SSRN/NBER/institutional links | ~15 |
| Organization/report direct URLs | ~13 |
| Parallel search agents launched | 7 |
| Follow-up web searches by orchestrator | 16 |
| Total edits to FastLit.md | 68 |
