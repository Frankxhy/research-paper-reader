---
name: academic-review-writer
description: Convert one detailed evidence-grounded Paper Reading Report from research-paper-reader or paper-report-synthesizer into one concise, coherent academic paper review. Preserve accurate findings, critical arguments, paper citations, qualifications and uncertainty; remove duplication and note-like scaffolding. Use when the user wants a polished short academic review rather than a detailed eight-step reading report.
---

# Academic Review Writer

## Purpose

**One detailed Paper Reading Report in → one concise academic review out.**

This is **Skill 3**, the writing stage. It does not replace the eight-step Universal Research Paper Reading SOP, does not conduct the initial independent reading, and does not synthesize multiple reports. Skill 1 and Skill 2 continue to produce their complete, detailed, interchangeable eight-step reports.

Skill 3 may operate directly on Skill 1's report or on Skill 2's unified detailed report. The final review uses a separate, shorter academic writing format; it is **not** required to reproduce the eight SOP sections or the full claim-to-evidence audit.

Read `templates/academic-review-template.md` and `references/writing-standards.md` before writing.

## Inputs

- **Required:** one complete detailed Paper Reading Report from Skill 1 or Skill 2, including its source pointers and limitations.
- **Strongly recommended:** the original paper in the same version used by that report; use it to check key quotations, numbers, figures, and claims if available.
- **Optional:** target audience, language, length, venue/style, required points, citation style and deliverable constraints.

If several separate reports are provided, do **not** silently merge them; direct the user to Skill 2 first or request one already unified report. If the detailed report is incomplete, produce a clearly qualified review; do not silently fill gaps.

## Writing procedure

1. **Identify the core thesis.** Extract the research question, most important contribution, central method, decisive result(s), and 2–4 most consequential strengths/limitations. Respect the relative importance established by evidence, not how many words the detailed report spends on a point.
2. **Create an evidence map internally.** Connect each retained concrete finding or substantive criticism to its original paper location and verification status in the input report. If the original paper is available, independently cross-check high-impact claims and cited numbers against it. Never claim verification if the paper was not inspected.
3. **Prioritize and compress.** Aim for **1,000–1,200 English words by default** (unless the user specifies otherwise). Remove repetitive background, mechanical question-by-question responses, duplicate metrics, repeated restatements of limitations, optional tables, and non-decisive examples. Preserve the central research problem, contribution, method, decisive evidence, consequential critiques, original-paper citations, and assumptions/caveats that alter meaning. Prefer deleting lower-priority material over compressing crucial evidence into ambiguous wording.
4. **Write a cohesive review.** Follow `templates/academic-review-template.md`. Explain what the authors did, what results demonstrate, and **why** the most consequential critiques affect confidence or practical value. Integrate related findings rather than stacking mini-summaries.
5. **Audit fidelity.** Compare the drafted review against the source report (and paper where accessible). Check numbers, units, sampling/evaluation conditions, authorship of claims, citations, confidence and scope. If a critical citation is only inherited from a report and not independently checked, do not present it as newly verified.
6. **Edit for density and flow.** Cut repeated factual sentences, vague praise, filler, gratuitous jargon, and arbitrary lists. Check the approximate English word count against the default range; if outside it, edit while protecting decisive evidence and material uncertainty. Do not cut the evidence needed to justify the central assessment.

## Default output contract

- Write exactly **one standalone Concise Academic Review** using `templates/academic-review-template.md` (six integrated sections: Summary; Background & Contributions; Methodology; Key Results & Evidence; Strengths & Limitations; Overall Assessment).
- **Default target: 1,000–1,200 English words** for the review body, across all six sections (an editorial target, not a reason to distort the evidence). Honor any explicit user-specified length. For especially complex papers, exceed the target only as needed to preserve essential evidence, qualifications, and a defensible critical judgment; never pad to reach the minimum.
- Choose content based on importance rather than equal section lengths. The method, decisive results, and critical judgment deserve more attention than broad background.
- Retain precise source locations for substantive findings and criticisms where provided and verifiable. Do not pad with citations or invent them.
- Preserve material uncertainties, external-validity boundaries and missing-source limitations. Mark unresolved source claims rather than laundering them into facts.
- Avoid reporting multiple model identities, comparisons, voting, internal synthesis, or the LLM-use methodology. A separate LLM Usage Explanation may be authored only if separately requested.
- Do **not** print the full claim-to-evidence matrix, reading passes, understanding verification, or drafting checklist in the review.
- Do not expand a limited source report into a seemingly comprehensive review through speculation.

## Hard exclusions

- Do not perform Skill 2's multi-model synthesis.
- Do not invent findings, results, citations, experiments, independent reproduction, or unseen source inspection.
- Do not drop a qualification that changes an important finding's interpretation.
- Do not replace the detailed report with an abridged eight-step outline; the purpose is **academic communication**, not another reading checklist.

For a single paper's detailed analysis, use `../research-paper-reader/SKILL.md`. For merging multiple independent detailed reports, use `../paper-report-synthesizer/SKILL.md`.
