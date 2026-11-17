# Research Paper Reader — Universal Research Paper Reading SOP v2.0

Two independent, consistently organized Agent Skills for paper analysis. **Skill 1 is the primary skill.** Skill 2 is optional and only consumes reports from Skill 1.

## Repository layout

```text
research-paper-reader/
├── README.md
└── skills/
    ├── research-paper-reader/
    │   ├── SKILL.md
    │   ├── templates/
    │   │   └── review-template.md
    │   └── references/
    │       └── evaluation-checklist.md
    └── paper-report-comparator/
        ├── SKILL.md
        ├── templates/
        │   └── comparison-template.md
        └── references/
            └── model-comparison.md
```

## Skill 1 — [Research Paper Reader](skills/research-paper-reader/SKILL.md) (PRIMARY)

**Input:** One research paper (PDF or full text).

**Output:** A standalone, detailed, source-grounded **Paper Reading Report**, using the [full report template](skills/research-paper-reader/templates/review-template.md).

Follows Universal SOP v2.0 **Steps 1–8**:

- **Phase 1 — Initial Understanding:** Step 1 Overview; Step 2 Background & Motivation; Step 3 Contributions & Novelty.
- **Phase 2 — Deep Understanding:** Step 4 Research Approach & Methodology; Step 5 Evidence & Results; Step 6 Discussion & Limitations.
- **Phase 3 — Critical Evaluation:** Step 7 Critical Analysis; Step 8 Overall Assessment.

Adapts to experimental, theoretical, qualitative, conceptual, review, and other research styles. It does not require or compare other LLMs.

## Skill 2 — [Paper Report Comparator](skills/paper-report-comparator/SKILL.md) (OPTIONAL)

**Input:** Two or more independent Paper Reading Reports for the same paper, preferably also the original paper.

**Output:** Cross-model comparison, evidence verification, and synthesis using its [comparison template](skills/paper-report-comparator/templates/comparison-template.md).

Follows **Phase 4 — LLM-Assisted Verification**, Steps 9–11: Multi-Model Analysis, Evidence Verification, Final Synthesis.

## Example workflow

1. Run Skill 1 independently on the same paper in Model A and Model B, producing Report A and Report B.
2. Supply both reports and the original paper to Skill 2 to compare results and verify discrepancies.
3. Review the final synthesis and record what each model contributed or missed.

Only Step 1 is needed for single-paper reading.

## Installation

Each directory under `skills/` is an independent Agent Skill with its own `SKILL.md`. Install the relevant skill directory according to your agent's instructions; a GitHub repository alone does not activate skills. Some clients require separate installation of the two skills.

## Status

v0.3 — unified skill paths; further validation against varied paper types is recommended.
