# STYLES.md — Formal government template

> Use this template for public-sector, compliance-heavy, or high-trust environments
> where plain language standards and policy traceability are required.
> Replace every `[PLACEHOLDER]`. Remove sections that do not apply.

---

## Scope

| Surface | Files | Applies? |
| :--- | :--- | :--- |
| **Repository documentation** | README, AGENTS.md, and all Markdown files | ✅ |
| **Published website** | `index.md`, `_layouts/`, `assets/` | ✅ / ❌ |

---

## 1. Core philosophy

1. **Accessibility is non-negotiable.** Every resident must be able to use public content regardless of ability.
2. **Plain language is policy.** Write for the reading level of the broadest audience, not the subject-matter expert.
3. **Traceability over convenience.** Every decision must be attributable to a policy, standard, or documented rationale.
4. **Trust through transparency.** Acknowledge limitations and publish known gaps.

---

## 2. Voice and tone

### Target reading level

- Aim for a **grade 6** reading level for public-facing content.
- Aim for a **grade 8** reading level for technical documentation.
- Test with the Hemingway App or the Flesch-Kincaid index.

### Plain language rules

| Avoid | Use instead |
| :--- | :--- |
| Utilize | Use |
| Notwithstanding | Despite / even though |
| Prior to | Before |
| Subsequent to | After |
| In order to | To |
| Shall | Must (if mandatory) / Should (if recommended) |
| Request for proposals | Call for bids |

### Grammar defaults

- **Voice:** Active. "The agency issues the permit" — not "The permit is issued."
- **Headings:** Sentence case throughout.
- **Oxford comma:** Always.
- **Spelling:** Follow the official language policy for your jurisdiction. Default: American English.
- **Dates:** Write in full — "March 18, 2026" — not "03/18/26."
- **Numbers:** Spell out numbers one to nine; use numerals for 10 and above.

### Policy traceability

Where a rule derives from a specific policy or standard, cite the source inline:

```markdown
All public-facing pages must meet WCAG 2.2 AA. [Source: [POLICY NAME] §[SECTION]]
```

---

## 3. Design tokens (delete if docs-only)

| Token | Light value | Dark value | Notes |
| :--- | :--- | :--- | :--- |
| `--bg` | `#ffffff` | `#0b0d10` | Base background |
| `--text` | `#121212` | `#f3f4f6` | 4.5:1 contrast required |
| `--button` | `[PRIMARY BRAND COLOR]` | `[DARK VARIANT]` | Check contrast against white |
| `--font-stack` | `[OFFICIAL GOVERNMENT FONT], system-ui, sans-serif` | — | Use `rem`, never `px` |

---

## 4. Accessibility constraints

- Target: WCAG 2.2 AA minimum. AAA for high-risk content.
- All public-facing forms must be keyboard-accessible and screen-reader-tested.
- Heading levels must be sequential: `h1` → `h2` → `h3`. No skipping.
- All links must have descriptive text.
- All images require alt text. Decorative images use `alt=""`.
- Video content requires closed captions and a transcript.
- PDFs must be tagged and readable by assistive technology.
- See [ACCESSIBILITY.md](../ACCESSIBILITY.md) for full commitment and severity taxonomy.

---

## 5. AI agent rules

- Read `AGENTS.md` before making any change.
- Do not generate content that implies policy positions unless explicitly instructed.
- Cite sources when adding factual claims.
- Flag ambiguities — do not make assumptions about policy intent.
- Never override accessibility or sustainability constraints.
- Use the jurisdiction's official language standard unless overridden.

---

## 6. References

- [AGENTS.md](../AGENTS.md)
- [ACCESSIBILITY.md](../ACCESSIBILITY.md)
- [SUSTAINABILITY.md](../SUSTAINABILITY.md)
- [Plain Language Act (US)](https://www.plainlanguage.gov/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [GOV.UK Content Design Guide](https://www.gov.uk/guidance/content-design/writing-for-gov-uk)
- [[JURISDICTION POLICY REFERENCE]]
