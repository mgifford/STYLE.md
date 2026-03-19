# Voice and copy rules — ai-browser-test brand pack

## Audience

Web developers who understand browser APIs. Write for someone who is comfortable
reading MDN documentation. Do not over-explain technical terms.

## Voice by context

| Context | Tone | Strategy |
| :--- | :--- | :--- |
| UI labels, button text, status chips | Precise and neutral | Use the exact API or feature name; avoid marketing phrasing |
| Demo instructions and talk tracks | Direct and instructional | Use numbered steps and active verbs; address the reader in second person |
| Governance docs (ACCESSIBILITY.md, SUSTAINABILITY.md, AGENTS.md) | Authoritative and collegial | State commitments plainly; use bullet lists; avoid hedging |
| Error and probe result messages | Honest and informative | Report what was detected or what failed; do not soften a negative result with vague language |
| Code comments and agent instructions | Terse and imperative | One sentence per concern; no filler words |

## Word substitutions

| Avoid | Use instead | Reason |
| :--- | :--- | :--- |
| "leverage" | "use" | Clearer; consistent with existing docs |
| "utilize" | "use" | Simpler; matches the README register |
| "functionality" | "feature" or "behavior" | More specific; avoids bureaucratic tone |
| "Please note that…" | State the fact directly | Removes filler; aligns with direct voice |
| "built-in AI abilities" | "built-in AI APIs" or "built-in AI features" | Precise; matches Chrome developer docs naming |
| "currently" (without a date or version) | Specify the version, channel, or date | Prevents stale copy that misleads |
| Passive constructions ("is shown", "is rendered") | Active constructions ("the page shows", "the matrix renders") | Matches existing README style |

## Grammar and mechanics

- **Voice:** Prefer active voice. Use passive only when the actor is genuinely unknown or unimportant.
- **Headings:** Sentence case throughout. Capitalize only the first word and proper nouns. Do not use title case.
- **Lists:** Bullets for unordered items. Numbered lists for sequential steps. Do not mix in a single list.
- **Oxford comma:** Always. "Summarize, rewrite, and compare" — not "Summarize, rewrite and compare."
- **Numbers:** Spell out one through nine; use numerals for 10 and above. Always use numerals for measurements (350 KB, 8000, 640px).
- **Dates:** ISO 8601 for machine-readable dates (`2026-03-11`). "March 11, 2026" in prose.
- **Code and UI references:** Wrap code, file names, API names, and exact UI labels in backticks: `index.html`, `window.ai`.
- **Abbreviations:** Spell out on first use, then abbreviate: "carbon dioxide equivalent (CO2e)". Common technical abbreviations (API, HTML, CSS, JS, YAML) do not need expansion.

## Spelling

American English throughout. Examples: "color" not "colour"; "behavior" not "behaviour"; "summarize" not "summarise".
