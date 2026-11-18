# Research Paper Reader — Universal Research Paper Reading SOP

Three modular Agent Skills separate **deep reading**, **multi-report synthesis**, and **concise academic writing**.

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
    │       ├── evaluation-checklist.md
    │       └── reading-strategy.md
    ├── paper-report-synthesizer/
    │   ├── SKILL.md
    │   └── references/
    │       └── synthesis-checklist.md
    └── academic-review-writer/
        ├── SKILL.md
        ├── templates/
        │   └── academic-review-template.md
        └── references/
            └── writing-standards.md
```

## Skill 1 — [Research Paper Reader](skills/research-paper-reader/SKILL.md)

**Input:** One research paper (PDF, full text, or accessible source).

**Output:** One detailed [Paper Reading Report](skills/research-paper-reader/templates/review-template.md) using the **eight Universal Research Paper Reading SOP steps**.

- Phase 1: Step 1 Overview; Step 2 Background & Motivation; Step 3 Contributions & Novelty
- Phase 2: Step 4 Research Approach & Methodology; Step 5 Evidence & Results; Step 6 Discussion & Limitations
- Phase 3: Step 7 Critical Analysis; Step 8 Overall Assessment

Uses [Three-Pass Reading → Claim–Evidence Reasoning Chain → Understanding Verification](skills/research-paper-reader/references/reading-strategy.md) internally. It remains a complete, deep analysis, not the short final academic review.

## Skill 2 — [Paper Report Synthesizer](skills/paper-report-synthesizer/SKILL.md) (optional)

**Input:** Two or more independently generated Skill 1 detailed reports for the same paper, preferably with the original source.

**Output:** One **unified detailed Paper Reading Report** in **exactly the same eight-step format** as Skill 1.

Internally compares evidence, resolves disagreements and integrates complementary insights. No model-by-model breakdown, rankings or LLM-usage commentary appears in its final report. It continues to use [Skill 1's shared detailed report template](skills/research-paper-reader/templates/review-template.md).

## Skill 3 — [Academic Review Writer](skills/academic-review-writer/SKILL.md)

**Input:** One detailed report from **either Skill 1 or Skill 2**, preferably with the original paper for verification.

**Output:** One **concise, evidence-preserving Academic Review** using the independent [six-section academic review template](skills/academic-review-writer/templates/academic-review-template.md), usually approximately 3–5 pages.

Skill 3 prioritizes findings, removes duplication, preserves citations and important caveats, and turns structured reading notes into coherent academic prose. It does **not** independently read a new paper, merge multiple detailed reports, or invent support for claims. See [writing standards](skills/academic-review-writer/references/writing-standards.md).

## Workflows

**Single-model workflow:**
```text
Paper → Skill 1 (detailed eight-step report) → Skill 3 (concise academic review)
```

**Multi-model workflow:**
```text
Paper → Skill 1 (model A) ─┐
       → Skill 1 (model B) ├→ Skill 2 (unified detailed report) → Skill 3 (concise review)
       → Skill 1 (model C) ┘
```

Skill 2 is optional; Skill 3 can take a Skill 1 report directly. Preserve the intermediate detailed reports when you need a record of model analysis and original evidence.

## Installation notes

Each skill is housed under its own `skills/<skill-name>/SKILL.md`. Install or expose the folder to the agent environment you are using; simply hosting the files on GitHub does not install the skills. Skill 2's `../research-paper-reader/templates/review-template.md` relative reference requires a visible Skill 1 template when installed. Skill 3 carries its own template and writing standards and can run independently when a detailed report is supplied.

## Validation status

All three skill specifications and relative references can be inspected in this repository. Practical end-to-end testing with a real paper and independent model outputs remains necessary.
