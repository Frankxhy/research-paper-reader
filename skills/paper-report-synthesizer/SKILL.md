---
name: paper-report-synthesizer
description: Synthesize two or more independent Research Paper Reader reports for the same paper into ONE unified, evidence-grounded Paper Reading Report with exactly the same eight-section format as the original research-paper-reader output. Internally compare and verify claims, but do not expose model-by-model comparisons or evaluation.
---

# Paper Report Synthesizer — Unified Paper Reading Report

## Goal

**Many Skill 1 reports in; ONE Skill 1-format report out.** This is not a model evaluation deliverable.

The final output must read like a single high-quality Paper Reading Report written by one reviewer. It must follow the same Universal Research Paper Reading SOP v2.0 **Steps 1–8**, headings, order, level of detail, and claim-to-evidence audit as the primary skill's template at `../research-paper-reader/templates/review-template.md`.

Do not add a separate comparison, model ranking, voting, provenance ledger, LLM-reflection appendix, synthesis methodology section, or "what each model said." Keep the work of comparison internal.

## Inputs

- Required: **two or more independently produced reports** on the same paper, ideally all produced using the `research-paper-reader` skill.
- Strongly recommended: the **original paper, same version** each report evaluated. Read it to resolve evidence questions wherever possible.
- Optional: supplementary material and user priorities.

Verify that all reports refer to the same paper/version. When they do not, flag the mismatch and only synthesize claims whose sources and context are adequately comparable.

## Internal-only workflow (SOP v2.0 Steps 9–11)

### Step 9 — Internal multi-report analysis
1. Extract content from each report into the **eight common SOP sections** (Overview; Background & Motivation; Contributions & Novelty; Research Approach & Methodology; Evidence & Results; Discussion & Limitations; Critical Analysis; Overall Assessment).
2. Identify common findings, complementary details, contradictions, gaps, repeated unsupported claims, and distinct but potentially valid critiques.
3. Evaluate each claim based on factual grounding, methodological soundness, and reasoning quality — not which model wrote it or how many models agreed.
4. Maintain an internal claim matrix if useful. **Do not output the matrix.**

### Step 10 — Internal evidence verification
1. Validate the central claims and disagreements directly against the original paper wherever accessible, including figures, tables, equations, and appendices when relevant.
2. Distinguish author claims, original evidence, interpretations, and independent critiques.
3. Resolve discrepancies through evidence. When resolution is impossible, qualify or omit doubtful claims rather than average conflicting statements.
4. Agreement is **not** evidence; do not turn repeated errors into confident claims.
5. If the original source is unavailable, do not claim independent source verification; clearly mark unverified material in the corresponding report section/audit without discussing models.

### Step 11 — Single-report synthesis
1. Write **one complete report**, following the exact output template of Skill 1.
2. Combine complementary, well-supported insights, remove duplication, correct errors, and preserve useful nuanced critiques.
3. Make each section coherent, not a collage of separate report excerpts. Use one consistent voice and terminology.
4. Retain only paper-specific source citations that can be confirmed from the available paper. If a cited location exists only in an input report and has not been checked, mark it unverified.
5. Treat paper type appropriately: theoretical work may be judged by proofs, qualitative work by methods and interpretive rigor, surveys by selection/synthesis, and so forth.
6. Do not invent paper facts, external verification, experiments, citations, or personally performed procedures.

## Mandatory final output contract

**Exactly one** "Paper Reading Report — Universal SOP v2.0" with:

- Report metadata (paper identification and access limitations; do not list contributing LLMs)
- Phase 1: Step 1 Overview; Step 2 Background & Motivation; Step 3 Contributions & Novelty
- Phase 2: Step 4 Research Approach & Methodology; Step 5 Evidence & Results; Step 6 Discussion & Limitations
- Phase 3: Step 7 Critical Analysis; Step 8 Overall Assessment
- Claim-to-Evidence Audit and relevant limitations

Use `../research-paper-reader/templates/review-template.md` as the **single source of truth** for the complete layout and subquestions. The synthesized report should be directly interchangeable with a report from Skill 1.

### Never include in the final report

- "Model A says...", "Model B disagrees...", consensus counts or model names
- Comparison tables, rankings, model-quality assessments, separate verification workflow narratives
- A distinct synthesis/comparison report or LLM Usage Report unless expressly requested by the user

### Uncertainty

If evidence is missing, say **Not verified** or explain the specific limitation in the relevant section or audit. The final deliverable remains a single unified paper review, not a comparison.

See `references/synthesis-checklist.md` for internal safeguards.
