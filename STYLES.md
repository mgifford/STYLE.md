# STYLES.md: Design and content standards

This file defines how standards are written, designed, and published in this project.
It governs two distinct surfaces and is the authoritative reference for both humans
and AI coding agents contributing to this repository.

---

## Scope: documentation files vs. the website

This project has two surfaces that share the same standards:

| Surface | Files | Audience |
| :--- | :--- | :--- |
| **GitHub Pages site** | `index.md`, `_layouts/`, `assets/`, pages with front matter | Public visitors browsing the site |
| **Repository documentation** | `README.md`, `AGENTS.md`, `STYLES.md`, `ACCESSIBILITY.md`, `SUSTAINABILITY.md`, `examples/*.md`, `templates/*.md` | Contributors, adopters, and AI agents reading files directly on GitHub |

**What applies to both surfaces:**
- Section 2 — Content and voice standards (plain language, active voice, sentence-case headings, American English)
- Section 4 — Accessibility and semantic logic (heading hierarchy, alt text, link text)
- Section 5 — AI agent instructions

**What applies to the website only:**
- Section 3 — Design foundations (CSS tokens, typography, breakpoints, page layout)

Even though documentation files are rendered as plain Markdown rather than styled HTML,
they share the same voice, tone, and heading conventions as the site. This keeps the
project a unified whole for every reader, regardless of which surface they encounter first.

---

## 1. Core philosophy

We design for the reader, not the institution. The goal is to reduce cognitive load
through consistency, clarity, and radical accessibility.

1. **Reader-first.** Start with the reader's need, not the organization's structure.
2. **Plain language.** If a 12-year-old cannot understand it, it is a barrier.
3. **Inclusive by default.** See [ACCESSIBILITY.md](./ACCESSIBILITY.md) for all interaction and visual standards.
4. **Consistency is trust.** AI agents and humans must use the same tokens, patterns, and vocabulary.
5. **Sustainable by default.** See [SUSTAINABILITY.md](./SUSTAINABILITY.md) for efficiency constraints.

---

## 2. Content and voice standards

Derived from UK GDS and Digital.gov plain language standards.

### 2.1 Voice and tone

We use an **authoritative peer** tone: professional and knowledgeable, but accessible
and supportive.

| Context | Tone | Strategy |
| :--- | :--- | :--- |
| **Onboarding** | Encouraging | Focus on the benefit to the reader |
| **Technical / legal** | Precise | Be unambiguous; explain "why" if a rule is complex |
| **Error states** | Calm / helpful | Do not blame the reader; provide a clear path forward |

### 2.2 Plain language and word choice

AI agents must prioritize these substitutions:

| Avoid | Use instead |
| :--- | :--- |
| Utilize / leverage | Use |
| Facilitate / implement | Help / carry out |
| At this point in time | Now |
| In order to | To |
| Notwithstanding | Despite / even though |
| Requirements | Rules / what you need |

### 2.3 Grammar and mechanics

- **Active voice:** "The agent checks the link" — not "The link is checked by the agent."
- **Sentence case:** Use sentence case for all headings and buttons. "Save and continue" — not "Save and Continue."
- **Lists:** Use bullets for unordered items. Use numbered lists only for sequential steps.
- **Oxford comma:** Always use the serial comma in lists of three or more.

### 2.4 Spelling convention

This project uses **American English** as its default spelling standard.

| Variant | Example spellings | When to use |
| :--- | :--- | :--- |
| **American English** (default) | color, center, optimize, behavior | All documentation in this project unless overridden |
| **British English** | colour, centre, optimise, behaviour | Specify `lang: en-GB` in `_config.yml` |
| **Canadian English** | colour, centre, optimize, behaviour | Specify `lang: en-CA` in `_config.yml` |

To change the spelling variant for a derived project, update the `lang` attribute in
`_config.yml` and the `<html lang="…">` tag in `_layouts/default.html`.

> **AI agents:** Always check the `lang` attribute in `_config.yml` and apply the
> corresponding spelling rules throughout the document.

---

## 3. Design foundations (site surface only)

These rules apply to `index.md`, `_layouts/`, `assets/`, and any page with Jekyll
front matter. They do not govern plain Markdown documentation files.

### 3.0 Brand profile and pack selection

This repository supports reusable brand packs under `templates/brand-packs/`.
Each derived project should select one active brand profile and document it
explicitly so humans and AI agents apply the same design and voice rules.

**Selected profile for this repository:** `templates/brand-pack/` (single-pack mode)

Create a project-specific brand pack when any of these are true:
- The project has a distinctive visual language that should be portable.
- The project serves a specialized audience (for example, public sector or developer tooling).
- The project defines reusable component patterns that should stay consistent across repos.

At minimum, a pack should include token definitions, component contracts, voice rules,
and AI enforcement instructions.

### 3.1 Design tokens

The canonical values live in `assets/css/site.css`. This table documents the design intent.

| Token | Light value | Dark value | Requirement |
| :--- | :--- | :--- | :--- |
| `--bg` | `#ffffff` | `#0b0d10` | Base page background |
| `--bg-soft` | `#f7f7f8` | `#12161d` | Hero, footer, subtle backgrounds |
| `--text` | `#121212` | `#f3f4f6` | 4.5:1 contrast on `--bg` required |
| `--muted` | `#4b5563` | `#c5cad3` | Supporting copy; 3:1 minimum on `--bg` |
| `--line` | `#e5e7eb` | `#2a2f3a` | Cards, section separators |
| `--card` | `#ffffff` | `#0f1319` | Card backgrounds |
| `--code` | `#f3f4f6` | `#0c1016` | `<pre>` and inline code |
| `--button` | `#111111` | `#f3f4f6` | Primary CTA background |
| `--button-text` | `#ffffff` | `#111111` | Text on `--button` fill |

Both light and dark values use a single `@media (prefers-color-scheme: dark)` block.
No extra class is required.

### 3.2 Typography

- **Font stack:** `Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif`
- **Font scaling:** Use `rem` units. Never use `px` for font sizes.
- **Fluid type:** Use `clamp()` for headings: e.g. `clamp(2.1rem, 5vw, 3.8rem)`.
- **Line length:** 45–75 characters per line (`max-width: 760px` for `.prose` blocks).
- **Line height:** Minimum `1.6` for body text.

### 3.3 Responsive design (mobile-first)

Write base CSS for the smallest screen first, then enhance with `min-width` queries.

| Layer | Breakpoint | Intent |
| :--- | :--- | :--- |
| **Mobile** | `0`–`599px` (base, no query) | Single-column, touch targets ≥ 44×44 px |
| **Tablet** | `min-width: 600px` | Two-column layouts where content benefits |
| **Desktop** | `min-width: 900px` | Multi-column grids, wider prose, side panels |

### 3.4 User-preference media queries

| Query | Status | Implementation |
| :--- | :--- | :--- |
| `prefers-color-scheme` | Required | Dark/light token swap via CSS custom properties |
| `prefers-reduced-motion` | Required | Remove or reduce transitions and animations |
| `prefers-contrast` | Planned | Not yet implemented |
| `forced-colors` | Planned | Not yet implemented |

---

## 4. Accessibility and semantic logic

These rules apply to **both surfaces**.

- Use heading levels in order: `h1` → `h2` → `h3`. Do not skip levels.
- Write descriptive link text. "Read more about plain language" — not "click here."
- Every image needs meaningful alt text. Decorative images use `alt=""`.
- Use `aria-label` on landmark elements when the role is ambiguous.
- Minimum color contrast: 4.5:1 for body text, 3:1 for large text and UI components.
- See [ACCESSIBILITY.md](./ACCESSIBILITY.md) for the full commitment and severity taxonomy.

---

## 5. AI agent instructions

These rules apply to both surfaces. Agents editing documentation and agents
generating site content must follow all of them.

- Read [AGENTS.md](./AGENTS.md) before making any change to this repository.
- Identify which surface is being edited (site or documentation) and apply the correct rule set.
- Never override [ACCESSIBILITY.md](./ACCESSIBILITY.md) or [SUSTAINABILITY.md](./SUSTAINABILITY.md) constraints.
- Prefer deterministic, low-compute approaches over AI-assisted generation.
- Use American English unless `lang` in `_config.yml` specifies otherwise.
- Keep changes scoped to the minimum necessary to fulfill the user's request.
- Verify all cross-file references resolve before committing.

---

## 6. References

- [Plain Language Guidelines — Digital.gov](https://www.plainlanguage.gov/guidelines/)
- [GOV.UK Content Design Guide](https://www.gov.uk/guidance/content-design/writing-for-gov-uk)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [Brand pack templates](./templates/brand-packs/README.md)
- [ACCESSIBILITY.md](./ACCESSIBILITY.md)
- [SUSTAINABILITY.md](./SUSTAINABILITY.md)
- [AGENTS.md](./AGENTS.md)
