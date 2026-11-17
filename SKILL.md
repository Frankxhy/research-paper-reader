---
name: research-paper-reader
description: Read, understand, critically evaluate, and review academic research papers across disciplines using a staged, evidence-grounded workflow. Use when a user supplies a research paper or asks for structured paper reading, scholarly critique, or verification of paper-related claims.
---

# Research Paper Reader

Use this skill for any scholarly paper, including empirical, experimental, theoretical, conceptual, qualitative, systematic-review, and systems research. Adapt questions to the paper's actual research design. Never assume every paper has experiments, datasets, models, architecture diagrams, or quantitative metrics.

## Operating principles

1. **Source first.** Obtain the actual paper (and supplement if available). If not accessible, ask for it or clearly label any provisional response. Do not pretend to have read missing material.
2. **Distinguish evidence.** Mark statements as `[Author claim]`, `[Evidence]`, `[Interpretation]`, `[Independent critique]`, or `[Unverified]` when ambiguity matters.
3. **Traceability.** Attach precise page/section/figure/table/equation references to material paper-specific claims when available. Never fabricate locations, quotations, data, or citations.
4. **Human agency.** Support the reader's understanding and judgment. Do not present the agent's review as the reader's independent evaluation.
5. **Flexible depth.** Begin with a fast pass; deepen only relevant sections or uncertainties. If a phase does not apply, explain why and skip it.
6. **Visual and mathematical evidence.** Inspect figures, tables, equations, appendices, and supplements when relevant; do not rely solely on extracted text.
7. **Uncertainty.** Separate unclear writing, missing evidence, and your own limited understanding. Do not equate disagreement with error.

## Workflow

### Phase 0 — Intake and research-type classification
- Record title, authors, year, venue (if given), source version, and research type. Do not guess missing metadata.
- Determine the user's objective: learn, explain, critique, compare, or draft a review.
- Identify the paper's evidence type: empirical, theoretical, qualitative, conceptual, synthesis, or mixed.

### Phase 1 — Initial understanding
1. **Overview:** Read abstract, introduction, and conclusion where present. State research question, goal, high-level approach, main claimed findings, and what remains unclear.
2. **Background & motivation:** Identify necessary concepts, prior approaches, research gap, and motivation. Distinguish authors' framing of prior work from externally verified consensus.
3. **Contributions & novelty:** Enumerate claimed contributions, their evidence, and the comparator/baseline on which novelty depends. Do not automatically endorse novelty.
4. **Orientation through evidence objects:** Scan key tables, figures, equations, examples, or exhibits *if present*. Explain their roles without assuming a system architecture.

### Phase 2 — Deep understanding
5. **Research approach & methodology:** Explain the research design, process, definitions, assumptions, materials, data, methods, and methodological fit. Read deeply where needed.
6. **Evidence & results:** Identify which results, proofs, qualitative observations, arguments, or synthesis findings support each major claim. Examine relevant uncertainty, robustness, limitations, and alternative explanations.
7. **Discussion & limitations:** Extract author-acknowledged limitations, assess potential overlooked limitations, applicability, and plausible next questions.

### Phase 3 — Critical evaluation
8. **Evaluate rigor:** Examine question significance, validity of design, evidentiary sufficiency, logical consistency, interpretation, potential confounding/bias, and reproducibility or auditability as applicable.
9. **Overall assessment:** State strongest contributions, key weaknesses, confidence in major conclusions, open questions, and possible future directions. Avoid unsupported accept/reject recommendations.

### Phase 4 — Verification and synthesis
10. **Evidence audit:** Verify important claims directly against the paper and flag ungrounded or misattributed statements. Provide a claim-to-evidence table.
11. **Optional multi-model comparison:** If other independent model outputs are supplied or accessible, apply the same questions to each, compare differences, then adjudicate using the paper. Never invent a second model's output or claim independence when none exists.
12. **Synthesis:** Prepare the user's requested deliverable. Clearly distinguish paper summary, critical review, and reflection on LLM assistance.

## Interaction protocol

- Default to presenting a concise roadmap and Phase 1 findings first. Ask whether to deepen specific areas only when necessary; otherwise proceed for a full review request.
- For difficult concepts, give a plain-language explanation followed by a technical interpretation, tied to the actual paper.
- For each substantive analytical conclusion, provide `Claim | Paper evidence | Assessment | Confidence/uncertainty` where useful.
- If a claim cannot be verified, write `Not verified from the supplied paper` and identify what's needed.
- If working with PDFs, inspect embedded visuals when they are important and available; admit when not viewable.
- For model comparisons, use the protocol in `references/model-comparison.md`.
- Use the quality checklist in `references/evaluation-checklist.md`.
- Use `templates/review-template.md` only when a full written review is requested; it is not a mandatory output for every reading task.

## Deliverables

A full paper review should cover the research problem, background, contributions, approach, evidence/results, strengths, weaknesses, open questions, and overall assessment. A separate LLM-usage report can document prompts, model identities, verification decisions, errors detected, and what the human reader independently concluded. Be transparent about what was actually done.
