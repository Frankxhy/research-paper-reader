---
name: research-paper-reader
description: Independently read and critically evaluate a single academic research paper, regardless of discipline or research design, and generate a detailed evidence-grounded Paper Reading Report using Universal Research Paper Reading SOP steps 1–8. Use when given a paper/PDF/full text to understand or review. Do not compare LLMs or synthesize multiple model reports.
---

# Research Paper Reader — Universal Research Paper Reading SOP

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

## Analysis depth requirements

**Depth is determined by argumentative importance, not by a fixed word count.** A complete report must explain how the paper gets from its question to its conclusions. Never satisfy a section by merely copying the abstract, listing names of methods, or repeating authors' claims without explaining them.

- **Step 1 — Overview:** Provide a coherent problem → approach → findings → conclusion narrative in the reader's own words. Identify the scope, not just the topic.
- **Step 2 — Background & Motivation:** Explain the specific gap and the minimum prerequisite concepts needed to understand why the work was conducted. Do not reproduce unrelated background.
- **Step 3 — Contributions & Novelty:** Break down substantive contribution claims individually. For each, show what is claimed to differ from prior work, what evidence supports it, and what remains unverified about novelty.
- **Step 4 — Methodology (high-priority depth):** Explain the actual reasoning or operational sequence. Identify critical assumptions and design decisions; explain the roles of essential equations, figures, definitions, procedures, or cases when relevant. A reader should understand *how* the approach works, not just its label.
- **Step 5 — Evidence & Results (high-priority depth):** Explain major findings individually, report consequential concrete values or propositions faithfully, connect each to its supporting table/figure/proof/observation, and discuss what the evidence does **and does not** establish. Do not invent values or significance tests.
- **Step 6 — Discussion & Limitations:** Separate author-acknowledged limitations from your reasoned, potentially unverified concerns; identify scope and boundary conditions.
- **Step 7 — Critical Analysis (high-priority depth):** Explain why each important strength or weakness matters for validity, significance, or interpretation, using evidence and alternative explanations where applicable. Avoid generic praise or speculative criticism.
- **Step 8 — Overall Assessment:** Synthesize the strongest supported insight, evidentiary confidence, remaining uncertainty, and research implications, rather than repeating earlier headings.

Allocate more space to the paper's central method, decisive evidence, and consequential critique; use less space for routine background. A short conceptual paper and a long technical paper should not have identical report lengths. If a necessary detail is inaccessible, state the missing information instead of padding the analysis.

## Citation and evidence rules

Use **precise, verifiable pointers into the actual paper**, preferably with a section/heading and a page, or a labeled figure/table/equation/proposition when these exist.

1. **Must ground:** the research question and contribution claims; technical method descriptions; concrete numerical findings or formal statements; descriptions of author-stated limitations; and every substantial critique whose premise is in the paper.
2. **Citation granularity:** attach source locations to the relevant claim or tightly connected group of claims. A single vague citation to the entire paper does not substantiate a set of unrelated assertions. Do not manufacture a citation for general explanatory text.
3. **Numbers and formal claims:** preserve original units, definitions, denominators, comparison conditions, signs, sample sizes, uncertainty qualifiers, and exact proposition assumptions where relevant. Do not report an inferred or rounded number as a verbatim result.
4. **Figures and tables:** inspect the actual visual when its content matters. Do not claim to have inspected it if only text extraction/captions were available. Note partial visibility.
5. **Citations to cited literature:** referencing a prior study within the paper is **not** the same as independently reading that study. Attribute background to the focal paper unless the external source was actually consulted.
6. **Unverifiable pointers:** never guess page, section, figure, or theorem numbers. Use a truthful location such as a verified section heading or say `Not verified from the available source`.
7. **Epistemic labels:** distinguish `Author claim`, `Paper evidence`, `Interpretation`, and `Independent critique` when the difference affects interpretation. A critical inference does not become an author statement.
8. **Final evidence audit:** include the major contributions, pivotal findings, and high-impact criticisms; identify which are supported, partially supported, or not verified. Do not substitute the audit table for explanations in the body.

## Report acceptance criteria — self-check before submitting

The final report is ready only when all applicable checks pass:

- **Coverage:** All eight SOP steps occur in order and answer their relevant questions; non-applicable questions are explicitly justified, not silently ignored.
- **Depth:** Steps 4, 5, and 7 explain mechanisms, evidentiary support, and consequences sufficiently to judge the paper. No step is only a set of labels or an abstract paraphrase.
- **Traceability:** Each main contribution, decisive result, and consequential criticism has a real source pointer or is explicitly marked unverified.
- **Faithfulness:** Reported metrics, quotations, assumptions, mathematical claims, and limitations match the accessible source. No invented figures, citations, experiments, references, or verification activity.
- **Separation:** The paper's claims, supporting observations, agent interpretation, and independent critique are not conflated.
- **Research-type fit:** Evaluation criteria match the study design; nothing is rejected merely because it lacks an inapplicable experimental feature.
- **Balance:** Strengths and weaknesses are specific and supported; uncertainty and alternative interpretations are noted where material.
- **Coherence:** The output reads as one standalone, internally consistent report with minimal duplication.
- **Template compliance:** Follow `templates/review-template.md` including metadata and the evidence audit. Do not include multi-model comparisons or a separate LLM-usage report.

If a criterion cannot pass because the source is missing or illegible, disclose the limitation and issue a **provisional** report. Never silently treat unavailable information as checked.

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

For synthesis of independently generated reports, use the distinct `../paper-report-synthesizer/SKILL.md` skill.
