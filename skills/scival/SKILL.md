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
5. **Weight by Recency:** Recency is a validity criterion alongside impact. First decide whether the claim sits in an actively studied field (one where new high-impact work still appears) or a settled one. For an active field, prioritize the most recent high-impact evidence and treat older findings as superseded unless they remain the current consensus; flag any claim resting mainly on dated work as a vulnerability. For a settled field, a foundational source may stand, but say explicitly that it is foundational and still current.

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

### References
List every source cited above. Format each entry in **APA 7th edition** style and order the list alphabetically by first author surname.

* **Recency:** for any claim in an actively studied field, cite the most recent high-impact work available and prefer it over older sources; cite an older work only when it is foundational and still the current consensus, and note that status. Do not lean on dated references when newer high-impact literature exists.

* **Journal article:** Author, A. A., & Author, B. B. (Year). Title of the article. *Journal Name, Volume*(Issue), page range. https://doi.org/xxxxx
* **Use the DOI** as the closing element when one exists; fall back to a stable URL only when no DOI is available.
* **Authors:** invert every name (Surname, F. M.); use an ampersand before the final author; for 21 or more authors, list the first 19, an ellipsis, then the final author.
* **Italicize** the journal name and volume number; do not italicize the issue number or pages.
* Provide an in-text citation (Author, Year) at each point in the report where a source is referenced, matching it to its reference-list entry.
