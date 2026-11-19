# Universal evaluation checklist

Use selectively based on research type; mark non-applicable dimensions N/A.

- **Problem and significance:** Is the question clear, relevant, and appropriately scoped?
- **Positioning:** Are the related work, definitions, and gap represented fairly?
- **Contribution:** What is new, and what evidence distinguishes it from prior work?
- **Method fit:** Is the design appropriate to the research question? Are assumptions explicit?
- **Evidence quality:** Is the chosen evidence sufficient, reliable, and reported transparently?
- **Inference:** Do the results/proofs/observations justify the conclusions? Which alternative explanations remain?
- **Robustness:** Are uncertainty, sensitivity, replication, triangulation, or counterexamples considered where appropriate?
- **Limitations and scope:** What boundaries constrain generalization or theoretical applicability?
- **Reproducibility/auditability:** Can an informed reader inspect or repeat the reasoning, materials, data, or analysis as appropriate? Are versions/dates of models, tools, data snapshots stated?
- **Internal consistency:** Do text, tables, figures, appendices and abstract agree (counts, denominators, labels, aggregates)? (Run the Consistency & Recomputation Audit.)
- **Writing and presentation:** Are key constructs, arguments, figures/tables, and conclusions understandable?

## Type-specific probes

- **Quantitative/experimental:** control/comparison groups, sampling, baselines, metrics, power/uncertainty, leakage, confounds, ablations when relevant.
- **Qualitative:** sampling rationale, coding/interpretation transparency, reflexivity, triangulation, negative cases, transferability.
- **Theoretical/mathematical:** definitions, assumptions, proof completeness, counterexamples, boundary cases, implications.
- **Conceptual/philosophical:** clarity, coherence, premises, argument validity, objections, alternative frameworks.
- **Survey/systematic review:** selection criteria, search coverage, inclusion/exclusion logic, synthesis process, publication bias.
- **Systems/engineering:** design tradeoffs, constraints, baselines, failure modes, resource costs, external validity.
- **Benchmark / dataset / evaluation-protocol papers:**
  - *Construct validity:* does each task measure what it claims to measure? Are scoring rules fully specified (multi-field answers, partial credit, thresholds/tolerances)?
  - *Data provenance and construction:* sources, selection filters, balance of classes, differences between positive and negative sources (shortcut/domain-shift risk), synthetic vs real mix, annotation procedure, annotator count and **inter-annotator agreement**, label-noise estimate, adjudication.
  - *Contamination:* could test items be in the training data of evaluated systems? Any temporal split, held-out or private set?
  - *Baselines:* human/expert baseline, chance and majority baselines, simple or classical non-ML baselines.
  - *Uncertainty:* sample sizes per task, confidence intervals/bootstrap, significance of rank differences, repeated runs, decoding settings (temperature, seeds).
  - *Fair comparison:* identical inputs and budgets across systems (modalities, frame sampling, context limits, reasoning/thinking settings, providers/quantization); invalid/refused/malformed outputs — dropped, counted wrong, or imputed?
  - *Aggregation:* how task scores combine into totals; weighting; imputed values; mixing tasks with different chance levels.
  - *Judge/annotator coupling:* LLM-as-judge validation against humans, judge also being an evaluated system (self-preference), single vs multiple references, prompt/question generation by an evaluated system.
  - *Prompt sensitivity:* variation across prompt wording and its size relative to leaderboard gaps.
  - *Deployment relevance:* base rates/prevalence, cost-sensitive metrics, calibration; are assumed thresholds justified?
  - *Time validity:* model/data snapshot dates, deprecated or preview endpoints, expected staleness.
  - *Licensing/ethics:* redistribution rights for third-party content, privacy, intended use.

Do not demand quantitative metrics from non-quantitative work or experimental baselines from a conceptual essay.