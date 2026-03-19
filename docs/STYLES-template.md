# STYLES.md — [PROJECT NAME]

> A machine-readable style standard for human and AI collaboration.
> Copy this file to your project root. Replace every `[PLACEHOLDER]` with your real values.
> Remove sections that do not apply. Keep sections short and testable.

---

## Scope

<!-- Describe which surfaces this file governs. Delete the row that does not apply. -->

| Surface | Files | Applies? |
| :--- | :--- | :--- |
| **Repository documentation** | README, AGENTS.md, and other Markdown files | ✅ Always |
| **Published website** | `index.md`, `_layouts/`, `assets/` | ✅ If you have a site / ❌ Remove if docs-only |

---

## 1. Core philosophy

<!-- State 2–4 principles that drive all decisions in this project. Be specific. -->

1. **[PRINCIPLE 1]:** [One sentence explanation.]
2. **[PRINCIPLE 2]:** [One sentence explanation.]
3. **[PRINCIPLE 3]:** [One sentence explanation.]

---

## 2. Voice and tone

### Target reading level

- Aim for a **grade [X]** reading level (recommended: grade 6–8 for public-facing content).
- Test with [Hemingway App](https://hemingwayapp.com/) or equivalent.

### Plain language rules

| Avoid | Use instead |
| :--- | :--- |
| Utilize | Use |
| In order to | To |
| [BUREAUCRATIC TERM] | [PLAIN ALTERNATIVE] |

### Grammar defaults

- **Voice:** [Active / Passive — default: active]
- **Headings:** [Sentence case / Title Case — default: sentence case]
- **Oxford comma:** [Yes / No — default: yes]
- **Spelling:** [American English / British English / Canadian English]

---

## 3. Design tokens (delete if docs-only)

<!-- Only needed if you have a published website. -->

| Token | Light value | Dark value | Notes |
| :--- | :--- | :--- | :--- |
| `--bg` | `[#FFFFFF]` | `[#0b0d10]` | Base background |
| `--text` | `[#121212]` | `[#f3f4f6]` | 4.5:1 contrast required |
| `--button` | `[#111111]` | `[#f3f4f6]` | Primary CTA fill |
| `--font-stack` | `[Inter, system-ui, sans-serif]` | — | Use `rem`, never `px` |

---

## 4. Accessibility constraints

<!-- Minimum requirements. For full details, see ACCESSIBILITY.md if present. -->

- Heading levels must be sequential: `h1` → `h2` → `h3`. No skipping.
- All links must have descriptive text ("Read the guide" — not "click here").
- All images require alt text. Decorative images use `alt=""`.
- Minimum color contrast: 4.5:1 for body text, 3:1 for large text and UI.
- [ADDITIONAL PROJECT-SPECIFIC REQUIREMENT]

---

## 5. AI agent rules

<!-- These rules apply to any AI coding agent working in this repository. -->

- Read `AGENTS.md` before making any change.
- Identify which surface is being edited and apply the correct section of this file.
- Never override accessibility or sustainability constraints.
- Keep changes scoped to the minimum needed to fulfill the request.
- Use [American English / project lang] unless explicitly overridden.
- [ADDITIONAL PROJECT-SPECIFIC RULE]

---

## 6. References

<!-- Add links to your pillar standards and any external references you follow. -->

- [AGENTS.md](./AGENTS.md)
- [ACCESSIBILITY.md](./ACCESSIBILITY.md) — or link to [mgifford/ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md)
- [SUSTAINABILITY.md](./SUSTAINABILITY.md) — or link to [mgifford/sustainability.md](https://github.com/mgifford/sustainability.md)
- [Plain Language Guidelines](https://www.plainlanguage.gov/guidelines/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
