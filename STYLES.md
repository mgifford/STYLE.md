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
- Section 2 — Content and voice standards (plain language, active voice, sentence-case headings, American English, abbreviations, citation, content structure)
- Section 4 — Accessibility and semantic logic (heading hierarchy, alt text, link text)
- Section 5 — AI agent instructions
- Section 6 — Content governance

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

### 2.5 Abbreviations, numbers, and dates

#### Abbreviations

- Spell out an abbreviation on first use, then use the short form: "Accessibility
  Guidelines (WCAG)."
- Do not use periods in acronyms: "HTML," "CSS," "AI" — not "H.T.M.L."
- Avoid jargon-only abbreviations without explanation unless writing for a specialist audience.

#### Numbers

| Context | Rule | Example |
| :--- | :--- | :--- |
| **In body text** | Spell out one through nine; use numerals for 10 and above | "three pillars," "12 tokens" |
| **Starts a sentence** | Always spell out | "Twelve steps are required." |
| **Percentages** | Use numerals and the % symbol | "4.5% contrast ratio" |
| **Versions and technical values** | Always use numerals | "WCAG 2.2," "font-size: 1rem" |

#### Dates

- Use **ISO 8601** for machine-readable dates: `2025-06-01`.
- Use **spelled-out months** for human-readable dates: "June 1, 2025" (American English)
  or "1 June 2025" (British/Canadian English).
- Do not use all-numeric dates that could be ambiguous across locales (01/06/2025).

### 2.6 Attribution and citation

When quoting, adapting, or referencing external work in documentation:

- **Quote directly** only when the original wording matters and cannot be improved.
  Block-quote passages over three lines.
- **Paraphrase** when the idea is what matters. Paraphrasing does not remove the need
  to credit the source.
- **Credit the source** inline or in a references section: "Derived from UK GDS Content
  Design Guide."
- **Link to the source** rather than reproducing large portions of external content.
- **Do not reproduce** entire copyrighted works, style guides, or specifications.
  Reference them and link to the canonical source.

> **AI agents:** Do not reproduce large passages from external style guides or
> specifications verbatim. Summarize, paraphrase, and link to the canonical source.

### 2.7 Content structure and document types

Different document types follow different patterns. Use the appropriate structure
rather than treating all Markdown files the same.

| Document type | Purpose | Structure pattern |
| :--- | :--- | :--- |
| **Reference** (STYLES.md, ACCESSIBILITY.md) | Authoritative rules; consulted, not read cover-to-cover | Numbered sections, tables, bullet rules |
| **Guide or how-to** (examples/, README.md) | Step-by-step walkthrough for a specific audience | Numbered steps, "you" voice, outcome-focused |
| **Template** (STYLES-template.md) | Scaffold to copy and customize | Placeholders clearly marked, minimal prose |
| **Explainer** (index.md) | Introduces concepts to someone unfamiliar with the project | Short paragraphs, definitions, analogies |

Rules that apply to all document types:

- Use heading levels in order (`#` → `##` → `###`). Do not skip levels.
- Open each document with a one-sentence purpose statement.
- Keep paragraphs short: three to five sentences is a good maximum.
- Prefer short sentences over long, complex ones.

---

## 3. Design foundations (site surface only)

These rules apply to `index.md`, `_layouts/`, `assets/`, and any page with Jekyll
front matter. They do not govern plain Markdown documentation files.
Presentation quality rules in this section are informed by the
[Opquast Digital Quality Checklist](https://checklists.opquast.com/en/digital-quality/).

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
- **Text alignment:** Use left-aligned text for body content. Avoid `text-align: justify` — it creates uneven word spacing that reduces readability.
- **Capitalization:** Use CSS `text-transform` for decorative uppercase styling. Do not write uppercase text directly in HTML source.

### 3.3 Responsive design (mobile-first)

Write base CSS for the smallest screen first, then enhance with `min-width` queries.

| Layer | Breakpoint | Intent |
| :--- | :--- | :--- |
| **Mobile** | `0`–`599px` (base, no query) | Single-column, touch targets ≥ 44×44 px |
| **Tablet** | `min-width: 600px` | Two-column layouts where content benefits |
| **Desktop** | `min-width: 900px` | Multi-column grids, wider prose, side panels |

- **Never block zoom.** The viewport meta tag must not include `maximum-scale=1` or `user-scalable=no`. Users must be able to scale the page freely.

### 3.4 User-preference media queries

| Query | Status | Implementation |
| :--- | :--- | :--- |
| `prefers-color-scheme` | Required | Dark/light token swap via CSS custom properties |
| `prefers-reduced-motion` | Required | Remove or reduce transitions and animations |
| `prefers-contrast` | Planned | Not yet implemented |
| `forced-colors` | Planned | Not yet implemented |
| `print` | Recommended | Hide navigation and decorative elements; render body text at ≥ 12pt; append `href` values on links |

### 3.5 Usability heuristics

Style decisions in this project are informed by Nielsen Norman Group's
[ten usability heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/).
Each heuristic maps to concrete style and interaction choices.

| Heuristic | Style implication |
| :--- | :--- |
| **1. Visibility of system status** | Provide visible feedback for all interactive states: hover, focus, active, and error. Use status labels in UI components so users always know what is happening. |
| **2. Match between system and the real world** | Use plain, familiar language (see § 2.2). Avoid technical jargon unless writing for a specialist audience. Order and group content the way users think, not the way the system is built. |
| **3. User control and freedom** | Design error states with a clear path forward. Do not trap users in irreversible flows without confirmation. Provide visible "undo" or "cancel" options wherever an action can be reversed. |
| **4. Consistency and standards** | Reuse the same tokens, patterns, and vocabulary defined in this file. Do not invent parallel naming systems. Platform and industry conventions take priority over novel patterns. |
| **5. Error prevention** | Prefer design that prevents problems over good error messages. Provide inline constraints, confirmation steps, and warnings before destructive actions. |
| **6. Recognition rather than recall** | Surface navigation options and contextual cues visibly. Do not require users to remember information across steps or screens. Make objects, actions, and options visible or easily retrievable. |
| **7. Flexibility and efficiency of use** | Provide keyboard shortcuts and accelerators for expert users without cluttering the default experience for newcomers. Allow users to tailor frequent actions. |
| **8. Aesthetic and minimalist design** | Remove decorative elements that compete with content. Every visual and textual element must earn its place. Irrelevant information reduces the relative visibility of useful information. |
| **9. Help users recognize, diagnose, and recover from errors** | Write error messages in plain language (see § 2.1 error-state tone), explain the cause precisely, and suggest a clear remedy. Never blame the user. |
| **10. Help and documentation** | Ensure documentation is easy to search, scoped to a specific task, and lists concrete steps. Prefer inline context over separate help pages when the user may not think to look for help. |

Where a heuristic conflicts with accessibility or sustainability constraints,
those constraints take precedence (see [ACCESSIBILITY.md](./ACCESSIBILITY.md)
and [SUSTAINABILITY.md](./SUSTAINABILITY.md)).

---

## 4. Accessibility and semantic logic

These rules apply to **both surfaces**.

- Use heading levels in order: `h1` → `h2` → `h3`. Do not skip levels.
- Write descriptive link text. "Read more about plain language" — not "click here."
- Every image needs meaningful alt text. Decorative images use `alt=""`.
- Use `aria-label` on landmark elements when the role is ambiguous.
- Minimum color contrast: 4.5:1 for body text, 3:1 for large text and UI components.
- Do not convey information by color alone. Always pair color with a secondary indicator: an icon, label, pattern, or text.
- Ensure touch and click targets are at least 44×44 pixels for primary interactive elements.
- Use underlines only for links, not for decorative or non-link text.
- Differentiate visited and unvisited link states visually.
- Provide a "skip to main content" skip link at the start of each page so keyboard users can bypass repeated navigation.
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

## 6. Content governance

These rules describe how this style guide itself is maintained and updated.

- **Ownership:** The project maintainer is responsible for keeping these standards
  current. Contributors may propose changes via pull request.
- **Versioning:** Changes to standards that affect existing content should be noted
  in commit messages and, for significant changes, in a changelog comment in this file.
- **Conflict resolution:** When two rules conflict, the more specific rule takes
  precedence. When this file conflicts with ACCESSIBILITY.md, ACCESSIBILITY.md wins.
- **Review cycle:** Standards should be reviewed against current practice at least
  once per year or when a major tool or platform change occurs.
- **Deprecation:** Remove outdated rules rather than leaving contradictions. A rule
  that no longer applies should be deleted, not commented out.

> **AI agents:** Do not silently override or quietly contradict rules in this file.
> If a requested change would conflict with an existing rule, surface the conflict
> and ask for clarification before proceeding.

---

## 7. References

- [Plain Language Guidelines — Digital.gov](https://www.plainlanguage.gov/guidelines/)
- [GOV.UK Content Design Guide](https://www.gov.uk/guidance/content-design/writing-for-gov-uk)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [Opquast Digital Quality Checklist](https://checklists.opquast.com/en/digital-quality/)
- [CivicActions Style Guide](https://civicactions-style-guide.readthedocs.io/en/latest/)
- [Brad Frost: Style Guides](https://bradfrost.com/blog/post/style-guides/)
- [Nielsen Norman Group: Design Systems vs. Style Guides](https://www.nngroup.com/articles/design-systems-vs-style-guides/)
- [Nielsen Norman Group: Ten Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)
- [Purdue OWL — Avoiding Plagiarism](https://owl.purdue.edu/owl/avoiding_plagiarism/guide_overview.html)
- [Brand pack templates](./templates/brand-packs/README.md)
- [ACCESSIBILITY.md](./ACCESSIBILITY.md)
- [SUSTAINABILITY.md](./SUSTAINABILITY.md)
- [AGENTS.md](./AGENTS.md)
