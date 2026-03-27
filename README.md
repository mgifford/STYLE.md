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
| [templates/brand-packs/](./templates/brand-packs/) | Multi-brand starter profiles for projects that need more than one reusable style system |
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

For downstream adoption from another repository, copy that project's dedicated
`brand-pack/` first, then adapt values intentionally. This preserves the original
style fingerprint better than regenerating from prose alone.

## AI disclosure

This section lists every AI tool known to have contributed to this project, what it was used for, and where it operates. AI tools that were not used are not listed.

| AI tool | Role | Where it operates |
| :--- | :--- | :--- |
| GitHub Copilot (Claude Sonnet) | Used to draft and refine documentation, including this disclosure section and related `AGENTS.md` instructions | Build-time / authoring only — not present at runtime or in the browser |
| GitHub Copilot (Claude Sonnet 4.5) | Used to expand the framework section (`section-framework.html`), add sections 2.5–2.7 and section 6 to `STYLES.md`, and update `assets/css/site.css` for new layout classes | Build-time / authoring only — not present at runtime or in the browser |
| GitHub Copilot (Claude Sonnet 4.6) | Used to integrate Opquast Digital Quality presentation rules into `STYLES.md` sections 3, 4, and 7 | Build-time / authoring only — not present at runtime or in the browser |
| GitHub Copilot (Claude Sonnet 4.6) | Used to add usability heuristics section (§ 3.5) and corresponding reference to `STYLES.md` | Build-time / authoring only — not present at runtime or in the browser |

**Runtime AI:** No AI model runs at runtime. This project is a static documentation site served by GitHub Pages. No server-side or client-side AI inference occurs when the site is loaded.

**Browser-based AI:** No browser-based AI is enabled. The site contains no JavaScript that invokes an AI API, no on-device model, and no AI-powered browser extension is required or assumed.

**How to keep this current:** When an AI tool contributes a change, the contributor (human or AI agent) must update this table. See `AGENTS.md` for the AI disclosure requirement that governs this section.

## Related projects

- [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md)
- [SUSTAINABILITY.md](https://github.com/mgifford/sustainability.md)
- [AGENTS.md](https://agents.md)
