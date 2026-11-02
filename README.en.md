# Review Writing Skill

[中文](README.md) | English

A Codex skill for turning literature into an evidence-based review argument. It supports drafting from papers, notes or outlines, comparative reviews, and explicitly requested full rewrites.

## What it does

- Define the guiding question, scope, working definitions and contribution.
- Organize studies by concepts, mechanisms or shared tasks.
- Synthesize agreements and disagreements, explaining why findings matter.
- Check claims against original sources and relevant supplementary information.
- Compare metrics only after establishing their definitions, references, conditions and system boundaries.
- Connect figures, tables and equations to the argument.
- Draw conditional conclusions and propose specific research directions.
- Maintain new requirements through stable rule IDs and scoped additions.

The core rules are W01–W13 in [SKILL.md](SKILL.md). Project-specific examples in [references/additions.md](references/additions.md) apply only within their stated scope. The skill instructions are written in Chinese; manuscript language follows the user's request.

## Install

Clone into a local skills directory under the skill name `review-writing`:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/borin9Wang/review-writing-skill.git "${CODEX_HOME:-$HOME/.codex}/skills/review-writing"
```

For PowerShell instructions, see the [Chinese installation section](README.md#快速开始). If a personalized copy already exists, merge its additions before replacing it.

## Use

```text
Use $review-writing to draft a review from these papers and notes.
Define the guiding question and contribution, organize the evidence by theme,
and support substantive synthesis with original sources.
```

This repository supplies instructions. Literature access, document handling, rendering and plotting use tools available in the host environment.

## Extend

Ask the assistant to add or revise a rule, for example: “Add this to the writing skill: explain differences in measurement before treating findings as contradictory.” General requirements belong in `SKILL.md`; scoped preferences belong in `references/additions.md`. See [CONTRIBUTING.md](CONTRIBUTING.md).

For revisions to an existing manuscript, use the companion [review-fixing-skill](https://github.com/borin9Wang/review-fixing-skill), invoked as `$review-revision`.

## Methodological basis

The skill combines practical manuscript experience with selected principles from Karen V. Fernandez (2019), [Critically reviewing literature: A tutorial for new researchers](https://doi.org/10.1016/j.ausmj.2019.05.001). Engineering-specific evidence, metric and delivery rules are adaptations from practice. No original paper PDFs or unpublished manuscripts are included.
