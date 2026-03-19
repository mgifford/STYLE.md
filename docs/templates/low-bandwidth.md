# STYLES.md — Low-bandwidth template

> Use this template for projects where environmental sustainability, data efficiency,
> or offline-capable delivery are primary constraints.
> Replace every `[PLACEHOLDER]`. Remove sections that do not apply.

---

## Scope

| Surface | Files | Applies? |
| :--- | :--- | :--- |
| **Repository documentation** | README, AGENTS.md, and all Markdown files | ✅ |
| **Published website** | `index.md`, `_layouts/`, `assets/` | ✅ with strict size budgets / ❌ |

---

## 1. Core philosophy

1. **Less is more.** Every kilobyte transferred has an energy cost.
2. **Resilience over richness.** Content must work without JavaScript, custom fonts, or high-bandwidth connections.
3. **Reuse before create.** Reuse existing infrastructure and cached assets before adding new ones.
4. **Measure impact.** Track page weight and transfer size as part of the definition of done.

---

## 2. Voice and tone

### Target reading level

- Aim for a **grade 6** reading level.
- Short sentences and active voice reduce cognitive load and page size.

### Plain language rules

| Avoid | Use instead |
| :--- | :--- |
| Utilize | Use |
| In order to | To |
| At this point in time | Now |
| [COMPLEX TERM] | [PLAIN TERM] |

### Grammar defaults

- **Voice:** Active.
- **Headings:** Sentence case.
- **Oxford comma:** Yes.
- **Spelling:** [American English / project lang].
- **Images:** Include only when they add information not expressible in text. Always provide alt text.

---

## 3. Design tokens (delete if docs-only)

Performance budget: **target < 50 KB total page weight** (HTML + CSS + fonts).

| Token | Value | Notes |
| :--- | :--- | :--- |
| `--bg` | `#ffffff` / `#0b0d10` | No images used as backgrounds |
| `--text` | `#121212` / `#f3f4f6` | System font stack; no external font loads |
| `--font-stack` | `system-ui, -apple-system, sans-serif` | No custom font files. System stack provides zero extra network cost. |

### Performance rules (site surface only)

- No JavaScript unless absolutely required for accessibility.
- No custom web fonts — use system font stacks.
- Compress all images. Use `<picture>` with WebP + JPEG fallback.
- Set `loading="lazy"` on all below-the-fold images.
- Target a Lighthouse Performance score of 95+.
- Honor `prefers-reduced-data` where browser support exists.

---

## 4. Accessibility constraints

- Heading levels must be sequential: `h1` → `h2` → `h3`. No skipping.
- All links must have descriptive text.
- All images require alt text. Decorative images use `alt=""`.
- Minimum color contrast: 4.5:1 for body text.
- Content must be usable without JavaScript.
- See [ACCESSIBILITY.md](../ACCESSIBILITY.md) for full commitment.

---

## 5. AI agent rules

- Read `AGENTS.md` before making any change.
- Default to the lowest-compute, highest-reuse approach.
- Never add external dependencies, CDN resources, or tracking scripts.
- Flag any change that increases total page weight by more than 5 KB.
- Never override accessibility or sustainability constraints.
- See [SUSTAINABILITY.md](../SUSTAINABILITY.md) for the compute efficiency ladder.

---

## 6. References

- [AGENTS.md](../AGENTS.md)
- [ACCESSIBILITY.md](../ACCESSIBILITY.md)
- [SUSTAINABILITY.md](../SUSTAINABILITY.md)
- [Sustainable Web Design — sustainablewebdesign.org](https://sustainablewebdesign.org/)
- [Web Sustainability Guidelines — W3C](https://www.w3.org/TR/2024/NOTE-sustyweb-20240709/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
