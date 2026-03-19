# AI agent instructions — ai-browser-test brand pack

Agents working in a project that uses this brand pack must follow these rules in
addition to the project's own `AGENTS.md` and `STYLES.md`.

## Mandatory reading order

Before making any change:
1. Read `AGENTS.md`.
2. Read `STYLES.md` and note the selected brand profile.
3. Read the file you intend to edit.
4. If the change touches UI, read `brand-pack/components.md` and `brand-pack/tokens.css`.

## Surface identification

Determine whether you are editing:
- **Site surface** (`.html` files): apply token, component, typography, and layout rules.
- **Documentation surface** (`.md` files): apply voice, grammar, heading, and spelling rules only.

Do not apply CSS or token rules to documentation files.

## Token rules

- Never change the values of `--bg`, `--ink`, `--accent`, `--chrome`, `--firefox`, or `--edge`
  without an explicit instruction from the repository owner.
- Never add raw hex colors to markup or layout code. Use token references only.
- If a needed color role is missing, propose extending the token set and wait for approval.

## Typography rules

- Body font: `var(--font-body)` → `"Space Grotesk", "Segoe UI", sans-serif`.
- Display/heading font: `var(--font-display)` → `"Fraunces", Georgia, serif`.
- Both fonts must be loaded via Google Fonts with `<link rel="preconnect">` preconnect hints
  and `display=swap`. Do not load them via `@import`.
- Use `rem` for component-level font sizes. Use `clamp()` for fluid display headings.
  Never use `px` for text sizes.

## Accessibility rules

- Never remove `aria-live`, `aria-label`, `role`, `scope`, or visible focus styles,
  even if they appear redundant.
- Never use color as the sole means of conveying information. Status cells must
  carry text labels alongside color coding.
- Every `<table>` must include `<th scope="col">` or `<th scope="row">` headers.

## Documentation parity

If you add or change a probe, API test, or UI feature in an `.html` file, update
the corresponding `.md` documentation in the same change. Stale docs are a defect.

## Scope discipline

Make the smallest change that fully addresses the task. Do not:
- Reformat unrelated code.
- Reorder CSS declarations outside the scope of the task.
- Rename variables or tokens outside the scope of the task.
- Create `.html` versions of `.md` governance files.

## Commit messages

Use the imperative mood. Keep the subject line under 72 characters.
Examples: "Add aria-live region to probe results" — "Fix contrast on status chip in dark mode".

## Language and spelling

All generated text uses American English spelling (see `voice.md`).
Do not switch to British or Canadian spelling unless the project documents a different language policy.
