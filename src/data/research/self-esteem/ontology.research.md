# Research: Technical studies about confidence — Ontology & Knowledge Base
# Source: Perplexity API (sonar-pro), queried 2026-03-10T17:39:12.929Z
# Topic Slug: self-esteem

---

## Query 1: Overview & Key Concepts

**Analytic Confidence Levels (High, Moderate, Low)**: In intelligence analysis, such as used by the Center for Internet Security (CIS) Cyber Threat Intelligence team, these levels assess the quality and quantity of source information supporting judgments. High Confidence indicates high-quality information from multiple trustworthy sources with minimal conflict; Moderate Confidence means credibly sourced but insufficient for higher levels, often with opposing views; Low Confidence reflects scant, questionable, or poorly corroborated data.[1]

**Words of Estimative Probability (WEPs)**: Standardized phrasing in intelligence products, per Intelligence Community Directives 203 and 206, to express uncertainty in forecasts and predictions, such as "likely" or "almost certainly," paired with analytic confidences by organizations like CIS.[1]

**Confidence Level**: In statistics, the probability (e.g., 95%) that a sample-based estimation of a population parameter, like the arithmetic mean, holds true for the entire population; common levels are 90%, 95%, or 99%, set before surveys to determine margin of error and sample size.[2][4]

**Confidence Interval (CI)**: A range of values, derived from sample data, likely to contain the true population parameter (e.g., mean) at a specified confidence level; in frequentist inference, \( P(u(X) < \theta < v(X)) = \gamma \) for all \( \theta \), where \( \gamma \) is the confidence coefficient.[5][7]

**Margin of Error**: The maximum expected difference between a sample statistic and the true population parameter, calculated within a confidence interval; for a 95% confidence level, it represents the ± range around the point estimate.[7][9]

**Frequentist Confidence Interval**: A 95% CI means that if the sampling procedure is repeated many times, 95% of intervals will contain the true parameter; it measures long-run frequency, not probability for a specific interval.[4][6]

**Bayesian Credible Interval**: Unlike frequentist CIs, a 95% credible interval indicates a 95% probability that the true parameter lies within it, given the data and prior beliefs.[6]

**Alpha (α)**: The significance level or risk of Type I error (false positive), where 1 - α equals the confidence level; common values are 0.01 (99% confidence), 0.05 (95%), or 0.10 (90%).[4]

**Key Assumptions Check (KAC)**: A structured analytic technique (SAT) that lists and challenges analysts' assumptions against evidence early in assessments, used by CIS to mitigate bias in cyber threat intelligence.[1]

**Quality of Information Check**: A diagnostic SAT for vetting evidence strength, evaluating source reliability, motivations, and risks; aligns with confidence assessments in cyber intelligence by CIS.[1]

**Analysis of Competing Hypotheses (ACH)**: A diagnostic SAT where hypotheses are scored and ranked against evidence, including absences, to eliminate unlikely explanations; applied by CIS in limited-information scenarios like ransomware incidents.[1]

**Team A/Team B**: A SAT involving structured debate between opposing analyst teams to resolve gridlock, evaluate perspectives, and identify new information needs; used in intelligence analysis.[1]

**High-Impact/Low-Probability (HILP) Analysis**: A SAT that identifies major environmental shifts and assumes they cause significant change, forcing consideration of rare but consequential scenarios.[1]

**Point Estimate**: A single value (e.g., sample mean) approximating the population parameter, serving as the center of a confidence interval.[7][8]

**Standard Error (SE)**: The standard deviation of the sampling distribution of a statistic, used in CI formulas like \( \bar{x} \pm z \cdot SE \), where z is the critical value for the confidence level.[5]

**Central Limit Theorem (CLT)**: States that sample means approximate a normal distribution for large samples (n ≥ 30), enabling CI construction regardless of population distribution.[2]

**Population Parameter**: The true unknown value (e.g., μ for mean) for the entire population, estimated by sample statistics within CIs.[5][7]

**Sample Statistic**: A calculated value from sample data (e.g., \( \bar{x} \) for mean), used to infer population parameters.[7]

**Z-Score (Critical Value)**: For normal distributions, values like 1.96 for 95% confidence or 2.576 for 99%, determining CI width.[4][8]

**T-Distribution**: Used for CIs with small samples (n < 30) or unknown population variance, with wider intervals than z due to added uncertainty.[5]

**P-Value**: Probability of observing data as extreme as the sample assuming the null hypothesis is true; related but distinct from confidence levels (e.g., α = 0.05).[4]

**Type I Error (α Risk)**: Incorrectly rejecting a true null hypothesis; directly tied to 1 - confidence level in hypothesis testing.[4]

**Structured Analytic Techniques (SATs)**: Diagnostic tools like KAC, ACH, and Team A/Team B to improve analytic rigor, reduce bias, and assess evidence in intelligence, per CIS practices.[1]

**Intelligence Community Directive 203 (ICD 203)**: U.S. policy mandating analytic standards, including WEPs and confidences, followed by CIS in cyber threat products.[1]

**Intelligence Community Directive 206 (ICD 206)**: U.S. sourcing requirements for analysis, underpinning confidence levels in intelligence assessments.[1]

**Center for Internet Security (CIS)**: Nonprofit organization whose Cyber Threat Intelligence team applies WEPs, confidences, and SATs for state, local, tribal, and territorial (SLTT) cybersecurity.[1]

**Cyber Threat Actor (CTA)**: Malicious entities (e.g., ransomware groups) whose claims are vetted via Quality of Information Checks in intelligence analysis.[1]

**High Confidence (Secureworks Definition)**: Judgments based on sound argumentation, consistent multi-source reporting, low gaps/assumptions, and low deception risk; used in threat intelligence.[3]

**95% Confidence**: Standard level where there's a 5% risk (α=0.05) the CI misses the true parameter if repeated; common in surveys and UX research.[2][4][9]

**Long-Run Frequency**: Interpretation of confidence as the proportion of correct CIs over infinite repeated sampling under identical conditions.[4][5]

---

## Query 2: Deep Details & Standards

**In technical studies on confidence—primarily in machine learning classification systems—main categories distinguish between system-level confidence (overall model reliability) and prediction-level confidence (uncertainty for individual outputs), with key taxonomies including tolerance regions, posterior probability-based paradigms, and logit distribution methods.[1][3][4]**

### Primary Categories of Confidence
Technical literature categorizes confidence in classification as follows:
- **System Confidence**: Measures overall classifier reliability, often modeled as a value function linking developer estimates (e.g., via training data) to user expectations; equates expected user confidence to developer confidence using posterior probabilities.[3][4][6]
- **Prediction Confidence**: Quantifies uncertainty for specific outputs, such as via logit distributions or cross-entropy loss; divides predictions into **exploit subsets** (high confidence, e.g., 90-99% levels) and **waste subsets** (low confidence).[1]
- **Indication Confidence**: Functions of posterior probability estimates, incorporating non-declaration options to balance accuracy and rejection rates.[3][7]

### Key Taxonomies and Classification Systems
Studies propose structured frameworks without a single universal taxonomy, but recurring systems include:
- **Tolerance Region Framework** (from Carnegie Mellon University research): Classifiers define two tolerance regions per class for **classification with confidence**; contrasts with **classification with rejection** (ambiguous regions via thresholds like η(x) ≤ 0.5 + k); robust implementations use subsampling (e.g., two-thirds fitting, one-third ranking) and tuning parameters like spar=1 (cross-validated) or spar=0.5.[2]
- **Confidence Paradigm** (developed by Air Force Institute of Technology, e.g., Delany et al., 2011): Models confidence as posterior probability-derived value; unifies developer/user views via expected value maximization; extends to **out-of-library** (unseen) problems with detection and non-declaration rates; tested on automatic target recognition datasets showing rational behavior (e.g., higher thresholds reduce errors to 10%).[3][4][5][6][7][9]
- **Logit-Based Methods** (arXiv 2022): 
  - **KRT** (Eq. 1): Kernel-related threshold from logit distributions.
  - **WDF** (Eq. 2): Weighted distribution function for confidence estimation.
  Evaluated on 20 models (e.g., RelEx on TACRED dataset with 12 NN-based relation extractors); thresholds data-independent (e.g., 0.99 for 10% errors in one model, 0.78 in another); enhanced accuracy (E.ACCU) and F-measure gains at 90%, 95%, 99% confidence levels.[1]

| Framework | Core Mechanism | Key Metrics/Examples | Sources |
|-----------|----------------|----------------------|---------|
| Tolerance Regions | Dual regions per class; robust subsampling | Coverage targets; spar tuning (median 1.006 over 100 simulations) | [2] |
| Confidence Paradigm | Posterior value function; non-declaration | 10% error thresholds; out-of-library expansion | [3][4][6][7] |
| Logit Distributions | KRT/WDF equations; exploit/waste split | 90-99% levels on 20 models; data-independent thresholds | [1] |

These systems emphasize filtering for reliability (e.g., predefined thresholds at training time using test data).[1] No comprehensive meta-taxonomy spans all studies; confidence often ties to Bayesian-inspired weight distributions (e.g., Blundell et al., 2015) but focuses on per-prediction quantification.[1] For broader psychological confidence taxonomies, search results lack coverage—technical ML dominates here.

---

## Query 3: Tools, People & Resources

[API ERROR: 429] {"error":{"message":"Request rate limit exceeded, please try again later.","type":"request_rate_limit_exceeded","code":429}}

---

## Extraction Notes

Use the above research to populate the ontology.astro page.
- Extract specific facts with dates/numbers for the content body
- Use named entities (companies, tools, people) for authoritative references
- Verify all URLs before including in the final page
- Cross-reference statistics across queries for consistency
