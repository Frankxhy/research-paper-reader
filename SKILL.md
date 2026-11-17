---
name: research-paper-reader
description: Independently read and critically evaluate a single academic research paper, regardless of discipline or research design, and generate a detailed evidence-grounded Paper Reading Report using Universal Research Paper Reading SOP v2.0 steps 1–8. Use when given a paper/PDF/full text to understand or review. Do not compare LLMs or synthesize multiple model reports.
---

# Research Paper Reader — Universal Research Paper Reading SOP v2.0

## Purpose and scope

Read **one** research paper comprehensively and produce **one** standalone, detailed, traceable **Paper Reading Report**. This skill is designed to be run independently by different models with the **same paper and standardized report format**. It must never assume that another model's output exists or attempt multi-model comparison.

Applicable to empirical, experimental, theoretical, mathematical, qualitative, conceptual, computational, survey/review, and mixed-methods papers. Adapt questions to the study type. A paper without experiments does not fail for lacking benchmarks, and one without figures does not fail for lacking architecture diagrams.

**Read** `templates/review-template.md` when it is accessible; follow its eight sections and evidence audit. Its placeholders are questions to answer, not a license to fabricate details.

## Required principles

1. **Read the actual source.** Use the full paper whenever available. If a section, figure, appendix, supplement, or PDF page cannot be accessed, explicitly describe the limitation. Never claim to have inspected inaccessible material.
2. **Source-ground every important observation.** Cite exact page/section/figure/table/equation where possible. Never fabricate quotation, numbers, sources, or citation locations.
3. **Distinguish four things:** what authors claim, evidence the paper presents, your interpretation, and your criticism. Author-stated novelty is not proven novelty.
4. **Independence:** Do not consult, cite, imitate, or infer other model reports. Do not use multi-model voting or consensus.
5. **Discipline neutrality:** Select evidence standards appropriate to the paper; do not force experiments, baselines, code, datasets, or architecture descriptions on every research genre.
6. **Depth over volume:** Provide enough technical and evidentiary detail to evaluate the argument, without redundant paraphrases. Explain essential specialized concepts.
7. **Honest uncertainty:** Mark unsupported or unverified claims. If external prior-work validation was not performed, state that novelty judgments rely on the paper's own framing.
8. **Author versus reviewer:** Clearly mark your independent critique, including limitations absent from the authors' discussion.
9. **No invention of LLM activities:** This skill generates only its own analysis. A separate comparison skill handles independent reports from other models.

## Input

- Required: one paper's PDF, full text, or reliably accessible paper source.
- Optional: user objective (learning, detailed critique, literature review), discipline, desired depth, supplementary materials.
- If only an abstract is available, label the output **abstract-only preliminary analysis**, and do not claim a full reading.

## SOP — Phase 1: Initial Understanding

### Step 1 — Overview
Answer:
- What research problem does the paper address?
- Why is the problem important?
- What is the authors' central idea?
- What are the main conclusions?

Read the abstract, introduction, conclusion, and other key orientation material where available. Summarize the paper in your own words. Record open questions.

### Step 2 — Background & Motivation
Answer:
- What is the research background or context?
- What limitations or gaps in existing research are discussed?
- Why did the authors pursue this work?
- What prior knowledge is needed to understand it?

Explain prerequisite concepts and cited background accurately. Distinguish the authors' portrayal of prior work from independent confirmation.

### Step 3 — Contributions & Novelty
Answer:
- What contributions do the authors explicitly claim?
- How do these differ from earlier work?
- Are they a new method, discovery, framework, empirical insight, or improvement?
- Is there enough evidence to support the novelty claims?

Trace each claimed contribution to its location and supporting evidence. Distinguish perceived novelty from verified novelty.

## SOP — Phase 2: Deep Understanding

### Step 4 — Research Approach & Methodology
Answer:
- Which research methods are used?
- How is the research designed and executed?
- What technologies, data, concepts, theories, definitions, or assumptions are central?
- Why was this approach selected?
- Is the method appropriate for the stated problem?

Explain mechanisms, assumptions, choices, and relevant equations/figures/tables/examples **if present**. Do not require a system architecture.

### Step 5 — Evidence & Results
Answer:
- What evidence does the paper provide?
- What are the major results?
- Do these results support the conclusions?
- Which results need additional checking?
- For nonexperimental papers, how do arguments, formal proofs, conceptual analysis, qualitative evidence, or synthesis support the claims?

Tie every important result to an observable source location. Discuss relevant uncertainty and competing explanations. Separate evidence from interpretation.

### Step 6 — Discussion & Limitations
Answer:
- How do the authors interpret the results?
- What limitations do the authors acknowledge?
- What plausible limitations remain unaddressed?
- How transferable or generalizable are the conclusions?
- What follow-up questions or research directions arise?

Do not assert hypothetical weaknesses as established failures.

## SOP — Phase 3: Critical Evaluation

### Step 7 — Critical Analysis
Answer:
- Is the research question important and well-formed?
- Are the contributions genuinely novel, to the extent verifiable?
- Is the methodology sound and rigorous?
- Is the evidence sufficient and reliable?
- Are there logical gaps, bias, confounders, unreasonable premises, or alternative interpretations?
- What are the paper's **most significant strengths and weaknesses**, and why?

For every major critique, cite the relevant source or clearly label a reasoned inference. Use `references/evaluation-checklist.md` where available.

### Step 8 — Overall Assessment
Answer:
- What is the paper's greatest value?
- How credible are its conclusions?
- How does it contribute to the field?
- Which questions remain open?
- What did the reader learn from the work?

Give an intellectually independent, balanced assessment; identify strengths, limitations, unresolved uncertainty, and promising directions.

## Required output — Paper Reading Report

Produce all eight numbered sections from `templates/review-template.md` in order; complete the claim-to-evidence audit. Use **N/A + reason** for a non-applicable question, and **Not verified** for unsupported statements. The report must be self-contained enough that a second model can compare it without relying on conversational context.

Report metadata should include paper title/authors/version, evidence accessed, scope limitations, and model name **only if reliably known**. Do not embed a multi-model comparison or fabricated model-evaluation narrative in the report.

## Explicit exclusions

- No running or comparing multiple models.
- No cross-model consensus, rankings, or adjudication.
- No final synthesis across reports.
- No invented additional references or source evidence.
- Do not automatically generate a separate LLM usage report.

For comparison of independently generated reports, use the distinct `skills/paper-report-comparator/SKILL.md` skill.
