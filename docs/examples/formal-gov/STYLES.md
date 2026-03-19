---
title: Formal government example — STYLES.md
---

# STYLES.md — City of Riverside Open Data Portal

> This is a worked example of STYLES.md for a public-sector open data platform.
> It shows what a complete, filled-in style file looks like for a compliance-heavy context.

---

## Scope

| Surface | Files | Applies? |
| :--- | :--- | :--- |
| **Repository documentation** | README, AGENTS.md, CONTRIBUTING.md, and all Markdown files | ✅ |
| **Published website** | `index.md`, `_layouts/`, `assets/` | ✅ |

---

## 1. Core philosophy

1. **Accessibility is non-negotiable.** Every resident must be able to use public data tools regardless of ability. Follows WCAG 2.2 AA minimum; AAA for high-risk flows.
2. **Plain language is policy.** Target grade 6 reading level for public-facing content per the City's Plain Language Ordinance §4.12.
3. **Traceability over convenience.** Each rule cites the policy it derives from.
4. **Trust through transparency.** Known gaps are published and tracked in the issue queue.

---

## 2. Voice and tone

### Target reading level

- Public-facing content: **grade 6** (Flesch-Kincaid). Tested on each release.
- Internal/technical documentation: **grade 8**.

### Plain language rules

| Avoid | Use instead |
| :--- | :--- |
| Utilize | Use |
| Notwithstanding | Despite / even though |
| Prior to | Before |
| Subsequent to | After |
| Shall | Must (mandatory) / Should (recommended) |
| Fiscal year | Budget year |
| Remit payment | Pay |

### Grammar defaults

- **Voice:** Active. "The portal shows the data" — not "The data is shown by the portal."
- **Headings:** Sentence case throughout.
- **Oxford comma:** Always.
- **Spelling:** American English (follows City communications style guide v2.3).
- **Dates:** Full format — "March 18, 2026." Never "03/18/26."
- **Numbers:** Spell out one to nine; numerals for 10 and above.
- **Acronyms:** Spell out on first use followed by acronym in parentheses: "Americans with Disabilities Act (ADA)."

---

## 3. Design tokens

| Token | Light value | Dark value | Notes |
| :--- | :--- | :--- | :--- |
| `--bg` | `#ffffff` | `#0b0d10` | Base background |
| `--text` | `#121212` | `#f3f4f6` | 4.5:1 contrast on `--bg` — verified |
| `--muted` | `#4b5563` | `#c5cad3` | 3:1 minimum on `--bg` |
| `--button` | `#00529b` | `#90caf9` | City brand blue — contrast verified |
| `--button-text` | `#ffffff` | `#000000` | — |
| `--font-stack` | `Source Sans Pro, system-ui, sans-serif` | — | City approved. `rem` only. |

---

## 4. Accessibility constraints

- Target: WCAG 2.2 AA throughout. AAA for forms and search.
- All public-facing forms: keyboard-accessible, screen-reader tested with JAWS and NVDA before release.
- Heading levels sequential: `h1` → `h2` → `h3`. No skipping. [Source: WCAG 2.2 §1.3.1]
- All links have descriptive text. [Source: WCAG 2.2 §2.4.6]
- All images require alt text. Decorative: `alt=""`. [Source: WCAG 2.2 §1.1.1]
- Video content: closed captions and downloadable transcript.
- PDFs: tagged, linearized, and readable by assistive technology.
- See [ACCESSIBILITY.md](../../ACCESSIBILITY.md) for severity taxonomy and issue reporting.

---

## 5. AI agent rules

- Read `AGENTS.md` before making any change.
- Do not generate content that implies a policy position unless explicitly instructed.
- Cite the source standard when adding regulatory claims.
- Flag any ambiguity rather than making assumptions about policy intent.
- Never override accessibility or sustainability constraints.
- Use American English (City style guide v2.3).

---

## 6. References

- [AGENTS.md](../../AGENTS.md)
- [ACCESSIBILITY.md](../../ACCESSIBILITY.md)
- [SUSTAINABILITY.md](../../SUSTAINABILITY.md)
- City of Riverside Plain Language Ordinance §4.12
- City Communications Style Guide v2.3 (internal)
- [Plain Language Act (US)](https://www.plainlanguage.gov/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
