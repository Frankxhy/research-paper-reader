---
name: academic-review-critic
description: Critically evaluate one concise Academic Review produced by academic-review-writer, identify evidence-grounded weaknesses, and give prioritized, actionable revision recommendations. Use to audit review accuracy, fidelity to the detailed reading report, critical depth, argumentation, citations, concision, and academic writing quality. Output an improvement assessment and revision instructions, not an unsolicited rewritten review.
---

# Academic Review Critic

## Goal and boundaries

**Skill 3 Academic Review in → one actionable critique and improvement plan out.**

This is **Skill 4**, a separate quality-assurance and editorial evaluation stage. Its subject is **the quality of the review produced by Skill 3**, not the original research paper's quality in isolation. Identify weaknesses and show how to fix them without losing the review's concise, scholarly character.

Read `references/review-rubric.md` and `templates/critique-template.md` before running. Consult `../academic-review-writer/templates/academic-review-template.md` and `../academic-review-writer/references/writing-standards.md` if available to check the intended Skill 3 output contract.

## Inputs

- **Required:** one complete concise Academic Review (Skill 3 output).
- **Strongly recommended:** its upstream detailed eight-step Paper Reading Report (Skill 1 or Skill 2) to check omissions, distortions, and inappropriate compression.
- **Strongly recommended:** the focal original paper (same version), enabling source-level verification of key facts, numbers, figures, and reference pointers.
- **Optional:** audience, word/page limit, assessment rubric, assignment instructions, reviewer priorities, and citation convention.

Apply an explicit **verification ladder**:
1. **Review only:** You can assess structure, argumentative clarity, internal coherence, and visible citation quality. Do not assert factual or completeness verification without upstream sources.
2. **Review + detailed report:** Compare review against reported evidence and inspect what was lost or distorted; distinguish inherited claims from original-paper verification.
3. **Review + detailed report + original paper:** Directly verify major numerical, methodological and critical claims against accessible source locations. Verify only material actually inspected.

If upstream inputs are inaccessible, do not guess their contents or silently substitute outside knowledge. State what the assessment cannot determine.

## Evaluation workflow

1. **Establish the target:** Identify the review's thesis, main contribution and intended audience, as well as any explicit word/page constraints. Confirm that it is the six-section Academic Review rather than the eight-step internal reading output.
2. **Map retained claims:** Inspect the review's core problem, stated novelty, method, quantitative or formal findings, interpretation, limitations, and final judgment. For each high-stakes claim, check source support at the available verification level.
3. **Evaluate using the rubric:** Assess factual fidelity and citation precision, coverage and prioritization, critical depth, methodology/results explanation, coherence and redundancy, scholarly clarity, and length proportionality. **Distinguish missing content that matters from detail intentionally omitted for concision.**
4. **Detect issue patterns:** Examples include unsupported numerical assertions; model/task/metric mismatches; caveats removed during compression; repeated conclusions; generic strengths/weaknesses without evidence; criticism with no consequence explained; mismatch between cited section and statement; exaggerated novelty or causal claims.
5. **Prioritize changes:** Label each specific finding as **Critical** (factual error/unfounded assertion), **Major** (substantial loss of evidence, reasoning, or important qualification), or **Minor** (presentation, flow, or minor repetition). Only assign a severity when supported. Rank by academic impact, not number of issues.
6. **Make fixes actionable:** For each issue, identify (a) exact current review section and short excerpt or claim, (b) what is wrong or weak, (c) supporting evidence or limitation of verification, (d) a precise edit request, and (e) why it will improve the review.
7. **Run a final audit:** Ensure each recommendation is supported, proportionate, nonduplicative, and implementable by Skill 3 with the given materials. Recheck that shortening does not erase necessary evidence or uncertainty.

## Output contract

Produce **one Review Critique & Revision Plan**, following `templates/critique-template.md`, containing:
- A brief assessment of the review's main strengths and most consequential weaknesses.
- An evidence-qualified assessment using the rubric dimensions. Scores are **optional** and should not replace explanations or imply measurement precision.
- A **prioritized revision table** with exact locations, evidenced issue statements, concrete revisions, and Critical/Major/Minor levels.
- An ordered **revision brief for Skill 3** the user can paste back to the writer.
- A short **verification coverage statement** (what was read and what remains unverified).

Do **not** automatically produce a rewritten Academic Review, silently edit any input, or invoke Skill 3. If the user separately requests a revised review, provide it as a distinct deliverable, maintaining the six-section Skill 3 format.

Do not use cross-model voting or compare underlying LLMs; Skill 2 handles multi-report synthesis. Do not inflate the number of findings to populate a checklist. A good review may need only a few well-justified improvements.

## Revision loop

Preferred workflow:

`Skill 1 → [Skill 2 when multiple models] → Skill 3 → Skill 4 → Skill 3 (revision) → Skill 4 (optional recheck)`

When a revised review is provided later, assess whether earlier **Critical/Major** issues were resolved without introducing new errors; avoid endless cosmetic revision loops. Stop when serious unsupported claims are removed and the argument is accurate, concise, and appropriately critical.

## Explicit exclusions

- No fresh independent research-paper analysis that substitutes for Skill 1.
- No synthesis of multiple detailed model reports that substitutes for Skill 2.
- No automatic rewriting or fabrication of missing evidence.
- No punitive scoring for omission of nonessential detail in a deliberately concise review.
- No false claims of source verification, running code, or inspecting inaccessible figures.
