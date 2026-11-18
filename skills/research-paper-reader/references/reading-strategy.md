# Reading Execution Strategy — Internal Protocol

This file describes **how the agent reads and verifies understanding**, not the final report's structure. Keep the final output in the eight SOP steps defined by `../templates/review-template.md`. Do not output pass notes, understanding tests, intermediate matrices, or internal checklists unless explicitly requested.

## Three-Pass Reading

Use multiple passes over **the same original paper**, not multiple models. The passes are stages of reasoning, not three separate deliverables. Adapt their depth to the paper type and the user's request.

### Pass 1 — Global orientation

**Goal:** Form a provisional picture of what the paper tries to establish before becoming absorbed in details.

1. Inspect title, abstract, introduction, conclusion/discussion, section headings, and key figures/tables/equations/examples **when available**.
2. Identify the research question, why it matters, claimed contributions, high-level approach, main findings and apparent scope.
3. Identify the evidence type (experimental, observational, formal proof, qualitative, conceptual, synthesis, or mixed); do not assume a particular discipline or paper layout.
4. Record provisional uncertainties, unfamiliar concepts, and locations to investigate.
5. **Exit test:** Can you explain the question, approach and claimed conclusion in plain language without relying on copied abstract sentences? If not, revisit relevant framing sections.

Do not treat Pass 1's conclusions as independently confirmed.

### Pass 2 — Analytical reading

**Goal:** Understand how the research is done and what its evidence establishes.

1. Read the method/argument/proof/design and results/evidence sections closely. Follow important definitions, assumptions, steps, experiments, tables, figures, equations, cases, and appendices when relevant and accessible.
2. For each major contribution, construct the **Claim–Evidence Reasoning Chain** described below.
3. Check the conditions under which results hold: assumptions, comparisons, metrics, units, populations, settings, theoretical domain, exclusions, and uncertainty.
4. Read a cited prior work only if it is accessible and critical to a specific unresolved point; otherwise state that novelty or related-work claims are based on the focal paper.
5. Keep an internal list of unresolved questions and exact source locations.
6. **Exit test:** Can you explain how the central method/argument works, what the decisive evidence is, and what conclusions it actually supports? If not, return to the relevant text or visual.

### Pass 3 — Critical reconstruction and source check

**Goal:** Rebuild the strongest plausible argument, challenge its vulnerable links, and confirm the report's fidelity.

1. Without copying the paper's summary, reconstruct: **research problem → prior limitation/gap → proposed approach → supporting evidence → warranted conclusion**. For papers with multiple contribution claims, use one chain per major claim where useful.
2. Identify every weak or missing link: unsupported gap, unclear mechanism, untested assumption, inadequate evidence, overreach in inference, or important alternative explanation.
3. Independently inspect the supporting passage/figure/proof/table for pivotal findings and critiques. Agreement with the authors' narrative is not sufficient verification.
4. Cross-check major numerical or formal claims and their scope across abstract, methods, results, and conclusion as relevant.
5. Run the **Understanding Verification** below. Re-read targeted material for failed checks; do not invent certainty.
6. **Exit test:** Can you explain the contribution's mechanism and evidentiary limits, distinguish author claims from your own assessment, and identify residual uncertainty? If not, qualify the affected report claims.

A **provisional report** is acceptable when source access genuinely prevents completion, but its limits must be disclosed within the shared report template.

## Claim–Evidence Reasoning Chain

Use the following chain **internally** for each central contribution; it is a test of logical connection, not a demand for causal experiments:

| Link | Question | Evidence to record |
| --- | --- | --- |
| Research problem | What precise question is being answered? | Research question or framing |
| Existing limitation / gap | What is missing, inconsistent, or inadequate? | Related work, motivating example, assumption |
| Proposed approach | What changed, and why should it help? | Method, proof strategy, theoretical framework, procedure |
| Supporting evidence | Which observation, result, proof, case, or argument supports the claim? | Actual source location and conditions |
| Warranted conclusion | What can reasonably be concluded—and what cannot? | Inference with scope and caveats |

**Validation rules:**

- Do not assume the claimed research gap is objectively established without checking relevant prior work.
- Do not infer causal effects from mere correlation or descriptive comparison.
- Do not equate a mathematical proof with experimental validation, or impose experimental criteria on conceptual research.
- A claim can have multiple independent lines of evidence or a non-linear argument; adapt the chain without forcing a simplistic sequence.
- For each missing or unsupported link, return to the paper or mark the corresponding conclusion as uncertain.
- Use these connections throughout the existing SOP sections; **do not add a ninth section or mandatory chain table to the final report**.

## Understanding Verification — Explain, Test, Repair

Conduct the following **internal comprehension checks** for major claims. They test explanation quality, not whether the model can confidently produce words.

1. **Independent explanation:** Restate the research question and central idea accurately in your own words, without merely rephrasing the abstract.
2. **Mechanism / argument:** Explain why and under which assumptions the method or reasoning is expected to work; identify inputs, steps, and outputs when appropriate.
3. **Evidence mapping:** For a central conclusion, point to its decisive evidence and explain what is directly established versus inferred.
4. **Boundary / counterexample:** Describe a relevant limitation, failure mode, counterexample, or plausible alternative interpretation, clearly labeling hypotheses.
5. **Concrete illustration (when useful):** Work through a small illustrative example or critical proof step using the paper's actual definitions. Label constructed illustrations as illustrative, never as an author's experiment or original result.
6. **Confidence calibration:** State what remains unknown, inaccessible, only claimed by authors, or dependent on unverified external literature.

**If a check fails:**

- Locate the specific concept, equation, figure, proof step, or finding causing confusion.
- Revisit that source; examine supplementary text or necessary definitions when accessible.
- Rebuild the relevant chain and repeat the check.
- If still unresolved, preserve the uncertainty and narrow the claim rather than fabricating an explanation.

Do not expose invented private thought processes; report only the supported explanation and any substantive unresolved questions using the existing template. Avoid unbounded re-reading: prioritize questions that materially change the paper's main claims or overall assessment.

## Final output invariants

- The final deliverable is **one** Paper Reading Report with exactly the same eight named SOP steps, metadata and claim-to-evidence audit as Skill 1's shared template.
- Pass 1/2/3, reasoning chains and comprehension checks are **internal execution mechanisms**, not report sections.
- No model comparisons, output provenance leaderboard, or additional LLM-usage appendix.
- Never claim source verification or comprehension of inaccessible information.
