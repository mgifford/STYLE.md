# STYLES.md

A machine-readable style standard for human and AI collaboration.

Your style guide should be a file, not a PDF. Put it at your repo root where
every developer, reviewer, and AI coding agent can find it.

## What is STYLES.md?

STYLES.md is an open format for writing down how your project communicates —
voice, tone, design tokens, and AI agent constraints — in a single Markdown file
that both humans and machines can read, follow, and automate against.

It is part of a three-pillar ecosystem:

| Standard | Purpose |
| :--- | :--- |
| [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md) | Foundational inclusion requirements and contributor guardrails |
| [SUSTAINABILITY.md](https://github.com/mgifford/sustainability.md) | Environmental and compute-efficiency constraints |
| [STYLES.md](https://github.com/mgifford/STYLES.md) | Voice, design tokens, and AI agent style rules |

## Why does this exist?

In an era of AI-assisted development, a style guide that lives as a PDF or a
Figma board is invisible to the tools doing the work. STYLES.md makes your
standards explicit, version-controlled, and testable.

- **Humans** get a clear, plain-language reference at the repo root.
- **AI agents** get a machine-readable constraint file they can follow without guessing.
- **Reviewers** get a checklist they can verify in CI.

## How to replicate this

1. **Fork** this repository or copy [STYLES-template.md](./STYLES-template.md) into your project root.
2. **Choose an example** from the [examples](./examples/) folder close to your context.
3. **Customize** — replace every `[PLACEHOLDER]` with your project's real values.
4. **Connect the pillars** — add [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md) and [SUSTAINABILITY.md](https://github.com/mgifford/sustainability.md) for a full governance baseline.
5. **Wire it up** — reference `STYLES.md` in your `AGENTS.md` and LLM system prompts.

## Repository contents

| File / folder | Purpose |
| :--- | :--- |
| [STYLES.md](./STYLES.md) | This project's own style implementation (two-surface: site + docs) |
| [STYLES-template.md](./STYLES-template.md) | Minimal skeleton to copy and customize |
| [examples/](./examples/) | Worked examples: formal-gov, tech-minimal, low-bandwidth |
| [templates/](./templates/) | Blank scaffolds for starting from scratch |
| [_includes/components/](./_includes/components/) | Reusable Jekyll component partials used by the homepage |
| [templates/brand-pack/](./templates/brand-pack/) | Copy-ready brand portability kit: tokens, component contracts, and instruction snippets |
| [AGENTS.md](./AGENTS.md) | Operational instructions for AI coding agents |
| [ACCESSIBILITY.md](./ACCESSIBILITY.md) | Foundational accessibility commitment |
| [SUSTAINABILITY.md](./SUSTAINABILITY.md) | Environmental and efficiency constraints |

## GitHub Pages

This project publishes a browsable site at
[mgifford.github.io/STYLES.md](https://mgifford.github.io/STYLES.md) built with
Jekyll from `index.md`, `_layouts/`, and `assets/`.

The homepage is assembled from reusable partials in `_includes/components/` so
new sections can reuse existing layout and styling patterns.

## Brand portability

To maintain the same brand across repositories, start from
[templates/brand-pack/](./templates/brand-pack/):

1. Copy the folder into your new repository.
2. Merge `tokens.css` into your site stylesheet.
3. Add the AGENTS and STYLES snippets to enforce brand rules for humans and AI agents.
4. Keep token names and component contracts stable as your brand evolves.

## Related projects

- [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md)
- [sustainability.md](https://github.com/mgifford/sustainability.md)
- [agents.md](https://agents.md)
