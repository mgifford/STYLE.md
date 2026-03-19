---
title: Low-bandwidth example — STYLES.md
---

# STYLES.md — Field Health Records System

> This is a worked example of STYLES.md for a public health data collection tool
> designed for use in low-connectivity field environments.
> It shows what a complete, filled-in style file looks like for a sustainability-first project.

---

## Scope

| Surface | Files | Applies? |
| :--- | :--- | :--- |
| **Repository documentation** | README, AGENTS.md, CONTRIBUTING.md, and all Markdown files | ✅ |
| **Published web app** | All HTML templates, CSS, and static assets | ✅ with strict performance budgets |

---

## 1. Core philosophy

1. **Less is more.** Every kilobyte transferred has an energy cost and a connectivity cost.
2. **Resilience over richness.** Every feature must work without JavaScript, on a 2G connection, and on a four-year-old Android device.
3. **Reuse before create.** Reuse cached system resources before loading anything new.
4. **Measure impact.** Page weight and transfer size are tracked as part of every release.

---

## 2. Voice and tone

### Target reading level

- **grade 5** maximum for field-facing content (used by non-specialized health workers).
- **grade 8** for internal technical documentation.
- Short sentences. Active voice. No jargon.

### Plain language rules

| Avoid | Use instead |
| :--- | :--- |
| Utilize | Use |
| Administer | Give |
| Patient presents with | Patient has |
| Contraindicated | Do not use if… |
| Febrile | Has a fever |
| At this point in time | Now |

### Grammar defaults

- **Voice:** Active. "Record the patient's temperature" — not "The temperature should be recorded."
- **Headings:** Sentence case.
- **Oxford comma:** Yes.
- **Spelling:** American English (project default). Update `lang` in config for regional deployments.
- **Units:** Always include the unit. "38.5°C" — not "38.5."
- **Numbers:** Use numerals for all measurements and quantities. Spell out zero to nine in prose.

---

## 3. Design tokens (web app)

Performance budget: **< 30 KB total initial page weight** (HTML + CSS). Zero external requests on first load.

| Token | Light value | Dark value | Notes |
| :--- | :--- | :--- | :--- |
| `--bg` | `#ffffff` | `#0b0d10` | No background images |
| `--text` | `#121212` | `#f3f4f6` | 7:1 for field readability in bright sunlight |
| `--button` | `#1a6e3c` | `#2ea043` | Confirmed 4.5:1 on white |
| `--font-stack` | `system-ui, -apple-system, sans-serif` | — | No custom font files. Zero extra requests. |

### Performance rules

- No JavaScript unless required for a core accessibility feature.
- No custom web fonts. System font stack only.
- All images: compressed WebP + JPEG fallback, `loading="lazy"`, explicit `width` and `height`.
- Service worker required: app must function offline after first load.
- Target Lighthouse Performance: 95+ on simulated 3G.
- Target page weight after initial load: < 30 KB HTML + CSS; < 100 KB with all images.

---

## 4. Accessibility constraints

- Target: WCAG 2.2 AA throughout. AAA for critical health data entry forms.
- All forms: keyboard-accessible, tested with TalkBack (Android) and VoiceOver (iOS).
- Heading levels sequential: `h1` → `h2` → `h3`. No skipping.
- All links have descriptive text.
- All images require alt text. Decorative: `alt=""`.
- Touch targets: minimum 44×44 px — larger preferred for field use with gloves.
- Content must function without JavaScript.
- See [ACCESSIBILITY.md](../../ACCESSIBILITY.md) for severity taxonomy.

---

## 5. AI agent rules

- Read `AGENTS.md` before making any change.
- Default to the lowest-compute, highest-reuse approach.
- Never add external CDN resources, tracking scripts, or analytics.
- Flag any change that increases initial page weight by more than 2 KB.
- Never override accessibility or sustainability constraints.
- See [SUSTAINABILITY.md](../../SUSTAINABILITY.md) for the compute efficiency ladder.

---

## 6. References

- [AGENTS.md](../../AGENTS.md)
- [ACCESSIBILITY.md](../../ACCESSIBILITY.md)
- [SUSTAINABILITY.md](../../SUSTAINABILITY.md)
- [Sustainable Web Design — sustainablewebdesign.org](https://sustainablewebdesign.org/)
- [Web Sustainability Guidelines — W3C WSG](https://www.w3.org/TR/2024/NOTE-sustyweb-20240709/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [WHO Plain Language Toolkit](https://www.who.int/tools/plain-language-toolkit)
