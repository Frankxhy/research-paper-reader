# Conflict Resolution and Synthesis Coverage Protocol

This reference defines mandatory **internal checks**, not a new user-facing artifact. Apply to all input reports before writing the unified eight-step report. Keep any working matrix private; reflect consequential unresolved issues in the existing report sections and Claim-to-Evidence Audit, not in a separate comparison appendix.

## A. Claim normalization

For each potentially important claim, retain internally:
- Semantic proposition (not the input report's local C/F/W/R ID).
- Claim kind: paper fact, reported result, reviewer recomputation, interpretation, or independent critique.
- Exact original-paper locator and version; figures: viewed image vs caption only.
- Measurement context: task, dataset, denominator, metric, model/setting, missing-value rule, rounding, and assumptions as applicable.
- Input-report provenance **internally only**, allowing individual claims to be traced back without implying a model ranking.

Group equivalent claims by meaning and experimental conditions; do not equate numbers with different denominators or paper versions. Preserve an important unique insight even if no other report mentions it.

## B. Resolution states

Assign one internal resolution state to each material conflict:
- **Verified:** source directly supports the harmonized claim under the specified conditions.
- **Corrected:** an input claim is demonstrably wrong or misleading, with the correction checked against original evidence.
- **Unresolved:** evidence is incomplete, contradictory, unavailable, or version-incompatible; no defensible resolution is possible.
- **Not applicable:** an apparent conflict vanishes because the claims concern materially different settings, denominators, or interpretations.

These are *workflow states*, not replacements for the shared report template's Supported / Partial / Contradicted / Not verified audit statuses or Demonstrated / Concern / Unresolved critique statuses. Map accurately when writing the report.

For every material disagreement:
1. Compare exact propositions and source versions before treating it as a conflict.
2. Read the original supporting passage/table/figure, where accessible.
3. Recompute numerical discrepancies from the reported inputs; record formula, units, denominators, rounding and missing-output treatment.
4. Resolve based on evidence, **never majority vote, model identity, or model self-confidence**.
5. If unresolved, qualify or omit the affected conclusion; disclose the important limitation at its natural section and in the standard evidence audit.

Do not present a suspicion as an established defect. A conflict about evaluative judgment may have multiple defensible interpretations; preserve the reasons and conditions rather than forcing a binary winner.

## C. Synthesis Coverage Audit (mandatory)

Before finalization, check these internal categories across every input:
1. Central contributions and findings.
2. High-impact numerical or logical inconsistencies and recomputations.
3. Methodological validity threats, alternative explanations and negative/counterexample results.
4. Material access/version/citation caveats.
5. **Unique findings** appearing in only one report.

For each important item record one internal disposition:
- **Included** (with section or audit locator);
- **Merged** into another equivalent claim (with locator);
- **Excluded: disproven** (with specific evidence);
- **Excluded: low materiality / redundant** (with brief reason);
- **Unresolved / needs verification** (with the affected claim and why).

Never exclude a uniquely raised, source-grounded high-impact issue merely because other reports omitted it. Confirm that a claim's epistemic type and caveats survive merging. Recheck that every high/medium-severity weakness and every decisive finding either appears in the unified report or has a defensible exclusion reason.

## D. Human Verification / Escalation

Escalate for human verification **only** when all conditions hold:
- The unresolved issue is material to a central finding, credibility, or intended use;
- Available original sources and reasonable recovery/recomputation have failed to resolve it;
- A concrete human check (specific table, figure, version, dataset, annotation, or methodological clarification) could change the conclusion.

In the ordinary report, flag the issue concisely under the relevant step and Claim-to-Evidence Audit with **Human verification required**, a specific proposed check, and what remains unverified. Do not add a new section or a model-comparison ledger. Never claim a human check occurred without evidence.

## E. Exit checks

- All input reports inspected to their relevant full sections, not merely headlines.
- High-impact claims directly checked where the original was accessible.
- No claim promoted in certainty solely because several reports agree.
- Unique insights individually assessed.
- Conflicts reconciled, qualified, or explicitly unresolved.
- Core findings and high/medium weaknesses represented in the shared template's Claim-to-Evidence Audit.
- Exactly one Skill 1-format eight-step report remains the only final deliverable.
