# Brand pack: ai-browser-test

Derived from [mgifford/ai-browser-test](https://github.com/mgifford/ai-browser-test).

This pack captures the visual and voice fingerprint of the AI Browser Capability
Demo project, discovered during an AI-assisted style audit. Use it to replicate
that project's look and feel in another repository without starting from scratch.

## Style fingerprint summary

| Trait | Value |
| :--- | :--- |
| **Audience** | Web developers exploring browser AI APIs |
| **Voice** | Precise, direct, instructional |
| **Typography** | Fraunces (display) + Space Grotesk (body) — expressive serif paired with a legible geometric sans |
| **Palette** | Warm parchment light / deep forest dark; coral accent; teal secondary |
| **Browser tokens** | Chrome, Firefox, Edge brand colors defined as identity tokens |
| **Layout** | Single-column mobile base; 920px desktop breakpoint; 1120px constrained shell |
| **Radius** | Generous rounding (lg: 20px, md: 14px, sm: 10px) |
| **Elevation** | Pronounced card shadow to separate layers |

## Files in this pack

| File | Purpose |
| :--- | :--- |
| `tokens.css` | All CSS custom properties including browser brand tokens |
| `voice.md` | Copy rules by context: UI labels, instructions, errors, governance, code |
| `components.md` | Component contracts for matrix, card, chip, CTA, notice |
| `ai-instructions.md` | Guardrails for AI agents reusing or extending this pack |

## How to use in a new project

1. Copy this folder into your project as `brand-pack/`.
2. Import `tokens.css` at the top of your stylesheet (before any component styles).
3. Load `voice.md` into your `AGENTS.md` or LLM system prompt.
4. Follow `components.md` contracts before introducing new markup patterns.
5. Add a line to your `STYLES.md`:
   ```
   **Selected profile:** `brand-pack/` (derived from ai-browser-test)
   ```
6. Add browser brand tokens only if your project surfaces browser-specific content.
   Remove `--chrome`, `--firefox`, `--edge` if they are not relevant.
