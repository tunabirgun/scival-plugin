---
description: Rigorously evaluate the scientific validity of claims against high-impact literature.
disable-model-invocation: true
---

# The Scientific Validation Protocol
When the user invokes this skill, you must immediately suspend standard conversational replies and execute the following steps on the provided text:

1. **Map to the Hierarchy of Evidence:** Identify the highest level of evidence available for the claim (Meta-Analyses > RCTs > Cohorts > Animal/In-Vitro).
2. **Evaluate Statistical Rigor:** Assess sample sizes, p-values, and effect sizes. 
3. **Assess Bias:** Scan for replication crisis markers or funding bias.
4. **Establish Certainty:** Use a GRADE-inspired approach to determine the certainty of evidence.

## Output Generation Format
Generate the following structured report:

### SciVal Executive Summary
* **Target Claim:** [Directly quote the core claim]
* **Verdict:** [Unassailable / Strongly Supported / Mixed Evidence / Weakly Supported / Contradicted / Pseudoscientific]
* **Primary Evidence Base:** [e.g., "Multiple Meta-Analyses"]

### Scientific Rigor & Validity Matrix
Rate each metric on a scale of 1–10 based strictly on published literature.

| Evaluation Metric | Score | Justification & Evidence Threshold |
| :--- | :--- | :--- |
| **Evidence Tier (Hierarchy)** | X / 10 | 10 = Meta-analyses. 1 = Anecdotal. |
| **Statistical & Methodological Power**| X / 10 | Assessment of sample sizes, controls, and blinding. |
| **Replication Status** | X / 10 | Successfully replicated by independent labs? |
| **Contemporary Consensus** | X / 10 | Agreement in high-impact journals over the last 3–5 years. |
| **Absence of Bias/Confounders** | X / 10 | Likelihood that results are free from bias. |
| **OVERALL SCIVAL INDEX** | **X / 10** | **Weighted average.** |

### Deep Literature Analysis
Provide three short sections:
1. **High-Impact Consensus & Recent Meta-Analyses:** Detail the strongest evidence.
2. **Methodological Vulnerabilities & Counter-Evidence:** Identify the weakest links or refutations.
3. **Boundary Conditions:** Explain where/when the claim fails.

### Calibration Recommendation
* **Original Statement:** "[User's statement]"
* **Scientifically Calibrated Statement:** "[Rewrite empirically bulletproof.]"
