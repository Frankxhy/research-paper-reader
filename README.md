# Research Paper Reader — Universal Agent Skill

A reusable, discipline-neutral Agent Skill for understanding and critically reviewing academic papers. It emphasizes evidence grounding, human judgment, and optional multi-model verification.

## Contents

- `SKILL.md` — actionable agent instructions
- `references/evaluation-checklist.md` — flexible scholarly quality checks
- `references/model-comparison.md` — optional independent multi-LLM comparison
- `templates/review-template.md` — review and LLM-usage report structures

## Getting started

Install this directory in the skills location supported by your Agent Skills-compatible tool, or point a compatible agent to `SKILL.md`. Installation and invocation details depend on the agent product. Publishing this folder to GitHub does not automatically install it in all tools.

Ask your agent: “Use the research-paper-reader skill to read this paper. Start with a fast pass, then examine the evidence behind its main claims and produce a critical review.”

## Design principles

1. No assumed paper discipline or methodology.
2. Every material claim should be traceable to source evidence where possible.
3. The agent should disclose uncertain or inaccessible evidence.
4. Multi-model comparison is optional and must reflect models actually run.
5. The final academic judgment remains with the reader.

## Status

Initial draft v0.1; validate with papers from different disciplines before treating as mature.
