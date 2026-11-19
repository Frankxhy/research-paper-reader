# Evidence Fidelity, Uncertainty, and Critical Coverage Protocol

This is a mandatory **internal audit** for Skill 4, scaled to the sources actually supplied. Its target is the six-section Skill 3 review, not a new Skill 1 analysis or a merger of independent model reports.

## 1. Evidence Fidelity Audit

Build an internal mapping for each decisive claim in the concise review:
- Exact review section and a short verbatim excerpt.
- Corresponding detailed-report finding or claim and the precise original-paper locator/version.
- The type of statement: author claim, paper evidence, recomputation, interpretation, independent critique.
- Numerical context as applicable: task, sample count, numerator/denominator, definition, metric, input conditions, aggregation, missing/invalid-output treatment and relevant uncertainty.
- Verification level: original-paper checked / detailed-report only / review only / inaccessible.

Check for changed meanings during compression: score vs probability, per-task vs aggregate, conditional vs full-sample metric, correlation vs causation, allegation vs verified defect, and visually inspected vs caption-only examples. If an original figure or source passage was not accessed, do not characterize it as directly verified. Flag materially unsupported facts or fabricated locators; do not "repair" them by guessing.

## 2. Uncertainty Preservation Audit

Compare consequential qualifiers in the detailed report (or, where available, the original) against the polished review:
- Not verified, partially supported, source-version mismatch and inaccessible figures/appendices.
- Reviewer **concerns** vs **demonstrated** deficiencies.
- Author claims vs reviewer conclusions; interpretations vs recomputed values.
- External-validity assumptions, experimental confounders and uncertain denominators.

Classify material changes internally as:
- **Preserved** (meaning remains accurate),
- **Qualified edit required** (confidence overstated or context dropped),
- **Unsupported: remove or verify**,
- **Cannot assess at this verification level**.

A caveat can be compressed without repeating every caveat verbatim, provided meaning is not materially changed.

## 3. Critical Coverage Audit

Use the detailed report's high-impact findings, high/medium-severity critiques, core strengths and key counterexamples as the candidate set. For each, ask:
1. Is the issue material to the final review's argument or validity assessment?
2. Is it represented accurately, perhaps merged into another paragraph?
3. If omitted, was the omission reasonable given the six-section format and length?
4. Does omission change the reader's likely judgment?

Do **not** require one paragraph per detailed finding, or penalize omission of nonessential detail. Recommend additions only where their effect on interpretation warrants the words. Verify each critique connects **specific observation → consequence → confidence/status**.

## 4. Prioritization and reporting

Convert only material audit failures into the existing prioritized issue table:
- **Critical:** false/unsupported central fact, fabricated citation or reversed core result.
- **Major:** consequential dropped qualifier, unrepresented high-impact objection, or serious evidence-to-claim leap.
- **Minor:** localized clarity/citation precision or nonessential omission.

For each: exact review location → source evidence or verification limit → minimal concrete edit → expected impact. Give a paste-ready, ordered Skill 3 revision brief; never silently rewrite the review. Report verification scope truthfully. If source content is unavailable, assess only what the available level permits and mark the rest unverified.

## 5. Exit checks

- Decisive review claims traced at the available verification level.
- No inherited citation presented as independently verified.
- No material concern elevated to demonstrated error.
- Important upstream critiques represented or consciously omitted for concision.
- Revision directions preserve the six-section structure, source fidelity and requested length.
- Only one Critique & Revision Plan is output; no new audit appendix is exposed by default.
