---
name: paper-report-comparator
description: Compare two or more independently generated Paper Reading Reports for the same research paper, verify disagreements against the source when available, and produce a grounded cross-model synthesis. Use only after multiple standalone reports exist.
---

# Paper Report Comparator — Universal SOP v2.0 Steps 9–11

## Purpose

This **separate downstream skill** accepts 2+ reports independently generated using the `research-paper-reader` skill. It does **not** re-run the paper-reading workflow, replace the standalone reports, or generate fictitious model outputs.

## Inputs

- Required: two or more complete reports on the **same paper**, with provenance/model identity if available.
- Strongly recommended: original paper in the exact version used for those reports to verify claims.
- Optional: original prompts and sampling settings.
- If source paper is unavailable, compare reports but explicitly label source-based adjudication **not performed**. Do not infer truth from model agreement.

## Step 9 — Multi-Model Analysis

1. Check that reports refer to the same paper/version and comparable reading objectives.
2. Compare **each of the eight SOP sections**: overview, background, contributions, methodology, evidence/results, discussion/limitations, critical analysis, and overall assessment.
3. Identify agreements, substantive conflicts, omissions, distinctive insights, and differences in grounding or confidence.
4. Do not rank reports based on length, eloquence, or model identity; prefer evidence quality and useful reasoning.

## Step 10 — Evidence Verification

1. For each contested or high-impact claim, return to the exact paper page/section/figure/table/equation if source is available.
2. Distinguish author claims, original evidence, each report's interpretation, and your own adjudication.
3. Mark unsupported claims, hallucinations, misattributions, and unresolved uncertainty. Preserve minority interpretations if plausible and grounded.
4. Agreement is not verification. If evidence cannot resolve a dispute, say so.

## Step 11 — Final Synthesis

1. Integrate **verified** insights into a well-supported final review, retaining meaningful disagreements and remaining uncertainty.
2. Give an explicit summary of each model's practical contributions and observable limitations.
3. Provide a short transparent methodology description: inputs, prompts/settings if known, verification process, and what was or was not independently verified.
4. Never claim additional tools, papers, or model runs beyond what actually occurred.

## Output

Follow `templates/comparison-template.md` when available. Produce (a) model comparison by SOP step, (b) disputed-claim verification table, (c) evidence-grounded final synthesis, and (d) short LLM workflow/reflection. Output may be provisional if the paper was not provided.
