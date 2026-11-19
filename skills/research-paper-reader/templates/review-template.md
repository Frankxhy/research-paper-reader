# Paper Reading Report — Universal SOP

> **Usage:** Output template for **one paper read independently by one model**. Answer every relevant question with substantive analysis, not headings alone. Follow SOP Steps 1–8 exactly. Not a multi-model comparison template.
>
> Give exact original-paper locations (section/page/figure/table/equation, with version if more than one was used). Evidence tags: **[Author claim]**, **[Paper evidence]**, **[Reviewer recomputation]**, **[Interpretation]**, **[Independent critique]** (and **[External check]** only if `novelty_check=limited`). If evidence is absent or inaccessible write **Not verified**. Mark non-applicable prompts **N/A (reason)**.
>
> **ID scheme (for cross-report alignment):** contributions `C1…`, key findings `F1…`, strengths `S1…`, weaknesses `W1…`. Number in the order the paper presents them. **IDs are local to this report**; different model reports are not assumed to align by ID. Refer to items by ID instead of restating them.
>
> **De-duplication:** each point has one primary location (contributions → Step 3; findings → Step 5; author limitations → 6.2; reviewer concerns → 6.3 or 7.5, not both; strengths/weaknesses → 7.6/7.7). Elsewhere, cross-reference by ID.

## Report metadata

- **Paper title:** [Exact title]
- **Authors / year / venue:** [Known bibliographic details]
- **Source/version:** [DOI, URL, PDF/HTML version and date, or provided document]
- **Research type:** [Experimental, empirical, benchmark/dataset, theoretical, qualitative, conceptual, survey, systems, mixed, etc.]
- **Output language / parameters:** [language; novelty_check off/limited; structured_export off/yaml/json; objective/depth if given]
- **Source Access Log (summary):** [For each source: URL/file, verified version, scope inspected, access status (Complete / Partial / Truncated / Version mismatch / Unavailable / Not attempted), cause of failure if known, recovery attempts, substitute sources and unresolved sections; tag mixed-version citations]
- **Figure/table inspection status:** [viewed as image / caption + text only / not accessible — per consequential figure or grouped]
- **Analysis model/version:** [Only when reliably known; disclose if the paper evaluates the same model family]
- **Scope and access limitations:** [Any limitations; page-number availability; unread cited works]

**Evidence reference style:** exact source pointers beside important claims (Section, p., Fig., Table, Eq., theorem, appendix; add version tag if mixed). Unverifiable locator → **Not verified**. Keep original units, settings, assumptions.

---

## Phase 1 — Initial Understanding

### Step 1 — Overview

**1.1 Research problem:** [precise question; in/out of scope]

**1.2 Importance:** [why meaningful; for whom]

**1.3 Central idea:** [authors' approach, not yet evaluated]

**1.4 Main conclusions:** [authors' statements vs what is actually demonstrated]

**1.5 In-your-own-words summary:** [problem → approach → evidence → conclusion]

**1.6 Questions for deeper reading:** [ambiguities, unfamiliar terms]

### Step 2 — Background & Motivation

**2.1 Research context:** [discipline, literature, setting]

**2.2 Existing research:** [prior approaches/findings the authors rely on]

**2.3 Research gap:** [shortcomings the authors identify]

**2.4 Motivation:** [why new study per authors; plausible?]

**2.5 Prerequisites:** [terminology, assumptions, background concepts]

**2.6 Limits of verification:** [which prior-research statements come only from the paper]

### Step 3 — Contributions & Novelty

**3.1 Claimed contributions:**

| ID | Claimed contribution | Exact source location | Claimed difference from prior work | Supporting evidence (location / F-ID) | Initial assessment |
|---|---|---|---|---|---|
| C1 | [Contribution] | [Location] | [Comparison] | [Location] | [Supported / Partial / Not verified] |

**3.2 Contribution types:** [technique, theory, observation, proof, system, dataset/benchmark, synthesis, conceptual insight…]

**3.3 What is actually new?** [demonstrated advances vs rebranding/incremental/unverified priority claims]

**3.4 Novelty confidence:** [further literature comparison needed. If `novelty_check=limited`, add a separate **[External check]** block here listing only the works actually consulted and what they show; otherwise state that novelty rests on the paper's own framing]

## Phase 2 — Deep Understanding

### Step 4 — Research Approach & Methodology

**4.1 Research design:** [overall approach; why it fits]

**4.2 Procedure:** [reproducible conceptual sequence from the source]

**4.3 Materials and assumptions:** [data, participants, instruments, models, formal assumptions, configurations/versions]

**4.4 Key mechanisms:** [algorithms, proofs, analytical methods, qualitative procedures, argument structure]

**4.5 Measurement and scoring rules:** [metric definitions; denominators; handling of invalid/missing outputs; aggregation/weighting; tolerances; judge/annotator procedure. If not specified, write **Not verified** and say what is missing]

**4.6 Design rationale and alternatives:** [why choices were made; alternatives/tradeoffs discussed]

**4.7 Important visual and formal material (if present):** [role of consequential figures, tables, equations, examples; inspection status]

**4.8 Methodological fit and uncertainty:** [sufficient for the research question? unclear details]

### Step 5 — Evidence & Results

**5.1 Evidence type:** [measurements, experiments, proofs, qualitative, cases, conceptual arguments, synthesis…]

**5.2 Evaluation approach:** [comparisons, formal checks, metrics, baselines, sampling, coding, validation, inference methods]

**5.3 Key results:**

| ID | Finding / proposition | Evidence location | What the evidence establishes | Uncertainty / caveat |
|---|---|---|---|---|
| F1 | [Finding with values and conditions] | [Figure/table/section/proof] | [Grounded interpretation] | [Qualification] |

**5.4 Does the evidence support the claims?** [whether authors infer more than evidence permits; map to C-IDs]

**5.5 Consistency & Recomputation Audit:** [**[Reviewer recomputation]** results: what was checked (counts/denominators, aggregates, derived metrics, text-vs-table, cross-table, invalid-output handling, chance baselines, uncertainty where assumptions permit), the formula/inputs and assumptions, outcomes, and each discrepancy with locations and class (typo-like / interpretation-affecting / conclusion-affecting). State what was *not* checked]

**5.6 Additional verification needed:** [weakly supported findings, alternative explanations, counterexamples, missing checks/robustness analyses]

**5.7 Null, negative, or conflicting outcomes:** [meaningful exceptions reported]

### Step 6 — Discussion & Limitations

**6.1 Authors' interpretation:** [how they make sense of findings]

**6.2 Acknowledged limitations:** [explicit; cite; give L-IDs if useful]

**6.3 Additional potential limitations (scope, generalization, sampling, data, assumptions):** [reviewer concerns; label as concern unless demonstrated; do not repeat issues covered in 7.5]

**6.4 Generalizability and boundaries:** [settings, definitions, populations, assumptions constraining results]

**6.5 Future work:** [separate author suggestions from your own]

## Phase 3 — Critical Evaluation

### Step 7 — Critical Analysis

**7.1 Significance:** [relevant, meaningful, well posed?]

**7.2 Novelty:** [substantive advance on available evidence?]

**7.3 Methodological rigor:** [appropriate, transparent, justified?]

**7.4 Evidentiary strength:** [adequate for principal conclusions?]

**7.5 Logical issues, bias and validity threats:** [alternative interpretations, confounders, selection effects, unsupported assumptions, reasoning gaps; each with location and consequence]

**7.6 Main strengths (2–5):**

- **S1 —** [strength; specific reasoning and paper evidence]

**7.7 Main weaknesses (2–5), ordered by severity:**

- **W1 —** [weakness] — **Severity:** High / Medium / Low (effect on the paper's main conclusions) — **Status:** Demonstrated (supported by paper evidence or recomputation) / Concern (plausible, untested) / Unresolved (insufficient evidence to classify) — **Consequence:** [why it matters]

**7.8 Questions for the authors (2–5):** [specific, substantive]

### Step 8 — Overall Assessment

**8.1 Greatest value:** [single most important contribution/insight; refer to C/S IDs]

**8.2 Confidence:** [credibility of principal conclusions; separate descriptive from explanatory claims; refer to F/W IDs]

**8.3 Field impact:** [what it may change, given the evidence]

**8.4 Open questions:** [what still needs to be established]

**8.5 What was learned:** [technical, conceptual, methodological lessons]

**8.6 Final assessment:** [concise, balanced, independent judgment with qualifications]

---

## Claim-to-Evidence Audit (required)

Must cover: every C-ID, every high-impact F-ID, every W-ID of High or Medium severity, and any important recomputation or discrepancy. Low-importance items may be omitted.

| Local ID | Important statement in this report | Type: author claim / paper evidence / reviewer recomputation / interpretation / independent critique | Exact paper location | How checked | Verified status: Supported / Partial / Contradicted / Not verified |
|---|---|---|---|---|---|
| [C1/F1/W1/R1…] | [Statement] | [Type] | [Section/page/figure/etc. (+version)] | [read directly / recomputed from Table X / inferred / not checked] | [Status and limitation] |

**Optional machine-readable audit export:** Only if `structured_export=yaml` or `structured_export=json` is explicitly requested, append an equivalent record for each Markdown audit row (same local ID, statement, epistemic type, source/version, verification status, impact/severity, check method). Do not output a duplicate YAML/JSON block by default. Report-local IDs are not standardized across independent models.

**Reading limitations:** [Unavailable supplements, truncated sources, version mixing, figure inspection status, unverified novelty, inaccessible content.]

**Corrections / uncertainties:** [What should not be stated as established fact.]

> End of the standalone Paper Reading Report. Combining multiple independent reports is handled by the separate Paper Report Synthesizer skill, which must use this same eight-step report format and understand the optional export.