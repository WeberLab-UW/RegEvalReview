# Empirical evaluations of U.S. state and local technology policies, 2015–2024

**The empirical evidence base for evaluating subnational technology policies is uneven—robust in some domains (short-term rental regulation, gig economy worker classification, algorithmic risk assessment) and thin in others (surveillance oversight ordinances, facial recognition bans, children's online safety laws).** This literature review identified over 130 empirical studies across 11 policy areas, revealing a recurring pattern: legislatures often enact technology policies faster than researchers can evaluate them, and many landmark laws—San Francisco's facial recognition ban, Utah's social media restrictions, California's Age-Appropriate Design Code—have **zero** published empirical evaluations of their outcomes. Where rigorous evidence does exist, it frequently challenges policy assumptions: STR regulations reduce listings but often fail to lower rents; gig worker minimum pay laws raise base pay but trigger offsetting reductions in tips and task availability; and predictive policing tools trained on biased data perpetuate the biases they inherit.

---

## 1. License plate readers show limited crime prevention effects despite rapid proliferation

The ALPR evidence base consists primarily of quasi-experimental and randomized studies evaluating crime reduction, with almost no empirical work on data retention limits or disparate racial impact.

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["The Impacts of Large-Scale License Plate Reader Deployment on Criminal Investigations"](https://doi.org/10.1177/1098611119828039) | Koper & Lum | 2019 | *Police Quarterly* | Fixed LPR network (~100 units), unnamed U.S. city | Survival analysis of case closures pre/post LPR | Case clearances for auto theft improved but were **not statistically significant** in multivariate analyses. |
| ["A Randomized Test of Initial and Residual Deterrence from Directed Patrols and Use of License Plate Readers at Crime Hot Spots"](https://doi.org/10.1007/s11292-013-9190-2) | Koper, Taylor & Park | 2013 | *Journal of Experimental Criminology* | LPR patrol deployment, Fairfax County, VA | Quasi-randomized trial; 785 patrols at 33 hot spots | LPR increased stolen vehicle recoveries but not arrests; "little clear evidence for the crime prevention efficacy of using LPRs in general patrol." |
| ["Combating Auto Theft in Arizona: A Randomized Experiment with License Plate Recognition Technology"](https://www.policeforum.org/assets/docs/Free_Online_Documents/Technology/combating%20auto%20theft%20in%20arizona%202012.pdf) | Taylor, Koper & Woods | 2012 | PERF Report | LPR hot routes deployment, Mesa, AZ | Randomized controlled experiment (first ALPR RCT) | LPR patrols did not produce statistically significant reductions in auto theft compared to control routes. |
| ["License Plate Recognition Technology (LPR): Impact Evaluation and Community Assessment"](https://www.ojp.gov/ncjrs/virtual-library/abstracts/license-plate-recognition-technology-lpr-impact-evaluation-and) | Lum, Merola, Willis & Cave | 2010 | George Mason University / NIJ Report | LPR deployment, Alexandria & Fairfax County, VA | RCT + national survey | Adoption occurring in a "low-information environment"; limited crime reduction effects but improved stolen vehicle recovery. |
| ["An Evaluation of a Major Expansion in Automated License Plate Reader (ALPR) Technology"](https://doi.org/10.1177/08874034241309498) | Shjarback & Sarkos | 2025 | *Criminal Justice Policy Review* | 120 stationary ALPRs, Atlantic City, NJ (NJ AG Directive 2022-12) | ARIMA time series analysis | Mixed results; some crime reductions but not consistently significant; extensive implementation challenges. |
| ["Flock Safety Technologies in Law Enforcement: An Initial Evaluation"](https://www.researchgate.net/publication/377845222) | Nhan et al. | 2024 | White paper / ResearchGate | Flock Safety ALPR, 123 U.S. agencies | Cross-sectional survey; multilinear regression vs. FBI UCR data | One additional Flock camera per officer associated with **9.1% increase in clearance rate**. NOTICE: Industry-funded, not peer-reviewed, cross-sectional design. |
| ["Research in Brief: Assessing the Effectiveness of Automatic License Plate Readers"](https://www.policechiefmagazine.org/assessing-the-effectiveness-of-automatic-license-plate-readers/) | Potts / BetaGov | 2018 | *Police Chief Magazine* | Vallejo, CA PD ALPR deployment | RCT | ALPR identifies stolen cars effectively, but **37% of fixed ALPR hits were misreads**. |
| ["What You Can Learn from Oakland's Raw ALPR Data"](https://www.eff.org/deeplinks/2015/01/what-we-learned-oakland-raw-alpr-data) | Maass (EFF) | 2015 | EFF Report | Oakland PD ALPR deployment patterns | Geospatial analysis of 4.6 million ALPR scans vs. demographic data | ALPRs disproportionately concentrated in Black and Latino neighborhoods despite automobile crimes occurring elsewhere. |
| ["Law Enforcement Use of Automatic License Plate Recognition"](https://vscc.virginia.gov/Annual%20Reports/2024%20VSCC%20Annual%20Report%20-Law%20Enforcement%20Use%20of%20ALPR.pdf) | Virginia State Crime Commission | 2024 | State government report | 18 state ALPR regulatory frameworks | Comparative policy analysis + law enforcement survey | State retention periods range from minutes to years; limited effectiveness research exists; wide variation in internal policies. |

**Critical gap:** No published empirical study evaluates whether specific state data retention limits (New Hampshire's 3-minute, Maine's 21-day, Vermont's 18-month) affected crime clearance rates or privacy outcomes. No peer-reviewed assessment of California SB 34 exists. The National Policing Institute's multi-site evaluation across 93 agencies in 27 states is ongoing but unpublished.

---

## 2. Facial recognition accuracy disparities are well-documented, but ban evaluations are almost nonexistent

The facial recognition literature divides sharply: a robust body of work documents demographic accuracy disparities, while **virtually no empirical studies evaluate the effects of municipal bans**.

### Accuracy and bias studies

| Paper | Authors | Year | Venue | Method | Key finding |
|---|---|---|---|---|---|
| ["Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification"](https://proceedings.mlr.press/v81/buolamwini18a.html) | Buolamwini & Gebru | 2018 | FAT* 2018 (PMLR Vol. 81) | Benchmark audit of 3 commercial systems using 1,270 images | Darker-skinned females misclassified at rates up to **34.7%** vs. 0.8% for lighter-skinned males. |
| ["Actionable Auditing: Investigating the Impact of Publicly Naming Biased Performance Results"](https://doi.org/10.1145/3287560.3287596) | Raji & Buolamwini | 2019/2023 | AIES 2019; *Communications of the ACM* Vol. 66 | Follow-up audit using PPB benchmark | All three target companies reduced disparities within 7 months; non-target companies (Amazon: 31.4% error for darker females) showed persistent bias. |
| ["Face Recognition Vendor Test Part 3: Demographic Effects" (NISTIR 8280)](https://doi.org/10.6028/NIST.IR.8280) | Grother, Ngan & Hanaoka | 2019 | NIST Interagency Report | Evaluation of 189 algorithms on 18.27M images | False positive rates elevated for West/East African and East Asian individuals; **most accurate algorithms showed "undetectable" differentials**. |
| ["FRVT Part 8: Summarizing Demographic Differentials" (NISTIR 8429)](https://doi.org/10.6028/NIST.IR.8429) | Grother, Ngan & Hanaoka | 2022 | NIST Interagency Report | Summary inequity measures applied to hundreds of algorithms | False negative inequities largely due to poor photography of dark-skinned individuals; false positive variations require algorithmic mitigation. |
| ["Facial Recognition Systems in Policing and Racial Disparities in Arrests"](https://doi.org/10.1016/j.giq.2022.101753) | Johnson, Johnson, McCurdy & Olajide | 2022 | *Government Information Quarterly* 39(4) | Doubly robust propensity score models, 1,136 U.S. cities | FRT deployment associated with **greater racial disparity in arrests**—higher Black arrest rates, lower white arrest rates. |
| ["Police Facial Recognition Applications and Violent Crime Control in U.S. Cities"](https://doi.org/10.1016/j.cities.2024.105427) | Johnson, Johnson, Topalli, McCurdy & Wallace | 2024 | *Cities* 155 | Generalized DiD with multiway fixed effects, 268 cities (1997–2020) | FRT associated with reduced felony violence and homicide **without** contributing to racial disparities in violent arrests. First peer-reviewed crime-control evaluation. |

### Ban and regulation evaluations

| Paper | Authors | Year | Venue | Policy studied | Key finding |
|---|---|---|---|---|---|
| ["Facing Facts: The Effect of Facial Recognition Bans on Policing Effectiveness"](https://repository.digital.georgetown.edu/handle/10822/1088629) | (Georgetown thesis) | ~2024 | Georgetown University Digital Repository | Massachusetts municipal FRT bans | No evidence bans affected violent crime clearance rates. |
| San Francisco ban compliance (investigative) | Washington Post | 2024 | Investigative journalism | San Francisco Ordinance 107-19 (2019 ban) | Police circumvented ban at least 6 times by asking officers in other jurisdictions to run searches. |
| ["The Perpetual Line-Up: Unregulated Police Face Recognition in America"](https://www.perpetuallineup.org) | Garvie, Bedoya & Frankle | 2016 | Georgetown Law Center on Privacy & Technology | National FRT landscape | 117+ million adults in law enforcement face recognition networks; use almost completely unregulated. |

**No peer-reviewed empirical evaluations exist** for the San Francisco, Oakland, Boston, Portland, or Minneapolis facial recognition bans, nor for Virginia HB 2031. A 2026 scoping review in *Policing: An International Journal* found only 11 total empirical studies on law enforcement FRT published between 2020 and 2024. The Johnson et al. studies present an **unresolved tension**: the 2022 study finds FRT worsens racial arrest disparities while the 2024 study finds it reduces violent crime without racial bias in violent arrests.

---

## 3. Surveillance oversight ordinances lack quantitative outcome studies

Research on CCOPS-type ordinances is almost entirely qualitative.

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Municipal Surveillance Regulation and Algorithmic Accountability"](https://doi.org/10.1177/2053951719843831) | Young, Katell & Krafft | 2019 | *Big Data & Society* | Seattle Ordinance 125376 + 5 cities | Qualitative case study: 28 technologies analyzed, stakeholder interviews | Government employees often did not identify algorithmic surveillance as machine learning-reliant; definitional gaps undermine ordinance. |
| ["Local Surveillance Oversight Ordinances"](https://www.law.berkeley.edu/wp-content/uploads/2021/02/Local-Surveillance-Ordinances-White-Paper.pdf) | Chivukula & Takemoto | 2021 | Berkeley Law White Paper | 16 surveillance oversight ordinances | Systematic comparative analysis | All but NYC require elected body approval; Oakland uniquely tracks racial demographics; NYC POST Act structurally weak. |
| ["Surveying Surveillance: A National Study of Police Department Surveillance Technologies"](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3911442) | Oliver & Kugler | 2022 | *Arizona State Law Journal* 54(1) | National police surveillance technology landscape | Original nationwide CivicPulse survey | Surveillance technology access varies widely by jurisdiction size; even small departments have high body camera adoption. |

**Critical gap:** No quantitative study measures whether CCOPS ordinances actually reduced surveillance acquisition, improved privacy outcomes, or reduced disparate impact. Seattle's ordinance—enacted in 2017—has no quantitative outcome evaluation beyond administrative reports.

---

## 4. Consumer privacy law evaluations reveal compliance gaps and modest behavioral shifts

The CCPA/BIPA literature is the most developed privacy evaluation landscape, though most studies examine compliance rather than consumer outcomes.

### CCPA effectiveness and compliance

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Setting the Bar Low: Are Websites Complying with the Minimum Requirements of the CCPA?"](https://doi.org/10.56553/popets-2022-0092) | Van Nortwick & Wilson | 2022 | *PoPETS 2022* | CCPA | Longitudinal web crawl of top 1M websites | Many sites lack required "Do Not Sell" links; some geofence to hide links from non-Californians. |
| ["Gaining or Losing Control? An Empirical Study on the Real Use of Data Control Rights"](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4793249) | Corren | 2024 | SSRN Working Paper 4793249 | CCPA | Analysis of firm-reported CCPA usage metrics | Only a tiny fraction of consumers exercise data rights; large gaps between theoretical and actual rights usage. |
| [Consumer Reports CCPA study](https://advocacy.consumerreports.org/wp-content/uploads/2020/09/CR_CCPA-Are-Consumers-Digital-Rights-Protected_092020_vf.pdf) | Consumer Reports Digital Lab | 2020 | Consumer Reports | CCPA opt-out processes | User testing across multiple companies | 14% of the time, burdensome or broken processes prevented rights exercise; 46% of consumers unsure if requests were honored. |
| [CFA/Consumer Action survey](https://consumerfed.org/press_release/survey-shows-californians-are-still-unaware-of-privacy-rights/) | Consumer Action & CFA | 2021 | Survey report | CCPA consumer awareness | Survey of 1,507 California adults | **42% of non-users unaware they could opt out**; 40%+ unaware of access/deletion rights. |

### Economic impacts

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["The Cost of Data Privacy Law: Evidence from the California Mortgage Market"](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4404636) | Gupta, McGowan & Ongena | 2023 | SSRN 4404636 | CCPA | Econometric analysis of mortgage data | CCPA raises bank costs **$288 per $1M assets** but reduces data breach probability by 8%; mortgage lifetime costs increase $4,661. |
| ["Consumer Privacy and Value of Consumer Data"](https://doi.org/10.2139/ssrn.4162567) | Canayaz, Kantorovitch & Mihet | 2022 | Swiss Finance Institute Paper 22-68 | CCPA | DiD with 11,436 conversational-AI firms | CCPA advantaged firms with in-house data (higher valuations, profitability); firms dependent on purchased data suffered. |
| ["Data, Privacy Laws and Firm Production: Evidence from the GDPR"](https://www.nber.org/papers/w32146) | Demirer, Jiménez Hernández, Li & Peng | 2024 | NBER Working Paper 32146 | GDPR (CCPA comparison baseline) | DiD using Microsoft Azure cloud computing data | EU firms decreased data storage by **26%** and processing by 15% post-GDPR; represents 22% cost-of-data increase. |
| [CCPA Standardized Regulatory Impact Assessment](https://cppa.ca.gov/regulations/pdf/std_399_attachment.pdf) | Berkeley Economic Advising and Research | 2019 | CA Dept. of Finance | CCPA compliance costs | Economic impact modeling | Companies face up to **$55 billion in initial compliance costs** (~1.8% of California GSP). |

### Illinois BIPA

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["The Who, Why, and Where of Biometric Privacy Litigation: An Empirical Analysis of BIPA Cases 2015-2024"](https://www.analysisgroup.com/Insights/publishing/the-who-why-and-where-of-biometric-privacy-litigation-an-empirical-analysis-of-bipa-cases-2015-2024/) | Analysis Group | 2024 | *The Antitrust Source* | Illinois BIPA | Empirical litigation analysis | Identifies patterns in who files, why, and where; 2024 amendments limiting per-scan liability may reshape future litigation. |

Notable BIPA deterrent effects documented observationally: Clearview AI withdrew from Illinois; Google excluded Nest facial recognition features for Illinois consumers; Facebook paid a **$650 million** settlement, TikTok $92 million, Google $100 million.

### Data broker registration

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Registered Data Brokers in the United States: 2021"](https://privacyrights.org/resources-tools/reports/registered-data-brokers-united-states-2021) | Privacy Rights Clearinghouse | 2021 | PRC Report | CA & VT data broker registration laws | Cross-registry analysis of 540 businesses | 25% of brokers registered in only one state despite operating in both. |
| ["Why Are Hundreds of Data Brokers Not Registering with States?"](https://www.eff.org/deeplinks/2025/06/why-are-hundreds-data-brokers-not-registering-states) | EFF & PRC | 2025 | Joint analysis | CA, TX, OR, VT registration laws | Cross-state registry comparison | 291 brokers missing from California, 524 from Texas—significant gaps undermine deletion mechanisms. |

---

## 5. Gig economy studies reveal sub-minimum wages and complex policy tradeoffs

This is one of the richest empirical literatures, spanning NBER working papers to government-commissioned analyses.

### California AB5

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Assessing the Impact of Worker Reclassification: Employment Outcomes Post–California AB5"](https://doi.org/10.2139/ssrn.4709497) | Palagashvili, Suarez, Kaiser & Melo | 2024 | Mercatus/SSRN 4709497 | California AB5 | DiD using CPS data (2011–2023) | Self-employment fell **10.5%**, overall employment fell 4.4% for nonexempt occupations. No evidence W-2 employment increased. |
| ["ABC Tests and the Shrinking of Work"](https://www.mercatus.org/research/working-papers/abc-tests-and-shrinking-work) | Palagashvili & Bjoerkheim | 2025 | Mercatus Working Paper | ABC test adoption nationally | Causal DiD across states | States adopting ABC tests saw W-2 employment fall 4.7%, self-employment drop 6.4%. |

### Proposition 22 and driver pay

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Gig Passenger and Delivery Driver Pay in Five Metro Areas"](https://laborcenter.berkeley.edu/gig-passenger-and-delivery-driver-pay/) | Jacobs, Reich, Challenor & Farman | 2024 | UC Berkeley Labor Center | Prop 22 + comparison cities | Gridwise trip data, 1,000+ drivers | CA passenger drivers earned **$7.63/hr with tips** (employee-equivalent); less than Boston, Chicago, Seattle counterparts. |
| ["Prop 22 Depresses Wages and Deepens Inequities"](https://nationalequityatlas.org/prop22-paystudy) | National Equity Atlas / USC ERI | 2022 | USC Equity Research Institute | Prop 22 | Participatory research, 55 drivers | Prop 22 pay standards rarely binding; deepened racial pay inequities. |
| ["On Algorithmic Wage Discrimination"](https://columbialawreview.org/content/on-algorithmic-wage-discrimination/) | Dubal | 2023 | *Columbia Law Review* 123 | Prop 22 / gig classification | Ethnographic research, hundreds of driver interviews | Companies use data to set personalized, variable wages ("algorithmic wage discrimination"); workers describe it as gambling. |

### Seattle and NYC minimum pay ordinances

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| [**"Delivering Higher Pay? The Impacts of a Task-Level Pay Standard in the Gig Economy"**](https://www.nber.org/papers/w34545) | An, Garin & Kovak | 2025 | **NBER Working Paper 34545** | Seattle App-Based Worker Minimum Payment (SMC 8.37), effective Jan 2024 | Quasi-experimental with worker fixed effects, Gridwise trip-level data | Base pay rose but **tips fell substantially and tasks declined**, yielding **zero net effect on monthly earnings**. Most rigorous causal study in the field. |
| ["New York City's Gig Driver Pay Standard: Effects on Drivers, Passengers, and the Companies"](https://escholarship.org/uc/item/3xb4152j) | Koustas, Parrott & Reich | 2020 | New School / UC Berkeley | NYC minimum driver pay (effective Feb 2019) | Analysis of 500 million trips | Driver pay increased ~9%; fares rose slightly; wait times declined. |
| NYC DCWP Q1 2024 Compliance Data | NYC DCWP | 2024 | Government monitoring report | NYC delivery worker minimum pay (effective Dec 2023) | Mandatory quarterly app reporting | Earnings rose **64% to $19.26/hr**; tips fell 60%; total deliveries increased 8%; worker count fell ~8–9%. |

---

## 6. Short-term rental regulations reduce listings but often fail to lower rents

This domain has the strongest causal evidence, with multiple DiD and RDD studies in top economics journals.

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["The Effect of Home-Sharing on House Prices and Rents: Evidence from Airbnb"](https://doi.org/10.1287/mksc.2020.1227) | Barron, Kung & Proserpio | 2021 | *Marketing Science* 40(1) | Airbnb expansion, all U.S. zip codes | IV (shift-share), panel data | 1% increase in Airbnb listings → **0.018% rent increase, 0.026% price increase**; Airbnb accounts for ~1/5 of rent growth. |
| ["Short-Term Rentals and the Housing Market"](https://doi.org/10.1016/j.jue.2021.103356) | Koster, van Ommeren & Volkhausen | 2021 | *Journal of Urban Economics* 124 | Home Sharing Ordinances, 18 LA County cities | Panel RDD at city borders + DiD | HSOs reduced listings by **50%**, house prices by 2%, rents by 2%. |
| ["How Do Short-Term Rental Regulations Affect Market Outcomes?"](https://doi.org/10.1111/1540-6229.12537) | Bibler, Teltser & Tremblay | 2025 | *Real Estate Economics* | San Francisco 2017 registration requirement | DiD vs. surrounding cities | Availability fell **20–27%**; housing prices fell 10–14% in highest-density Airbnb areas. |
| ["Short-Term Rentals and Residential Rents: Evidence from a Regulation in Santa Monica"](https://doi.org/10.1108/IJHMA-01-2024-0001) | Chaves Fonseca | 2024 | *Intl. J. of Housing Markets and Analysis* | Santa Monica 2015 HSO | Synthetic control method | 60% reduction in listings but **no statistically significant effect on rents**—units were not returned to long-term market. |
| ["The Effects of Short-Term Rental Regulation: Insights from Chicago"](https://www.nber.org/papers/w32537) | Jin, Wagman & Zhong | 2024 | *Intl. J. of Industrial Organization* / NBER WP 32537 | Chicago 2016 ordinance | DiD vs. 3 control cities | Listings fell 16.4%; burglaries fell **12.4%** near restricted buildings; data-driven enforcement proved critical. |
| ["Do Short-Term Rental Platforms Affect Housing Markets? Evidence from Airbnb in Barcelona"](https://doi.org/10.1016/j.jue.2020.103278) | Garcia-López, Jofre-Monseny, Martínez-Mazza & Segú | 2020 | *Journal of Urban Economics* 119 | Barcelona license moratorium (2014) | Panel fixed-effects, IV shift-share | Top-decile Airbnb neighborhoods: rents +7%, transaction prices **+19%**. |
| ["The Welfare Effects of Peer Entry: The Case of Airbnb"](https://doi.org/10.1257/aer.20180260) | Farronato & Fradkin | 2022 | *American Economic Review* 112(6) | Airbnb competition with hotels, 50 largest U.S. cities | Structural demand/supply model | Airbnb generated **$41 consumer surplus per room-night**; reduced hotel profits up to 3.7%; total welfare gain $137M in 2014. |
| ["The Battle for Homes: How Does Home Sharing Disrupt Local Residential Markets?"](https://doi.org/10.1287/mnsc.2022.4299) | Chen, Wei & Xie | 2022 | *Management Science* 68(12) | Airbnb "One Host, One Home" policy (NYC, SF, Portland) | DiD + synthetic control | Platform self-regulation reduced rents and home values by ~3%. |
| NYC Local Law 18 case study | (Springer, 2025) | 2025 | Springer book chapter | NYC Local Law 18 (2022), implemented Sept 2023 | Case study with listing/rental data | Massive listing drop but **long-term housing supply did not correspondingly increase and rents grew faster than comparable cities**. |

**Cross-cutting insight:** Enforcement mechanisms—especially platform data-sharing agreements—determine regulatory effectiveness far more than the rules themselves. Chicago, Barcelona, and San Francisco all saw meaningful listing reductions only after platforms shared data or active monitoring began. Several studies (Santa Monica, San Francisco/Kytömaa, NYC LL18) found that even dramatic reductions in STR listings did not automatically reduce rents because units were not reintroduced to the long-term market.

---

## 7. Autonomous vehicle safety data is accumulating but independent verification remains limited

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Comparison of Waymo Rider-Only Crash Data to Human Benchmarks at 7.1 Million Miles"](https://doi.org/10.1080/15389588.2024.2380786) | Kusano et al. | 2024 | *Traffic Injury Prevention* | Waymo ADS under NHTSA SGO reporting (Phoenix, SF, LA) | Retrospective safety impact analysis | Any-injury crashes: **0.6 vs. 2.80 per million miles** (80% reduction); police-reported: 57% reduction. ⚠️ Waymo-authored. |
| ["Comparative Safety Performance"](https://doi.org/10.1016/j.heliyon.2024.e34379) | Di Lillo et al. | 2024 | *Heliyon* 10(14) | Waymo One (SF, Phoenix) vs. Swiss Re insurance data | Insurance claims comparison over 3.8M miles | 76% reduction in property damage claims; **zero bodily injury claims**. ⚠️ Waymo-authored. |
| ["A Root Cause Analysis of a Self-Driving Car Dragging a Pedestrian"](https://doi.org/10.1109/MC.2024.3429276) | Cummings, Wheeler & Kliem | 2024 | *IEEE Computer* 57(11) | Cruise Oct. 2, 2023 incident; CA DMV/CPUC regulatory response | Root cause analysis using TAIHA taxonomy | Major failures: lacking remote operations consideration, post-collision assessment deficiencies, absence of periodic design reviews. |
| ["Anatomy of a Robotaxi Crash"](https://doi.org/10.1007/978-3-031-68606-1_8) | Koopman | 2024 | SafeComp 2024 / *IEEE Reliability Magazine* | Cruise incident; California AV regulatory system | Technical case study | AV's collision detection **incorrectly classified** the pedestrian collision, triggering pullover instead of emergency stop. Identifies systemic safety culture issues. |
| ["Driving to Safety"](https://www.rand.org/pubs/research_reports/RR1478.html) | Kalra & Paddock | 2016 | RAND Research Report RR-1478 | Statistical framework for AV safety evaluation | Crash rate statistical analysis | AVs would need **hundreds of millions to billions of miles** to demonstrate fatality safety improvements with statistical confidence. |

**Key observation:** All published Waymo safety comparisons are authored by Waymo employees. Independent verification of raw data is limited. The Cruise incident studies by Cummings et al. and Koopman reveal how regulatory structures failed to prevent or detect fundamental safety design flaws, with a Harvard Kennedy School paper concluding that California's state preemption of local authority left San Francisco unable to limit AV operations.

---

## 8. Municipal broadband delivers measurable economic benefits where preemption allows it

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Ten Years of Fiber Optic and Smart Grid Infrastructure in Hamilton County, TN"](https://assets.epb.com/media/Lobo%20-%20Ten%20Years%20of%20Fiber%20Infrastructure%20in%20Hamilton%20County%20TN_Published.pdf) | Lobo | 2020/2025 | University of Tennessee at Chattanooga | Chattanooga EPB fiber network (deployed 2010) | Economic impact modeling (IMPLAN), employment/investment tracking | **$5.3 billion** in community benefits over 15 years (4.42x ROI on $396M investment); 10,420 jobs; 417 million minutes of prevented power outages. |
| ["State Broadband Policy: Impacts on Availability"](https://doi.org/10.1016/j.telpol.2020.102025) | Whitacre & Gallardo | 2020 | *Telecommunications Policy* 44(9) | State municipal broadband preemption laws (2012–2018) | County-level panel, System GMM, 3,140 counties | Municipal/cooperative restrictions **decreased broadband availability by ~3 percentage points**; state funding programs increased it by 1–2 points. |
| ["Measuring Incumbent ISP Response to Municipal Broadband Opt-Out Referenda in Colorado"](https://www.sciencedirect.com/science/article/abs/pii/S0308596123001829) | (ScienceDirect) | 2023 | *Telecommunications Policy* | Colorado SB 05-152 opt-out referenda | DiD exploiting referendum timing | DSL providers offered speeds **11–26% lower** after referenda passed; potential public competition did not consistently improve service. |
| ["Evaluating the Impact of the Affordable Connectivity Program (ACP)"](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4913528) | Galperin, Bar & Chavez Penate | 2024 | USC Annenberg / SSRN | ACP (launched Jan 2022) | DiD comparing broadband adoption in well-served vs. underserved low-income counties | ACP had positive impact on adoption; impact limited where supply-side constraints existed. |
| ["Can Affordable Internet Increase Employment?" (ACP labor market study)](https://doi.org/10.1080/1369118X.2025.2591771) | Galperin, Bar & Chavez Penate | 2025 | *Information, Communication & Society* | ACP labor market impacts | DiD using ACS data (N≈29.8M) + augmented inverse propensity weighting (CPS, N=35,561) | ACP participation associated with improved labor outcomes, **particularly among women and fixed broadband users**. |
| ["Measuring Broadband Policy Success" (CAF evaluation)](https://doi.org/10.1145/3651890.3672272) | Manda et al. | 2024 | ACM SIGCOMM 2024 | FCC Connect America Fund | ISP service availability queries at CAF-funded addresses | Only **55% of CAF-funded addresses** actually served by subsidized ISPs; only 33% meet program compliance—a critical warning for BEAD implementation. |
| ["Achieving Universal Broadband in California"](https://www.ppic.org/publication/achieving-universal-broadband-in-california/) | PPIC (Hayden et al.) | 2023 | Public Policy Institute of California | California SB 156 ($6B investment, 2021) | Mixed methods: broadband data + 41 interviews across 54 counties | At least 2 million CA households (15%) still lack broadband; current maps overstate access; SB 156 still in implementation. |

---

## 9. Predictive policing tools perpetuate bias through feedback loops, while pretrial risk assessment shows more balanced results

### Predictive policing

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Randomized Controlled Field Trials of Predictive Policing"](https://doi.org/10.1080/01621459.2015.1077710) | Mohler, Short, Malinowski et al. | 2015 | *JASA* 110(512) | PredPol/ETAS model, LAPD | Single-blind RCT across 3 LAPD divisions | PredPol forecasts led to **7.4% crime reduction** per 1,000 minutes of patrol vs. analyst predictions. ⚠️ Authors are PredPol co-founders. |
| ["Does Predictive Policing Lead to Biased Arrests?"](https://doi.org/10.1080/2330443X.2018.1438940) | Brantingham, Valasik & Mohler | 2018 | *Statistics and Public Policy* 5(1) | PredPol, LAPD RCT | Hypothesis tests on arrest data from LAPD experiment | No significant racial differences in arrest proportions between treatment and control. ⚠️ Authors are PredPol co-founders. |
| ["To Predict and Serve?"](https://doi.org/10.1111/j.1740-9713.2016.00960.x) | Lum & Isaac | 2016 | *Significance* 13(5) | PredPol algorithm, Oakland drug arrest data | Simulation study comparing algorithm output to NSDUH drug use survey | PredPol would target Black people at **roughly twice the rate of whites** despite similar drug use rates; demonstrated runaway feedback loops. |
| ["Runaway Feedback Loops in Predictive Policing"](https://proceedings.mlr.press/v81/ensign18a.html) | Ensign, Friedler, Neville, Scheidegger & Venkatasubramanian | 2018 | FAT* 2018 (PMLR 81) | PredPol-type systems | Mathematical proof + empirical simulation | Formal proof that feedback loops cause algorithm to diverge from true crime rates as policing generates discovered incidents that feed back into predictions. |
| ["Review of Selected LAPD Data-Driven Policing Strategies"](https://www.lapdpolicecom.lacity.org/031219/BPC_19-0072.pdf) | LAPD Inspector General | 2019 | Government audit (BPC #19-0072) | PredPol and LASER programs, LAPD | Internal audit of operational data | After 8 years, data "so unreliable it was difficult to draw conclusions" about effectiveness; 44% of LASER chronic offenders had zero or one violent crime arrest. |

### Algorithmic risk assessment (COMPAS and PSA)

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Machine Bias" (ProPublica)](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing) | Angwin, Larson, Mattu & Kirchner | 2016 | ProPublica | COMPAS, Broward County, FL | Statistical analysis of 7,000+ defendant scores vs. 2-year outcomes | Black defendants **falsely labeled high-risk at 44.9%** vs. 23.5% for white defendants. |
| ["The Accuracy, Fairness, and Limits of Predicting Recidivism"](https://doi.org/10.1126/sciadv.aao5580) | Dressel & Farid | 2018 | *Science Advances* 4(1) | COMPAS | Crowdsourced human predictions vs. COMPAS; simple linear classifiers | Untrained Amazon Mechanical Turk workers matched COMPAS accuracy (**63–67%**); a 2-feature linear classifier matched the 137-feature model. |
| ["Fair Prediction with Disparate Impact"](https://doi.org/10.1089/big.2016.0047) | Chouldechova | 2017 | *Big Data* 5(2) | COMPAS and recidivism instruments generally | Mathematical proof with empirical application | **Impossibility theorem**: when base rates differ between groups, simultaneous calibration and equal error rates are mathematically impossible. |
| ["Evaluation of Pretrial Justice System Reforms: Effects of New Jersey's Criminal Justice Reform"](https://www.mdrc.org/work/publications/evaluation-pretrial-justice-system-reforms-use-public-safety-assessment-0) | Anderson, Redcross & Valentine (MDRC) | 2019 | MDRC Report | PSA + NJ Criminal Justice Reform (2017) | Interrupted time series + qualitative | Nearly eliminated financial bail; significantly reduced jail time post-arrest; **racial disparities persisted** in jail population. |
| ["Dollars and Sense in Cook County"](https://safetyandjusticechallenge.org/resources/dollars-and-sense-in-cook-county/) | Stemen & Olson (Loyola) | 2020 | Loyola University Study | PSA + General Order 18.8A, Cook County | Pre-post comparison (24,000+ defendants) | Pretrial release rose 77%→81%; no increase in new criminal activity (~17% both periods, ~3% violent); no increase in Chicago crime. |
| ["The Empirical Case for Pretrial Risk Assessment Instruments"](https://doi.org/10.1177/00938548221085570) | Desmarais, Monahan & Austin | 2022 | *Criminal Justice and Behavior* 49(6) | PSA and risk assessment generally | Systematic review/synthesis | Instruments demonstrate good accuracy even across racial groups; scientific evidence does not support claims tools worsen disparities. |

### NYC Local Law 144 (AI hiring)

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| [**"Null Compliance: NYC Local Law 144 and the Challenges of Algorithm Accountability"**](https://doi.org/10.1145/3630106.3658903) | Wright, Muenster, Vecchione, Qu, Cai, Smith & Matias | 2024 | **FAccT '24** | NYC Local Law 144 (AI hiring audits) | 155 investigators analyzed 391 employers | Only **18 of 391 employers** published audit reports; only 13 posted transparency notices. Law's discretionary provisions make non-compliance indistinguishable from compliance. |

**No empirical evaluations exist** for LAPD post-PredPol crime outcomes, Santa Cruz's predictive policing ban, the Illinois AI Video Interview Act, or Colorado SB 24-205 (not yet in effect).

---

## 10. Children's online safety laws are largely untested empirically, but school phone bans show results

Most prominent children's online safety laws—Utah's Social Media Regulation Act, Arkansas's SAFE Act, California's AADC—have been **enjoined by courts before implementation**, making empirical evaluation impossible.

### School cellphone bans

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| [**"The Impact of Cellphone Bans in Schools on Student Outcomes: Evidence from Florida"**](https://www.nber.org/papers/w34388) | Figlio & Özek | 2025 | **NBER Working Paper 34388** | Florida HB 379 (2023 statewide ban) | DiD using 130,000+ student records, Advan smartphone data | Suspensions rose in year 1 (especially Black students, +30%); test scores improved **1.1 percentile points** in year 2; phone use dropped ~two-thirds. |
| ["Ill Communication: Technology, Distraction & Student Performance"](https://doi.org/10.1016/j.labeco.2016.04.004) | Beland & Murphy | 2016 | *Labour Economics* 41 | School-level mobile phone bans, England | DiD using NPD data, 91 schools | Performance increased ~0.07 SD (~6.4%); effects driven entirely by **lowest-achieving students** (14.23% for bottom quintile). |

### Age verification for adult content

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Do Age-Verification Bills Change Search Behavior?"](https://www.researchsquare.com/article/rs-6190162/v1) | Lang, Listyg, Ross, Musquera & Sanderson | 2025 | Stanford / NYU Working Paper | Age verification laws in 18 states (Louisiana pioneer) | Pre-registered synthetic control, Google Trends | **51% reduction** in searches for compliant platforms (Pornhub); **48% increase** in searches for non-compliant platforms; 23.6% increase in VPN searches. |
| ["Unintended Consequences of Age Verification Laws"](https://phoenix-center.org/perspectives/Perspective25-06Final.pdf) | Ford | 2025 | Phoenix Center Perspective 25-06 | State age verification laws (all 50 states + DC) | Staggered DiD, weekly Google Trends panel | Florida saw **1,150% increase in VPN demand**; users shifted behavior rather than reducing consumption. |

### COPPA compliance

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["'Won't Somebody Think of the Children?' Examining COPPA Compliance at Scale"](https://doi.org/10.1515/popets-2018-0021) | Reyes, Wijesekera, Reardon et al. | 2018 | *PoPETS* Issue 3 | COPPA compliance in children's apps | Dynamic analysis of 5,855 apps | **Majority of apps potentially violated COPPA** through third-party SDKs collecting data without parental consent. |

---

## 11. Data center incentives generate economic activity but impose growing energy and community costs

| Paper | Authors | Year | Venue | Policy studied | Method | Key finding |
|---|---|---|---|---|---|---|
| ["Data Centers in Virginia"](https://jlarc.virginia.gov/landing-2024-data-centers-in-virginia.asp) | JLARC / Weldon Cooper Center | 2019/2024 | Virginia state government evaluation | Virginia data center sales/use tax exemption (2010) | IMPLAN modeling, 300+ interviews, confidential tax data | **90% of investment** would not have occurred without exemption; exemption cost $1.02B in FY24; industry supports 74,000 jobs, $9.1B GDP. Energy demand projected to **double within 10 years**. |
| [Georgia High-Tech Data Center Equipment Exemption evaluation](https://www.audits.ga.gov/ReportSearch/download/33298) | Carl Vinson Institute / GA Dept. of Audits | 2022/2024 | Georgia state audit | Georgia data center tax exemption | IMPLAN cost-benefit analysis | 2022: negative state fiscal impact of $18M. 2024 update: **$2.10 in tax receipts per $1 in exemption cost**. |
| ["Cloudy with a Loss of Spending Control"](https://goodjobsfirst.org/cloudy-with-a-loss-of-spending-control/) | LeRoy & Tarczynska (Good Jobs First) | 2025 | Good Jobs First | Data center incentives across 32+ states | Fiscal data analysis | 10+ states lose >$100M/year; Virginia's program went from $1.5M estimated impact to **$1.6 billion**; 12 of 32 states fail to disclose revenue losses. |
| ["2024 United States Data Center Energy Usage Report"](https://doi.org/10.2172/2431322) | Shehabi et al. (LBNL) | 2024 | DOE / LBNL | U.S. data center energy trends | Bottom-up modeling | Data centers consumed **176 TWh in 2023** (~4.4% of U.S. electricity); projected **325–580 TWh by 2028** (6.7–12%). |
| ["Data Centers and 2023 Home Sales in Northern Virginia"](https://cra.gmu.edu/wp-content/uploads/2025/08/NoVa_DataCenters.pdf) | Clower & Waters | 2024 | George Mason University | Data center proximity and home values (Fairfax, Loudoun, Prince William) | Hedonic regression, 2023 home sales | **No statistically significant negative impact** on housing values from data center proximity. |
| ["How Data Centers Have Come to Matter"](https://doi.org/10.1111/1468-2427.13316) | Monstadt et al. | 2025 | *Intl. J. of Urban and Regional Research* | Amsterdam data center moratorium (2019) | Qualitative case study, interviews | Moratorium increased visibility/politicization; post-moratorium rules limited construction to four parks, imposed PUE ≤1.2. |
| [Amsterdam/Dublin moratorium comparative](https://www.sciencedirect.com/science/article/abs/pii/S1462901124001035) | Multiple | 2024 | *Environmental Science & Policy* | Moratoria in Singapore, Amsterdam, Dublin, Frankfurt, Virginia, London | Comparative policy analysis, 6 case studies | Moratoria produce short-term results managing growth-environment tradeoffs; Germany's reform approach (stricter permits) offers alternative. |
| ["The Cloud Next Door"](https://doi.org/10.1145/3715335.3736324) | (ACM SIGCAS/SIGCHI) | 2025 | COMPASS 2025 | Community impacts, Northern Virginia "Data Center Alley" | Mixed methods: quantitative resource data + qualitative engagement | Nearly **half of ~700 U.S. data centers** are in census tracts with above-median environmental burdens; power dynamics determine who benefits and who bears costs. |
| [WRI community impact analysis](https://www.wri.org/insights/us-data-center-growth-impacts) | World Resources Institute | 2025 | WRI Insights | Virginia data center community impacts | Health cost modeling; review of 31 municipalities | Backup generators estimated to cause **~$300M in annual public health costs** and 14,000 asthma-related impacts in Virginia; 80% of municipalities had NDAs limiting public information. |

Ireland's data centers consumed **18% of national electricity** in 2022 (31% year-over-year increase), projected to reach 32% by 2026. Dublin's moratorium effectively blocked new grid connections until December 2025. Amsterdam's moratorium reduced capacity additions to just 62MW in 2023 versus 82MW in London.

---

## Conclusion: What this evidence landscape reveals

Four patterns cut across all 11 policy domains. First, **enforcement determines effectiveness** more than the rules on the page—this holds for STR regulations, facial recognition bans, COPPA, data broker registration, and AI hiring audits. Chicago's Airbnb regulation only worked after platform data-sharing began; San Francisco police circumvented the facial recognition ban by asking other jurisdictions to run searches; and only 18 of 391 NYC employers published required AI hiring audits.

Second, **behavioral displacement undermines policy intent** across domains. Age verification laws shift traffic to non-compliant platforms (48% increase in searches for unregulated sites). STR bans remove listings but units often don't return to the long-term rental market. Gig worker minimum pay laws raise base pay but employers offset gains through reduced tips and task availability.

Third, the **empirical evidence base is severely unbalanced**. Short-term rentals and gig economy policies have dozens of rigorous studies published in top journals. Surveillance oversight, facial recognition bans, and children's online safety laws have essentially zero outcome evaluations—a gap that grows more consequential as these policies proliferate to new jurisdictions.

Fourth, **conflict of interest pervades** certain literatures. Waymo employees author AV safety studies. PredPol founders published the LAPD RCT. Flock Safety consulted on the ALPR evaluation finding their cameras increase clearance rates. Industry-funded studies of gig worker pay (Cornell/Hyman et al.) diverge sharply from independent analyses. Readers must weight these studies accordingly, and the field would benefit from genuinely independent replication.