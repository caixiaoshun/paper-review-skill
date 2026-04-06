# paper-review-skill

![GitHub Repo stars](https://img.shields.io/github/stars/caixiaoshun/paper-review-skill?style=flat-square)
![Paper Review](https://img.shields.io/badge/focus-paper%20review-0f766e?style=flat-square)
![Agent Agnostic](https://img.shields.io/badge/agents-Codex%20%7C%20Claude%20Code%20%7C%20Cursor%20%7C%20Trae%20%7C%20Copilot-1f2937?style=flat-square)
![Online Verification](https://img.shields.io/badge/verification-online%20search%20allowed-2563eb?style=flat-square)
![Review Style](https://img.shields.io/badge/writing-issue--focused%20reviewer%20style-7c3aed?style=flat-square)

Review ML/AI papers rigorously, then write reviewer comments that sound like real venue feedback instead of AI-generated executive summaries.

This skill is built around a simple idea: reading and thinking should be strict, but the final review prose should be direct, specific, and human.

> Built for paper-review workflows where "careful analysis" and "human-sounding review text" both matter.

## Why this skill exists

Most paper-review prompts fail in one of two ways:

- they are too shallow when checking claims, baselines, ablations, and reproducibility;
- or they think carefully but write in a polished "summary + long checklist" style that does not sound like a real reviewer.

This skill separates those two concerns:

- analyze the manuscript rigorously;
- write the review in an issue-focused reviewer style.

## What it does

- reads `.tex`, `.pdf`, `.docx`, and `.doc` manuscripts;
- checks claims against evidence, baselines, controls, ablations, equations, and reproducibility;
- allows online search during analysis for recent work, benchmark protocols, official docs, and implementation assumptions;
- matches venue-style review forms when the user already has one;
- writes strengths, major weaknesses, rebuttal guidance, and recommendation justifications in a more natural review tone.

## At a glance

- **Analyze first.** Read the manuscript in passes instead of pattern-matching from the abstract.
- **Verify when needed.** Use online search for recent baselines, benchmark protocols, official docs, and implementation details.
- **Write like a reviewer.** Keep the final prose short, direct, and centered on actual issues.
- **Reuse across agents.** The core workflow lives in plain Markdown under `skill/`.

## Repository layout

```text
paper-review-skill/
|- README.md
`- skill/
   |- SKILL.md
   |- agents/
   |  `- openai.yaml
   `- references/
      `- review-writing-style.md
```

## Use it with your agent

The `skill/` directory is the portable part of this repository.

### Codex

Copy `skill/` to:

```text
~/.codex/skills/paper-review-skill
```

### Claude Code

Copy `skill/` to either:

```text
~/.claude/skills/paper-review-skill
```

or a project-local directory such as:

```text
.claude/skills/paper-review-skill
```

### Copilot, Cursor, Trae, and other coding agents

These tools do not all share the same skill format, but the repository is still easy to reuse because the core content is plain Markdown.

Recommended approach:

1. Keep the `skill/` directory in your repo or prompt library.
2. Point the agent to `skill/SKILL.md` as the main workflow.
3. Load `skill/references/review-writing-style.md` when you want the final review text to sound less synthetic.

If your agent supports repository-level instructions, prompt packs, or reusable workflows, adapt the contents of `skill/` into that mechanism.

## Design choices

- **Strict analysis, restrained writing.** The skill encourages multi-pass reading, evidence checks, and external verification, but avoids bloated review prose.
- **Online verification is allowed.** It explicitly permits checking recent papers, official benchmarks, repositories, and official documentation when needed.
- **The manuscript remains primary.** External search is there to sharpen judgment, not to replace close reading of the paper.
- **Review-form aware.** If a venue form already exists, the skill follows that structure instead of forcing a generic essay template.

## Good fit

Use this skill when you want help with tasks such as:

- reviewing a conference or journal submission;
- drafting `Paper Summary`, `Strengths`, `Major Weaknesses`, or `Suggestions For Rebuttal` fields;
- checking whether a claim is actually supported by the paper's tables and ablations;
- rewriting a review that currently sounds too much like AI.

## Skill philosophy

The point of this repository is not to produce a flattering paper summary.

The point is to help an agent:

- understand what the paper actually claims;
- identify what is or is not supported;
- and write comments the way a real reviewer would.
