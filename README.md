# Research Paper Reader — Universal Research Paper Reading SOP 

Two modular Agent Skills with a **single shared final report format**. Skill 1 reads a paper. Skill 2 takes multiple independent Skill 1 reports and outputs **one stronger Skill 1-format report**.

## Repository layout

```text
research-paper-reader/
├── README.md
└── skills/
 ├── research-paper-reader/
 │ ├── SKILL.md
 │ ├── templates/
 │ │ └── review-template.md # Shared final report format
 │ └── references/
 │ ├── evaluation-checklist.md
 │ └── reading-strategy.md
 └── paper-report-synthesizer/
 ├── SKILL.md
 └── references/
 └── synthesis-checklist.md # Internal only
```

## Skill 1 — [Research Paper Reader](skills/research-paper-reader/SKILL.md) (PRIMARY)

**Input:** One paper (PDF/full text).

**Output:** One standalone [Paper Reading Report](skills/research-paper-reader/templates/review-template.md).

Runs the first three phases of SOP :

- Phase 1: **Step 1 Overview, Step 2 Background & Motivation, Step 3 Contributions & Novelty**
- Phase 2: **Step 4 Research Approach & Methodology, Step 5 Evidence & Results, Step 6 Discussion & Limitations**
- Phase 3: **Step 7 Critical Analysis, Step 8 Overall Assessment**

Applicable to research papers across disciplines and research designs. No other model is required.

**Internal reading process:** Three-Pass Reading → Claim–Evidence Reasoning Chain → Understanding Verification, documented in [reading-strategy.md](skills/research-paper-reader/references/reading-strategy.md). These checks do not change the eight-step final report structure.

## Skill 2 — [Paper Report Synthesizer](skills/paper-report-synthesizer/SKILL.md) (OPTIONAL)

**Input:** Two or more independently generated reports using Skill 1, ideally with the original paper.

**Output:** **One unified Paper Reading Report, identical in structure to Skill 1's output.**

Internally runs Phase 4 (Step 9 Multi-Model Analysis, Step 10 Evidence Verification, Step 11 Final Synthesis), but these steps **do not become sections of the deliverable**. It resolves differences, checks evidence, integrates useful perspectives, and presents the result as one coherent review.

**No model-by-model breakdown, model ratings, comparison tables, or separate LLM usage report** appear in the final report. If the original paper is unavailable, source verification limitations must be disclosed in the same report's relevant sections.

Both skills use [the same report template](skills/research-paper-reader/templates/review-template.md); Skill 2 explicitly references Skill 1's template rather than maintaining a divergent output structure.

## Example workflow

1. Give the same research paper to multiple models independently, each running Skill 1. Save their Paper Reading Reports.
2. Give the reports and original paper to Skill 2.
3. Receive **one** integrated Paper Reading Report with the same eight steps and evidence audit as any Skill 1 report.

For a single model and paper, run Skill 1 only.

## Installation notes

Each folder inside `skills/` contains an independent `SKILL.md`. To use Skill 2, ensure its environment can also access Skill 1's shared template (for example, by installing both skills together). GitHub hosting does not by itself install the skills.

## Status

v0.4 — unified report format and separate synthesis skill. Validate the primary reading skill on varied paper types and inspect source-grounding before relying on the synthesis.
