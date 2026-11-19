---
name: research-paper-reader
description: Independently read and critically evaluate a single academic research paper, regardless of discipline or research design, and generate a detailed evidence-grounded Paper Reading Report using Universal Research Paper Reading SOP steps 1–8. Use when given a paper/PDF/full text to understand or review. Do not compare LLMs or synthesize multiple model reports.
---

# Research Paper Reader — Universal Research Paper Reading SOP

## Purpose and scope

Read **one** research paper comprehensively and produce **one** standalone, detailed, traceable **Paper Reading Report**. The skill is designed to be run independently by different models on the same paper with the same report format, so that a separate synthesis skill can compare the reports. It never assumes another model's output exists and never attempts multi-model comparison.

Applicable to empirical, experimental, benchmark/dataset, theoretical, mathematical, qualitative, conceptual, computational, survey/review, systems, and mixed-methods papers. Adapt questions to the study type. A paper without experiments does not fail for lacking benchmarks; one without figures does not fail for lacking architecture diagrams.

**Read** `templates/review-template.md`, `references/reading-strategy.md` and `references/evaluation-checklist.md` when accessible; follow the template's eight sections, ID scheme and audit. Template placeholders are questions to answer, not a license to fabricate.

## Optional parameters (use defaults if absent)

- `structured_export` — `off` (default) or `yaml` / `json`. The report always contains the Markdown Claim-to-Evidence Audit; export the same entries as machine-readable data **only when explicitly requested**.

- `language` — output language of the report (default: English). Evidence tags, IDs and section headings stay in English for cross-report alignment.
- `novelty_check` — `off` (default) or `limited`. `off` keeps the report independent of external literature: novelty conclusions are explicitly "based on the paper's own framing". `limited` allows consulting at most the 3–5 closest prior works named in the paper or found by search; put findings in a clearly separated block (Step 3.4) and label them **[External check]**. Never let an external check silently change author-claim or evidence descriptions.
- `depth` / `objective` — as given by the user (learning, critique, literature review).

## Required principles

1. **Read the actual source; log access.** Use the full paper whenever available. Keep a *Source Access Log* (see below). Never claim to have inspected inaccessible material.
2. **Source-ground every important observation.** Cite exact section/page/figure/table/equation where possible. Never fabricate quotations, numbers, sources or locators; use `Not verified` instead.
3. **Five epistemic labels** (use where the difference affects interpretation):
   - **[Author claim]** — what the authors say or assert.
   - **[Paper evidence]** — what the paper actually presents (data, proofs, observations).
   - **[Reviewer recomputation]** — a number or relation *you* derived from the paper's own data (sums, averages, confusion-matrix metrics, base-rate adjustments). State the formula/inputs. It is not an author statement and not an opinion.
   - **[Interpretation]** — your reasoned reading of what evidence means.
   - **[Independent critique]** — your assessment of weaknesses/alternatives, including ones the authors do not discuss.
4. **Independence.** Do not consult, cite, imitate, or infer other model reports. No voting or consensus.
5. **Discipline neutrality.** Select evidence standards appropriate to the paper type (see `references/evaluation-checklist.md`).
6. **Depth over volume; no duplication.** Give enough technical and evidentiary detail to evaluate the argument. Every point has one *primary location* (see "Where things live"); elsewhere cross-reference by ID rather than restating.
7. **Honest uncertainty.** Mark unsupported or unverified claims. Cited prior work is not "read" unless actually consulted.
8. **No invented activities.** The skill reports only its own analysis; multi-model comparison belongs to a separate skill.

## Input

- Required: one paper's PDF, full text, or reliably accessible source.
- Optional: user objective, discipline, depth, supplementary materials, parameters above.
- If only an abstract is available, label the output **abstract-only preliminary analysis**.

## Source Access Protocol (mandatory)

Before analysis, build a **Source Access Log** and put its summary in the report metadata:

1. For each source (HTML, PDF, appendix, supplement, code/data page) record: URL or file, **version** (v1/v2/…, date if shown), what was retrieved, and what was truncated or missing.
2. **Version discipline:** if an un-versioned URL may resolve to a different version than the one requested, verify (section numbering, date, abstract, figure numbers). If versions are mixed, tag every cited location with its version (e.g., `[v2 §5.2]`, `[v1 App. E.9]`) and say which v2 counterpart is presumed. Do not assume numbers are unchanged across versions.
3. **Source recovery order:** if retrieval is truncated or incomplete, first retry the exact requested version (including section/range-specific retrieval); next use a same-version PDF or HTML representation, then same-version appendices/supplements. If consequential figures are inaccessible and a renderer is available, inspect the matching PDF page image. Only use an alternate version after verifying its identity and explicitly tagging each affected citation. Record sections still unread after recovery; never assume the alternate version has identical results.
4. **Figure/table inspection status** (one line per consequential figure/table, or grouped): `viewed as image` / `caption + text only` / `not accessible`. Prefer rendering PDF pages to images when tooling allows. Never describe a figure's visual content you did not see.
5. Page numbers: if the source has none, say so and use section/figure/table locators.

## Internal reading execution — mandatory

Before drafting the report, execute the **Three-Pass Reading** protocol in `references/reading-strategy.md` (global orientation → analytical reading → critical reconstruction). During Passes 2–3 apply:

- **Claim–Evidence Reasoning Chain** for each central contribution: `Research Problem → Existing Limitation/Gap → Proposed Approach → Supporting Evidence → Warranted Conclusion`.
- **Understanding Verification:** explain (a) the problem, (b) mechanism/argument and assumptions, (c) why the decisive evidence supports the result, (d) a boundary or alternative interpretation, (e) residual uncertainty. If a check fails, re-read the relevant parts.
- **Consistency & Recomputation Audit (new, mandatory for any paper with numbers, tables or formal statements):** see `references/reading-strategy.md`. Check the paper's internal consistency (text vs tables vs abstract vs appendix; sample counts; denominators; averaging rules; imputed values; labels/names) and recompute the headline aggregates and conclusion-critical derived metrics **when the necessary raw values, definitions and assumptions are available**; otherwise document what prevents recomputation. Record outcomes under Step 5.5 as **[Reviewer recomputation]**.

Do **not** append pass summaries, chain matrices, or comprehension transcripts to the report.

## Analysis depth requirements

Depth is set by argumentative importance, not word count. Never satisfy a section by copying the abstract, listing method names, or repeating author claims without explanation.

- **Step 1 Overview:** coherent problem → approach → findings → conclusion narrative in your own words; scope, not just topic.
- **Step 2 Background:** the specific gap and minimum prerequisites; separate authors' portrayal of prior work from independent confirmation.
- **Step 3 Contributions:** break contributions into report-local IDs `C1…Cn`; for each: location, claimed difference, supporting evidence, status.
- **Step 4 Methodology (high priority):** explain how the approach works, assumptions, design decisions, scoring/measurement rules, and consequential equations/figures/tables.
- **Step 5 Evidence & Results (high priority):** key findings as report-local IDs `F1…Fn` with values, conditions, locations, and what is and is not established; include the consistency audit.
- **Step 6 Discussion & Limitations:** author-acknowledged limitations vs your concerns; boundary conditions; future work.
- **Step 7 Critical Analysis (high priority):** strengths `S1…` and weaknesses `W1…` with consequence for validity; severity and evidential status for each weakness.
- **Step 8 Overall Assessment:** synthesis, not repetition.

Allocate more space to the central method, decisive evidence and consequential critique.

## Where things live (de-duplication rule)

**Local ID scope:** C/F/S/W (and optional R) identifiers are unique only within this report. Independently written model reports may assign different meanings to the same ID. Skill 2 must align claims by meaning, source location, scope and evidence—not ID string.

| Content | Primary location | Elsewhere |
|---|---|---|
| Contribution claims | Step 3 table (C-IDs) | refer by ID |
| Findings and numbers | Step 5 table (F-IDs) | refer by ID |
| Author-acknowledged limitations | 6.2 | refer by ID |
| Reviewer-identified limitations/concerns | 6.3 (scope/generalization) and 7.5 (logic/validity); do not restate the same issue in both | cross-reference |
| Strengths / weaknesses | 7.6 / 7.7 (S-/W-IDs) | Step 8 refers by ID |
| Statement-level traceability | Audit table | must cover all C, high-impact F, and every W of severity High/Medium; low-importance items may be omitted |

## Citation and evidence rules

1. **Must ground:** research question and contribution claims; method descriptions; numerical findings and formal statements; author-stated limitations; every substantial critique whose premise is in the paper.
2. **Granularity:** attach locations to the claim or tightly connected group; a single vague citation for unrelated assertions is not allowed.
3. **Numbers:** preserve units, definitions, denominators, comparison conditions, sample sizes, uncertainty. Never present an inferred or rounded value as verbatim; use **[Reviewer recomputation]**.
4. **Figures and tables:** report inspection status (see protocol). Do not claim visual inspection otherwise.
5. **Cited literature:** attribute to the focal paper unless the external source was actually consulted (and then label **[External check]**).
6. **Unverifiable pointers:** never guess page/section/figure/theorem numbers.
7. **Final evidence audit:** include major contributions, pivotal findings and high-impact criticisms with status (Supported / Partial / Contradicted / Not verified) and how it was checked.

## Report acceptance criteria — self-check before submitting

- **Coverage:** all eight steps in order; non-applicable items marked `N/A (reason)`.
- **Depth:** Steps 4, 5, 7 explain mechanisms, evidence and consequences.
- **Process:** three passes, claim–evidence chains, understanding checks and the Consistency & Recomputation Audit done; nothing unverified reported as verified.
- **Traceability:** each C, key F and each W has a locator or is marked `Not verified`; Source Access Log present.
- **Faithfulness:** metrics, quotes, assumptions and limitations match the accessible source; derived numbers labeled as recomputations.
- **Separation:** the five labels are not conflated; weaknesses are marked *demonstrated* vs *concern*.
- **Research-type fit:** criteria match the study design (use the type-specific probes).
- **Balance and coherence:** specific strengths and weaknesses; minimal duplication; internally consistent.
- **Template compliance:** exact template structure including metadata, IDs and the audit (plus the machine-readable audit block). No multi-model comparison or LLM-usage report.

If a criterion cannot pass because the source is missing or illegible, disclose it and issue a **provisional** report.

## SOP — Phase 1: Initial Understanding

### Step 1 — Overview
Answer: What problem? Why important? Central idea? Main conclusions? Read abstract, introduction, conclusion and key orientation material. Summarize in your own words; record open questions.

### Step 2 — Background & Motivation
Answer: Context? Limitations/gaps discussed? Why pursued? Prerequisites? Explain prerequisites accurately; distinguish authors' portrayal of prior work from independent confirmation.

### Step 3 — Contributions & Novelty
Answer: Claimed contributions? Differences from earlier work? Type (method, discovery, framework, empirical insight, dataset…)? Is there enough evidence for the novelty claims? Assign IDs `C1…Cn`; distinguish perceived from verified novelty.

## SOP — Phase 2: Deep Understanding

### Step 4 — Research Approach & Methodology
Answer: Methods? Design and execution? Technologies/data/concepts/assumptions? Why selected? Appropriate for the problem? **Include measurement/scoring rules** (how outcomes are computed, how invalid/missing outputs are handled, aggregation and weighting). Do not require a system architecture.

### Step 5 — Evidence & Results
Answer: Evidence? Major results (IDs `F1…Fn`)? Do they support the conclusions? Which need additional checking? For non-experimental papers, how do arguments, proofs, qualitative evidence or synthesis support the claims? Complete **5.5 Consistency & Recomputation Audit**.

### Step 6 — Discussion & Limitations
Answer: Authors' interpretation? Acknowledged limitations? Plausible unaddressed limitations (concerns, not established failures)? Generalizability? Follow-up directions (author vs yours)?

## SOP — Phase 3: Critical Evaluation

### Step 7 — Critical Analysis
Answer: Is the question important and well-formed? Novelty (as verifiable)? Methodology sound? Evidence sufficient? Gaps, bias, confounders, alternative interpretations? Strengths (S-IDs) and weaknesses (W-IDs), each weakness with **Severity** (High/Medium/Low = effect on the paper's main conclusions) and **Status** (*Demonstrated* from the paper's own content or recomputation / *Concern* plausible but untested). Use `references/evaluation-checklist.md`.

### Step 8 — Overall Assessment
Answer: Greatest value? Credibility? Field contribution? Open questions? What the reader learned? Give an independent, balanced judgment, tracing back to S/W IDs.

## Required output — Paper Reading Report

Produce all eight sections from `templates/review-template.md` in order, with metadata, Source Access Log summary, ID scheme, claim-to-evidence audit and an **optional** machine-readable audit block only if `structured_export` is requested. Use **N/A + reason** for non-applicable questions and **Not verified** for unsupported statements. The report must be self-contained for later comparison. Report model name only if reliably known; if the evaluated models include the analysis model's own family, disclose it.

## Explicit exclusions

- No running or comparing multiple models; no cross-model consensus, rankings or adjudication; no synthesis across reports.
- No invented references or evidence.
- No separate LLM-usage report.

For synthesis of independently generated reports use `../paper-report-synthesizer/SKILL.md`.