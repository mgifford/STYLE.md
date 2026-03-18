---
title: Style guide discovery prompt
---

# Style guide discovery prompt

Use this prompt with an LLM to generate a `STYLES.md` for an existing project.
The prompt guides the LLM to audit the project first, then produce a filled-in
style file that connects to the STYLES.md family while staying true to what the
project already does.

Primary reference: [https://github.com/mgifford/STYLES.md](https://github.com/mgifford/STYLES.md).

---

## How to use this

1. Open a chat session with your LLM of choice.
2. Paste the prompt below, then attach or paste the relevant project files.
3. If you want to replicate the style of another project, attach that project's
   `STYLES.md` as a style seed and label it "source style reference."
4. Review the output. Push back on anything that does not match your real project.
5. Save the result as `STYLES.md` in your project root.
6. Add `AGENTS.md`, [ACCESSIBILITY.md](https://github.com/mgifford/ACCESSIBILITY.md),
   and [SUSTAINABILITY.md](https://github.com/mgifford/sustainability.md) as companion standards.

**Files to attach or paste (bring what you have):**
- `README.md`
- Any existing style guide, brand guide, or design tokens file
- A source `STYLES.md` from a project whose style you want to emulate (optional but strongly recommended)
- Source CSS or layout files from that reference project (optional, if available)
- A sample of your best-written documentation (1–3 files)
- `_config.yml` or equivalent site config, if you have one
- `package.json` or `pyproject.toml` — helps identify the tech stack
- Any existing `AGENTS.md` or LLM prompt files

---

## The prompt

```text
You are a style guide author helping me create a STYLES.md for an existing project.

STYLES.md is a machine-readable style standard in the STYLES.md open format. It is
read by both humans and AI coding agents. The output should be a complete,
filled-in Markdown file — not a template with placeholders.

## Your task

1. **Audit the project materials I am providing.**
   Read everything I attach. Identify:
   - The project's name, purpose, and primary audience
   - The writing patterns already in use (voice, tone, sentence structure, heading style)
   - Any design tokens already defined (colors, fonts, spacing)
   - The tech stack (does this project have a website surface, or is it docs-only?)
   - Any existing accessibility or sustainability commitments
   - Anything the project does well that should be preserved
   - Anything inconsistent that the STYLES.md should normalize

   If I provide a "source style reference" STYLES.md, also extract a
   **style fingerprint**:
   - Distinctive typography pairings and hierarchy behavior
   - Token strategy (core neutrals, accents, semantic tokens, radius/spacing)
   - Layout motifs (card density, section rhythm, prose width, CTA treatment)
   - Voice signature (how technical, how direct, how instructional)
   - Non-negotiables vs. adaptable choices

2. **Ask me three to five clarifying questions before writing.**
   Focus on gaps you cannot resolve from the files alone. For example:
   - Target reading level
   - Spelling convention (American / British / Canadian English)
   - Whether a GitHub Pages or equivalent site exists or is planned
   - Primary language for AI agent instructions
   - Any known brand or legal constraints
   - Should the output preserve the source style "as-is" or adapt it to this project's identity?
   - Which source style elements are non-negotiable (fonts, accent palette, tone, spacing rhythm)?

3. **Generate the STYLES.md.**
   Follow the structure below exactly. Fill in every section with specific,
   project-accurate values. Do not leave placeholders. Remove sections that
   do not apply.

4. **Generate a brand-pack bundle when a source style reference is provided.**
   Include a `brand-pack/` folder specification with:
   - `tokens.css`
   - `components.md`
   - `voice.md`
   - `ai-instructions.md`
   Mark each rule as either "Preserved from source" or "Adapted for project".

## Required structure

Use this section order:

---

# STYLES.md — [PROJECT NAME]

One-sentence description of what this file governs and who it is for.

---

## Scope: documentation files vs. the website

A table with two rows: GitHub Pages site and Repository documentation.
State clearly which surfaces exist for this project.
State which sections apply to which surface.

---

## 1. Core philosophy

Two to four principles specific to this project. Make them concrete, not generic.
Each principle should be falsifiable — something a reviewer could check.

---

## 2. Content and voice standards

### 2.1 Voice and tone
A table: context / tone / strategy. At least three rows.

### 2.2 Plain language and word choice
A substitution table. At least five rows drawn from actual patterns in the project.

### 2.3 Grammar and mechanics
Bullets covering: voice, headings, lists, Oxford comma, numbers, dates.

### 2.4 Spelling convention
State the variant. Explain how to override for derived projects.

---

## 3. Design foundations (site surface only)
Include this section only if the project has a website surface.

### 3.1 Design tokens
A table of CSS custom properties with light value, dark value, and requirement.
Derive these from existing brand assets if available; otherwise propose values
consistent with the STYLES.md family defaults.

If a source style reference is provided, include a short note after the table:
- "Preserved from source" tokens (carry over unchanged)
- "Adapted for project" tokens (changed deliberately with reason)

### 3.2 Typography
Font stack, scaling approach, line length, line height.

If a source style reference is provided, preserve the typography system's intent
(for example: expressive display + highly legible body) unless I explicitly ask
for a different direction.

### 3.3 Responsive design
Mobile-first breakpoints. At least three layers.

### 3.4 User-preference media queries
A table: query / status / implementation.

---

## 4. Accessibility and semantic logic

Apply to both surfaces. Draw from real gaps identified in the audit.
Reference [ACCESSIBILITY.md](./ACCESSIBILITY.md) for the full commitment.

---

## 5. AI agent instructions

Rules for coding agents working in this repository.
Cover: which file to read first, which surface they are editing, what they must
never override, language and spelling defaults, scope discipline.

---

## 6. References

Link to:
- STYLES.md (local or https://github.com/mgifford/STYLES.md)
- AGENTS.md
- ACCESSIBILITY.md (local or https://github.com/mgifford/ACCESSIBILITY.md)
- SUSTAINABILITY.md (local or https://github.com/mgifford/sustainability.md)
- Any style authorities the project already follows

---

## Design family constraints

This STYLES.md must be compatible with the STYLES.md open standard family:
- Use the same two-surface model (GitHub Pages site vs. repository documentation).
- Use the same section numbering (1–6) and heading conventions.
- Use sentence case for all headings.
- Use American English unless the project has a documented language policy.
- CSS tokens should use the same naming convention (--bg, --text, --muted, etc.)
  and the same single @media (prefers-color-scheme: dark) override pattern.
- The voice must be "authoritative peer": professional and precise, but accessible.

The project's unique character should come through in the content of each section,
not by changing the structure.

## What to avoid

- Do not copy this prompt or these instructions into the output file.
- Do not leave any [PLACEHOLDER] in the final output.
- Do not add sections that are not in the required structure.
- Do not assume a website surface exists unless the files confirm it.
- Do not invent brand colors or typography — ask me first if they are not in the
  files I have provided.
- Do not collapse to generic defaults (for example, "Inter + neutral grays") if
   a source style reference has stronger, distinctive choices.
- Do not output STYLES.md alone when I explicitly ask for portable style reuse;
   include the brand-pack bundle specification.

Begin by confirming you have read the attached files, then ask your clarifying
questions before generating anything.
```

---

## Tips for better results

**Be specific when answering clarifying questions.**
"Grade 8 reading level" is more useful than "readable." "American English" is
more useful than "standard English."

**Attach real writing samples, not just the README.**
The LLM will match patterns it can see. Attach docs, error messages, or UI copy
that represents the project's actual voice.

**If you want visual replication, attach a source style reference.**
Provide the reference `STYLES.md` and, if possible, its CSS/layout files.
Tell the LLM exactly what to preserve: typography pair, accent logic, spacing
rhythm, and tone.

**Push back if the tokens are invented.**
If the LLM proposes colors not in your brand, say so. Either provide the real
values or ask it to use the STYLES.md family defaults (`#ffffff` / `#0b0d10`,
`#121212` / `#f3f4f6`) as a neutral starting point.

**Run the output through a plain language checker.**
Paste the sections under "Content and voice standards" into
[Hemingway App](https://hemingwayapp.com/) to verify the reading level matches
what the prompt requested.

**Commit the result and reference it from AGENTS.md.**
A STYLES.md that is not wired into your agent instructions will be ignored.
Add a line to `AGENTS.md` such as:

```markdown
- Read [STYLES.md](./STYLES.md) before generating or editing any content.
```
