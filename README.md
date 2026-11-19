# Research Paper Reader — Universal Research Paper Reading SOP

Four modular Agent Skills separate **deep reading**, **multi-report synthesis**, **concise academic writing**, and **critical review of the written review**.

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
    ├── academic-review-writer/
    │   ├── SKILL.md
    │   ├── templates/
    │   │   └── academic-review-template.md
    │   └── references/
    │       └── writing-standards.md
    └── academic-review-critic/
        ├── SKILL.md
        ├── templates/
        │   └── critique-template.md
        └── references/
            └── review-rubric.md
```

## Skill 1 — [Research Paper Reader](skills/research-paper-reader/SKILL.md)

**Input:** One research paper (PDF, full text, or accessible source).

**Output:** One detailed [Paper Reading Report](skills/research-paper-reader/templates/review-template.md) using the **eight Universal Research Paper Reading SOP steps**.

- Phase 1: Step 1 Overview; Step 2 Background & Motivation; Step 3 Contributions & Novelty
- Phase 2: Step 4 Research Approach & Methodology; Step 5 Evidence & Results; Step 6 Discussion & Limitations
- Phase 3: Step 7 Critical Analysis; Step 8 Overall Assessment

Uses [Three-Pass Reading → Claim–Evidence Reasoning Chain → Understanding Verification + Consistency/Recomputation Audit](skills/research-paper-reader/references/reading-strategy.md) internally. It remains a complete, deep analysis, not the short final academic review. Skill 1 adds source access/version recovery logs, figure inspection status, benchmark/dataset evaluation probes, reviewer-derived calculations and report-local evidence IDs. Its Markdown evidence audit is required; YAML/JSON export is optional.

## Skill 2 — [Paper Report Synthesizer](skills/paper-report-synthesizer/SKILL.md) (optional)

**Input:** Two or more independently generated Skill 1 detailed reports for the same paper, preferably with the original source.

**Output:** One **unified detailed Paper Reading Report** in **exactly the same eight-step format** as Skill 1.

Internally compares evidence, resolves disagreements and integrates complementary insights. Claim IDs are local to each input report, so Skill 2 matches content and source evidence rather than assuming C1/F1 IDs align across models. No model-by-model breakdown, rankings or LLM-usage commentary appears in its final report. It continues to use [Skill 1's shared detailed report template](skills/research-paper-reader/templates/review-template.md).

## Skill 3 — [Academic Review Writer](skills/academic-review-writer/SKILL.md)

**Input:** One detailed report from **either Skill 1 or Skill 2**, preferably with the original paper for verification.

**Output:** One **concise, evidence-preserving Academic Review** using the independent [six-section academic review template](skills/academic-review-writer/templates/academic-review-template.md), usually **1,000–1,200 English words** by default (unless a different length is requested or essential evidence requires more space).

Skill 3 prioritizes findings, removes duplication, preserves citations and important caveats, and turns structured reading notes into coherent academic prose. It does **not** independently read a new paper, merge multiple detailed reports, or invent support for claims. See [writing standards](skills/academic-review-writer/references/writing-standards.md).

## Skill 4 — [Academic Review Critic](skills/academic-review-critic/SKILL.md)

**Input:** A concise Skill 3 Academic Review. For stronger factual checking, also provide the corresponding Skill 1/2 detailed report and the original paper.

**Output:** One [Academic Review Critique & Revision Plan](skills/academic-review-critic/templates/critique-template.md), not a rewritten paper review.

Skill 4 evaluates evidence fidelity, coverage, methodological understanding, critical depth, citations, coherence, concision and academic writing quality using its [review rubric](skills/academic-review-critic/references/review-rubric.md). It identifies specific passages, prioritizes Critical/Major/Minor issues, and produces concrete revision instructions for Skill 3. The degree of verification must match the sources actually inspected.

## Workflows

**Single-model workflow:**
```text
Paper → Skill 1 (detailed eight-step report) → Skill 3 (concise review) → Skill 4 (critique)
```

**Multi-model workflow:**
```text
Paper → Skill 1 (model A) ─┐
       → Skill 1 (model B) ├→ Skill 2 (unified detailed report) → Skill 3 (concise review) → Skill 4 (critique)
       → Skill 1 (model C) ┘
```

Skill 2 is optional; Skill 3 can take a Skill 1 report directly. Skill 4 reviews Skill 3's output and, when needed, produces targeted instructions for a revision in Skill 3. Preserve intermediate detailed reports to enable accurate cross-checking.

## Installation notes

Each skill is housed under its own `skills/<skill-name>/SKILL.md`. Install or expose the folder to the agent environment you are using; simply hosting the files on GitHub does not install the skills. Skill 2's `../research-paper-reader/templates/review-template.md` relative reference requires a visible Skill 1 template when installed. Skill 3 carries its own template and writing standards and can run independently when a detailed report is supplied. Skill 4 carries its own rubric and critique template; the Skill 3 output is its required input.

## Validation status

All four skill specifications and relative references can be inspected in this repository. Practical end-to-end testing with a real paper and independent model outputs remains necessary.
