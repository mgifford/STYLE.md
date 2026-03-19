# Component contracts — ai-browser-test brand pack

These contracts define required structure, class names, and rules for each
reusable component. Follow them before introducing new markup.

---

## Page shell

- **Layout:** Single-column mobile base. Content constrained to `var(--shell-width)` = `min(1120px, calc(100% - 2rem))`.
- **Breakpoints (mobile-first):**
  - Default (< 640px): single-column; full-width controls and CTAs.
  - Medium (≤ 920px): two-column grid collapses to one column.
  - Wide (> 920px): full multi-column grid.
- **Required elements:** `<main>`, `<footer>` with sustainability disclosure visible on every HTML page.

---

## Capability matrix

The central interactive component showing browser AI API availability.

- **Required elements:** `<table>` with `<th scope="col">` or `<th scope="row">` on every header cell.
- **Status cells:** Must use text labels (e.g., "Available", "Not detected") alongside color coding. Color must never be the sole indicator.
- **Overflow:** Matrix scrolls horizontally at narrow widths; do not truncate column headers.
- **Live updates:** Inject probe results into an `aria-live` region so screen-reader users receive the same updates as sighted users.

---

## Card / panel

- **Background:** `var(--card)`.
- **Border radius:** `var(--radius-md)` (14px).
- **Elevation:** `var(--shadow)`.
- **Rules:**
  - Each card must have one heading (h2 or h3 depending on page hierarchy).
  - Do not place interactive controls inside a card title.

---

## Status chip

A small inline badge indicating API or feature state.

- **Required attributes:** Must carry a visible text label; icon-only chips require `aria-label`.
- **Color:** Use `--accent`, `--accent-2`, or `--accent-3` with sufficient contrast on the card background.
- **Rules:** Do not use browser brand tokens (`--chrome`, `--firefox`, `--edge`) for chips unless the chip refers specifically to that browser.

---

## CTA button

- **Primary:** Background `var(--accent)`, text white, radius `var(--radius-sm)`.
- **Secondary:** Border `var(--line)`, transparent background.
- **Minimum touch target:** 44×44 CSS pixels on mobile viewports.
- **Required:** Visible focus ring (3:1 contrast against adjacent color). Never suppress with `outline: none` without a replacement style.

---

## Notice / status banner

- **Use for:** Transparent status messages about completeness, experimental state, or data freshness.
- **Rules:** State the fact plainly. Do not soften negative results. If the notice has a date implication, include the version, channel, or ISO date.

---

## Accessibility requirements (all components)

- Use semantic HTML (`<button>`, `<nav>`, `<main>`, `<section>`, `<table>`) rather than `<div role="...">` wherever the native element is available.
- Every interactive control must have an accessible name — visible label text or `aria-label`.
- Focus styles must not be suppressed. The focus ring must meet 3:1 contrast against adjacent colors.
- Minimum touch target: 44×44 CSS pixels on mobile.
- `prefers-reduced-motion`: disable or shorten transitions and animations; do not remove content or controls.
