# Research Paper Reader — Universal Research Paper Reading SOP v2.0

Two **separate Agent Skills** for a modular, evidence-grounded research-paper workflow.

## Skill 1 — Research Paper Reader (PRIMARY)

**Input:** One research paper (PDF/full text).

**Output:** One complete, standalone **Paper Reading Report**.

**SOP v2.0 — Steps 1–8:**

- **Phase 1 — Initial Understanding:** 1. Overview; 2. Background & Motivation; 3. Contributions & Novelty.
- **Phase 2 — Deep Understanding:** 4. Research Approach & Methodology; 5. Evidence & Results; 6. Discussion & Limitations.
- **Phase 3 — Critical Evaluation:** 7. Critical Analysis; 8. Overall Assessment.

The primary `SKILL.md` uses `templates/review-template.md` and `references/evaluation-checklist.md`. It works independently: no model comparisons, no cross-model synthesis, and no requirement for multiple LLMs. It adapts to experimental, theoretical, qualitative, conceptual, survey, and other research designs.

## Skill 2 — Paper Report Comparator (OPTIONAL / DOWNSTREAM)

**Input:** Two or more reports created independently by Skill 1, ideally alongside the source paper.

**Output:** Comparison, verified adjudication of disagreements, and final synthesis.

**SOP v2.0 — Steps 9–11:**

- **Phase 4 — LLM-Assisted Verification:** 9. Multi-Model Analysis; 10. Evidence Verification; 11. Final Synthesis.

This skill is defined in `skills/paper-report-comparator/SKILL.md` with its own template at `skills/paper-report-comparator/templates/comparison-template.md`.

## Directory

```text
research-paper-reader/
├── SKILL.md                                  # Skill 1
├── README.md
├── references/
│   ├── evaluation-checklist.md               # Skill 1
│   └── model-comparison.md                   # Reference for Skill 2
├── templates/
│   └── review-template.md                    # Skill 1 report structure
└── skills/
    └── paper-report-comparator/
        ├── SKILL.md                          # Skill 2
        └── templates/
            └── comparison-template.md
```

## Example use

**Step A:** Give the same paper to Model A and Model B. Ask each independently to *“Use research-paper-reader and produce a complete Paper Reading Report following SOP v2.0.”*

**Step B:** Supply the two finished reports and the original paper to a model running *paper-report-comparator*. Ask it to compare both reports, verify discrepancies against the paper, and synthesize a final critical assessment.

Only Step A is required to use this repository's primary skill.

## Installation notes

Different Agent Skills-compatible applications use different install/discovery paths. The primary skill lives at repository root; the comparator is a separate nested skill directory. Some agents require installing each skill independently. GitHub hosting alone does not activate a skill.

## Status

v0.2 modular architecture. Validate the single-paper skill on varied paper types before using model comparisons in a research deliverable.
