# AGENTS.md

Repository instructions for AI coding agents working on this project.

## Project overview
This repository defines a machine-readable style standard for human and AI collaboration.

Primary goals:
- Keep guidance clear, plain-language, and implementation-ready.
- Align style decisions with accessibility and sustainability.
- Keep documentation lightweight and easy to parse by both humans and agents.

Core docs in this repo:
- `README.md`: project introduction and usage guidance.
- `STYLES.md`: canonical style framework content.
- `ACCESSIBILITY.md`: foundational accessibility commitments and guardrails.
- `SUSTAINABILITY.md`: environmental and efficiency constraints.

## Working principles
- Prefer small, focused edits over broad rewrites.
- Preserve the existing voice: concise, direct, standards-oriented.
- Keep content portable across orgs and toolchains.
- Do not add unnecessary tooling or dependencies for documentation-only changes.

## Setup commands
This repo is documentation-first and currently has no required build system.

Common commands:
- List files: `ls -la`
- Show repo status: `git status --short`
- Review changes: `git diff`

## Writing and formatting style
- Use Markdown headings in logical order (`#`, `##`, `###`).
- Keep bullets short and parallel in structure.
- Prefer active voice and plain language.
- Avoid marketing language and filler text.
- Wrap commands, paths, and filenames in backticks.
- Use relative links where possible.

## Surface-aware editing rules
This repository has two surfaces with shared intent but different implementation constraints.

### Surface 1: Repository documentation
Applies to: `README.md`, `AGENTS.md`, `STYLES.md`, `ACCESSIBILITY.md`, `SUSTAINABILITY.md`, `templates/*.md`, `examples/*.md`.
- Prioritize clarity, scannability, and portability.
- Keep guidance testable and explicit.
- Avoid site-only implementation details unless directly relevant.

### Surface 2: GitHub Pages site
Applies to: `index.md`, `_layouts/*`, `assets/*`, and any page with front matter.
- Follow token and layout constraints in `STYLES.md`.
- Preserve semantic HTML and accessible structure.
- Keep CSS minimal, reusable, and aligned with defined design tokens.

### Rules that apply to both surfaces
- `ACCESSIBILITY.md` and `SUSTAINABILITY.md` are non-negotiable constraints.
- Preserve sentence-case headings, active voice, and plain-language defaults.
- Prefer small, focused edits over broad rewrites.
- Verify links and cross-file references before finishing.

## Content requirements
When editing standards content:
- Maintain compatibility with the three-pillar model:
  - `ACCESSIBILITY.md` (foundational)
  - `SUSTAINABILITY.md` (constraints)
  - `AGENTS.md` (operational instructions)
- Keep guidance actionable: include concrete steps when possible.
- Keep guidance testable: avoid vague statements that cannot be verified.

## Validation checklist
Before finishing changes, verify:
- Markdown renders cleanly (headings, lists, links).
- Cross-references to files are correct.
- No contradictions between `README.md`, `STYLES.md`, `AGENTS.md`, `ACCESSIBILITY.md`, and `SUSTAINABILITY.md`.
- Edits stay scoped to the user request.

## Pull request guidance
- Keep PRs focused on one documentation objective.
- Include a short summary of what changed and why.
- If structure changes, mention impact on downstream users and agents.

## Precedence and scope
- Explicit user instructions in chat take highest precedence.
- For nested projects, the nearest `AGENTS.md` to edited files should be treated as authoritative.
- Treat this file as living documentation and update it when project conventions change.
