# STYLES.md — Tech-minimal template

> Use this template for developer tools, internal documentation, and speed-focused
> engineering teams where precision and brevity matter more than formality.
> Replace every `[PLACEHOLDER]`. Remove sections that do not apply.

---

## Scope

| Surface | Files | Applies? |
| :--- | :--- | :--- |
| **Repository documentation** | README, AGENTS.md, and all Markdown files | ✅ |
| **Published website / docs site** | `index.md`, `_layouts/`, `assets/` | ✅ / ❌ |

---

## 1. Core philosophy

1. **Precision first.** Every word must earn its place.
2. **Consistency is the default.** Follow the pattern already in the repo.
3. **Docs are code.** Apply the same review standards you apply to source code.

---

## 2. Voice and tone

### Target reading level

- Assume the reader is a developer familiar with the domain.
- Avoid jargon from adjacent domains (legal, marketing, HR).

### Plain language rules

| Avoid | Use instead |
| :--- | :--- |
| Leverage | Use |
| Utilize | Use |
| Going forward | From now on |
| Best-in-class | [Specific claim with evidence] |

### Grammar defaults

- **Voice:** Active.
- **Headings:** Sentence case.
- **Oxford comma:** Yes.
- **Spelling:** American English.
- **Code references:** Wrap in backticks: `function`, `--flag`, `FILE.md`.
- **Commands:** Use code blocks. Show exact input and expected output.

---

## 3. Design tokens (delete if docs-only)

| Token | Value | Notes |
| :--- | :--- | :--- |
| `--bg` | `#ffffff` / `#0b0d10` | Light / dark |
| `--text` | `#121212` / `#f3f4f6` | 4.5:1 contrast required |
| `--code` | `#f3f4f6` / `#0c1016` | Code blocks and inline code |
| `--font-stack` | `ui-monospace, Menlo, Monaco, "Cascadia Code", monospace` | Monospace for code-heavy contexts |

---

## 4. Accessibility constraints

- Heading levels must be sequential: `h1` → `h2` → `h3`. No skipping.
- All links must have descriptive text.
- Code examples must have explanatory context — do not rely on code alone to convey meaning.
- Minimum color contrast: 4.5:1 for body text, 3:1 for large text.
- See [ACCESSIBILITY.md](../ACCESSIBILITY.md) for full commitment.

---

## 5. AI agent rules

- Read `AGENTS.md` before making any change.
- Prefer the simplest solution that satisfies the requirement.
- Never add boilerplate, placeholders, or filler text.
- Do not refactor code outside the scope of the request.
- Keep docs and code in sync — if you change behavior, update the docs.
- Never override accessibility or sustainability constraints.

---

## 6. References

- [AGENTS.md](../AGENTS.md)
- [ACCESSIBILITY.md](../ACCESSIBILITY.md)
- [SUSTAINABILITY.md](../SUSTAINABILITY.md)
- [Plain Language Guidelines — Digital.gov](https://www.plainlanguage.gov/guidelines/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
