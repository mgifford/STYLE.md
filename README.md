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

1. **Fork** this repository or copy [STYLES-template.md](./docs/STYLES-template.md) into your project root.
2. **Choose an example** from the [examples](./docs/examples/) folder close to your context.
3. **Customize** — replace every `[PLACEHOLDER]` with your project's real values.
4. **Connect the pillars** — add [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md) and [SUSTAINABILITY.md](https://github.com/mgifford/sustainability.md) for a full governance baseline.
5. **Wire it up** — reference `STYLES.md` in your `AGENTS.md` and LLM system prompts.

## Repository contents

| File / folder | Purpose |
| :--- | :--- |
| [docs/STYLES.md](./docs/STYLES.md) | This project's own style implementation (two-surface: site + docs) |
| [docs/STYLES-template.md](./docs/STYLES-template.md) | Minimal skeleton to copy and customize |
| [docs/examples/](./docs/examples/) | Worked examples: formal-gov, tech-minimal, low-bandwidth |
| [docs/templates/](./docs/templates/) | Blank scaffolds for starting from scratch |
| [docs/_includes/components/](./docs/_includes/components/) | Reusable Jekyll component partials used by the homepage |
| [docs/templates/brand-pack/](./docs/templates/brand-pack/) | Copy-ready brand portability kit: tokens, component contracts, and instruction snippets |
| [docs/templates/brand-packs/](./docs/templates/brand-packs/) | Multi-brand starter profiles for projects that need more than one reusable style system |
| [docs/AGENTS.md](./docs/AGENTS.md) | Operational instructions for AI coding agents |
| [docs/ACCESSIBILITY.md](./docs/ACCESSIBILITY.md) | Foundational accessibility commitment |
| [docs/SUSTAINABILITY.md](./docs/SUSTAINABILITY.md) | Environmental and efficiency constraints |

## GitHub Pages

This project publishes a browsable site at
[mgifford.github.io/STYLES.md](https://mgifford.github.io/STYLES.md) built with
Jekyll from `docs/index.md`, `docs/_layouts/`, and `docs/assets/`.

The homepage is assembled from reusable partials in `docs/_includes/components/` so
new sections can reuse existing layout and styling patterns.

## Brand portability

To maintain the same brand across repositories, start from
[docs/templates/brand-pack/](./docs/templates/brand-pack/):

1. Copy the folder into your new repository.
2. Merge `tokens.css` into your site stylesheet.
3. Add the AGENTS and STYLES snippets to enforce brand rules for humans and AI agents.
4. Keep token names and component contracts stable as your brand evolves.

For downstream adoption from another repository, copy that project's dedicated
`brand-pack/` first, then adapt values intentionally. This preserves the original
style fingerprint better than regenerating from prose alone.

## AI disclosure

This section lists every AI tool known to have contributed to this project, what it was used for, and where it operates. AI tools that were not used are not listed.

| AI tool | Role | Where it operates |
| :--- | :--- | :--- |
| GitHub Copilot (Claude Sonnet) | Used to draft and refine documentation, including this disclosure section and related `AGENTS.md` instructions | Build-time / authoring only — not present at runtime or in the browser |

**Runtime AI:** No AI model runs at runtime. This project is a static documentation site served by GitHub Pages. No server-side or client-side AI inference occurs when the site is loaded.

**Browser-based AI:** No browser-based AI is enabled. The site contains no JavaScript that invokes an AI API, no on-device model, and no AI-powered browser extension is required or assumed.

**How to keep this current:** When an AI tool contributes a change, the contributor (human or AI agent) must update this table. See `docs/AGENTS.md` for the AI disclosure requirement that governs this section.

## Related projects

- [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md)
- [SUSTAINABILITY.md](https://github.com/mgifford/sustainability.md)
- [AGENTS.md](https://agents.md)
