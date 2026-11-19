# Reading Execution Strategy — Internal Protocol

This file describes **how the agent reads and verifies understanding**, not the report structure. The final output follows the eight SOP steps in `../templates/review-template.md`. Do not output pass notes, comprehension tests, chain matrices or internal checklists unless explicitly requested. (Exception: the *results* of the Consistency & Recomputation Audit and the Source Access Log are reported in the template.)

## Pass 0 — Source access (before Pass 1)

1. Retrieve the paper (and appendices/supplements). Build the Source Access Log: source, version, date, what was read, what was truncated or missing.
2. Check version identity if a URL is un-versioned or a second source is used (section numbering, date, abstract, figure/table numbers). Record mismatches.
3. If truncated, recover exact-version content in order: retry targeted sections/ranges; use same-version PDF/HTML; use same-version appendices and rendered PDF pages for pivotal visuals when possible. Use alternate versions only after checking identity and mark every affected citation. Otherwise log unread sections.
4. Decide figure strategy: render key pages to images if tools allow; otherwise record `caption + text only`.

## Three-Pass Reading

Passes are stages of reasoning over the **same original paper**, not separate deliverables.

### Pass 1 — Global orientation
**Goal:** a provisional picture before details.
1. Inspect title, abstract, introduction, conclusion/discussion, headings, key figures/tables/equations/examples.
2. Identify question, importance, claimed contributions, approach, main findings, scope.
3. Identify the **paper type** (experimental, observational, benchmark/dataset, formal proof, qualitative, conceptual, synthesis, systems, mixed) and select checklist probes.
4. Record uncertainties, unfamiliar concepts, and places to investigate.
5. **Exit test:** explain question, approach and claimed conclusion in plain language without copying abstract sentences.

Pass 1 conclusions are not yet confirmed.

### Pass 2 — Analytical reading
**Goal:** how the research is done and what the evidence establishes.
1. Read method/argument/proof/design and results closely, including appendices relevant to results (scoring rules, prompts/protocols, ablations, extra tables).
2. Capture **measurement rules**: metric definitions, denominators, handling of invalid/missing outputs, aggregation and weighting, baselines, comparison conditions.
3. For each major contribution build the **Claim–Evidence Reasoning Chain** (below).
4. Check conditions under which results hold: assumptions, comparisons, settings, domain, exclusions, uncertainty.
5. Read cited prior work only if accessible and critical to a specific unresolved point; otherwise state that related-work claims rest on the focal paper (or, if `novelty_check=limited`, follow the SKILL limits and label **[External check]**).
6. Maintain an internal list of unresolved questions with exact locations.
7. **Exit test:** explain how the central method/argument works, the decisive evidence, and what it actually supports.

### Pass 3 — Critical reconstruction and source check
**Goal:** rebuild the strongest argument, challenge vulnerable links, confirm fidelity.
1. Reconstruct `problem → gap → approach → evidence → warranted conclusion` without copying the paper's summary (one chain per major claim).
2. Identify weak or missing links.
3. Independently inspect the passage/figure/proof/table behind pivotal findings and critiques.
4. Run the **Consistency & Recomputation Audit** (below).
5. Run **Understanding Verification** (below); re-read targeted material for failed checks.
6. **Exit test:** explain the mechanism, evidentiary limits, the difference between author claim and your assessment, and residual uncertainty. Otherwise qualify the affected claims.

A **provisional report** is acceptable when source access prevents completion, with limits disclosed.

## Claim–Evidence Reasoning Chain

| Link | Question | Evidence to record |
|---|---|---|
| Research problem | What precise question is being answered? | Research question or framing |
| Existing limitation / gap | What is missing, inconsistent or inadequate? | Related work, motivating example, assumption |
| Proposed approach | What changed and why should it help? | Method, proof strategy, framework, procedure |
| Supporting evidence | Which observation, result, proof, case or argument supports the claim? | Actual location and conditions |
| Warranted conclusion | What can reasonably be concluded — and what cannot? | Inference with scope and caveats |

**Validation rules:** do not assume the claimed gap is objectively established; do not infer causation from correlation; do not equate proof with experimental validation, or impose experimental criteria on conceptual work; adapt the chain for non-linear arguments; for any unsupported link, return to the paper or mark uncertain. Do not add a ninth section or mandatory chain table.

## Consistency & Recomputation Audit (mandatory when the paper has numbers, tables or formal statements)

Goal: detect problems that reading alone misses. Report results in Step 5.5 as **[Reviewer recomputation]** with inputs and formulas. Prioritize items that bear on the main conclusions.

1. **Counts and denominators:** do sample/item counts in text, tables, abstract and appendices agree? Do subset sizes sum to totals? Are denominators fixed or "valid responses only"?
2. **Aggregates:** recompute headline averages/totals using the paper's stated rule (weighting, macro vs micro, handling of missing entries, imputed values such as zeros).
3. **Derived metrics:** recompute precision/recall/specificity/F1, base-rate adjusted values, effect sizes, ratios from reported raw counts; check stated multipliers/gaps.
4. **Text vs table:** compare each prose number and qualitative statement ("at or below X", "highest", "consistently") with the table values.
5. **Cross-table consistency:** same entity, same number across tables/versions; labels and names (typos, renamed models/methods/variables).
6. **Invalid/refusal/missing handling:** inspect the stated scoring rules first. Use arithmetic to test whether invalid outputs appear counted wrong, dropped or imputed; arithmetic alone does not establish the protocol. Record unresolved ambiguity.
7. **Uncertainty:** check reported intervals/tests and assumptions. Compute an exploratory uncertainty estimate only if the needed denominators, sampling design and independence assumptions are defensible; otherwise note that uncertainty cannot be reliably calculated.
8. **Chance/trivial baselines:** calculate a chance or majority-class baseline only if the task, answer space, class balance and scoring conventions make that baseline well defined; otherwise note it as unavailable or N/A.
9. **Setting flags:** do reported configurations (e.g., thinking/reasoning modes, hyperparameters, sample sizes) match the way results are described?
10. Record each discrepancy with locations; classify as *typo-like*, *interpretation-affecting*, or *conclusion-affecting*. Do not assert the cause unless the source states it.

Adapt for non-quantitative papers: check internal consistency of definitions, premises, coding schemes, case counts, quotation attributions, proof steps.

## Understanding Verification — Explain, Test, Repair

1. **Independent explanation** of question and central idea without rephrasing the abstract.
2. **Mechanism / argument:** why and under which assumptions it should work; inputs, steps, outputs.
3. **Evidence mapping:** decisive evidence for a central conclusion; what is established vs inferred.
4. **Boundary / counterexample:** a limitation, failure mode, or alternative interpretation (labeled as hypothesis).
5. **Concrete illustration (optional):** a small worked example with the paper's own definitions, labeled illustrative.
6. **Confidence calibration:** what remains unknown, inaccessible, only claimed, or dependent on external literature.

**If a check fails:** locate the specific concept/figure/proof step; revisit the source; rebuild the chain and repeat; if unresolved, preserve uncertainty and narrow the claim.

Do not expose invented private thought processes; report only the supported explanation and substantive unresolved questions through the template. Prioritize questions that materially change main claims or the overall assessment.

## Final output invariants

- One Paper Reading Report with the eight named SOP steps, metadata, Source Access Log summary, report-local ID scheme (C/F/S/W), and Markdown claim-to-evidence audit. A machine-readable block is optional (`structured_export`).
- Pass notes, chains, and comprehension checks stay internal.
- No model comparisons, leaderboards or LLM-usage appendix.
- Never claim verification or comprehension of inaccessible information.