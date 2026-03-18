# Copilot Instructions for STYLES.md

## Read This First
- Always read [AGENTS.md](../AGENTS.md) before making changes.
- Always read [ACCESSIBILITY.md](../ACCESSIBILITY.md) before making standards changes.
- Always read [SUSTAINABILITY.md](../SUSTAINABILITY.md) before making standards changes.

## Repository Summary
- Purpose: Define and publish a machine-readable style standard for humans and AI agents.
- Project type: Documentation-only repository (Markdown).
- Size and layout: Very small root-level docs with no source tree or package manifests.
- Languages/frameworks/runtimes: Markdown only. No build framework is configured.

## High-Level Layout
Root files currently present:
- [README.md](../README.md)
- [STYLES.md](../STYLES.md)
- [AGENTS.md](../AGENTS.md)
- [ACCESSIBILITY.md](../ACCESSIBILITY.md)
- [SUSTAINABILITY.md](../SUSTAINABILITY.md)

Key content:
- [README.md](../README.md): Project overview, three-pillar model, usage steps.
- [STYLES.md](../STYLES.md): Canonical standards text for reuse.
- [AGENTS.md](../AGENTS.md): Operational instructions for coding agents.
- [ACCESSIBILITY.md](../ACCESSIBILITY.md): Foundational accessibility commitments and guardrails.
- [SUSTAINABILITY.md](../SUSTAINABILITY.md): Environmental and efficiency constraints.

Current CI/pipeline config checked in:
- `.github/workflows/link-check.yml`
- `.github/workflows/plain-language.yml`
- `.github/workflows/accessibility-scan.yml`
- `.github/lychee.toml`
- `.github/pa11yci.json`

## Command Reality (Validated)
The following were executed in this repository:

Working commands:
- `ls -la`
- `find . -maxdepth 3 -type f | sort`
- `git status --short`
- `git diff --stat`
- `grep -RInE 'TODO|HACK|FIXME|WORKAROUND|XXX' . --exclude-dir=.git`
- `git clean -ndx` (dry-run only)

Failing commands (expected in current repo state):
- `npm install`
- `npm run build`
- `npm test`
- `npm run lint`
- `npm start`

Failure mode:
- All npm commands fail with `ENOENT` because `package.json` does not exist in repo root.
- Timed sample: `time npm install` failed in about `0.397s` (exit code `254`).

Observed side effect:
- Running `npm install` can create an unintended `package-lock.json` even when it fails.
- Workaround: remove the artifact with `rm -f package-lock.json`.

Tooling caveat observed in this environment:
- `rg` (ripgrep) is not installed (`bash: rg: command not found`).
- Use `find` and `grep` fallbacks instead of assuming `rg` is available.

## Recommended Execution Order
For any change, follow this sequence:
1. Read [AGENTS.md](../AGENTS.md), then [ACCESSIBILITY.md](../ACCESSIBILITY.md), then [SUSTAINABILITY.md](../SUSTAINABILITY.md), then [README.md](../README.md), then [STYLES.md](../STYLES.md).
2. Inspect current state: `git status --short`.
3. Make minimal Markdown edits scoped to the user request.
4. Validate references and formatting by re-reading modified files.
5. Run `git diff --stat` and `git diff`.
6. Re-run `git status --short` to confirm only intended files changed.

## Bootstrap/Build/Test/Run/Lint Guidance
Because this is docs-first:
- Bootstrap: no local install step is required for basic edits.
- Build: GitHub Actions builds the Jekyll site for accessibility checks.
- Test: CI includes link checking, plain-language checks, and accessibility scans.
- Lint: CI uses `write-good` and a banned-term pass for language quality.
- Run: no app runtime entrypoint exists outside static site preview.

## Pre-Check-In Checks Agents Should Replicate
Before finishing a task:
- Confirm changed files are expected: `git status --short`.
- Confirm diff size and scope: `git diff --stat` and `git diff`.
- Confirm no accidental artifacts (especially `package-lock.json`).
- Confirm instructions in [README.md](../README.md), [STYLES.md](../STYLES.md), [AGENTS.md](../AGENTS.md), [ACCESSIBILITY.md](../ACCESSIBILITY.md), and [SUSTAINABILITY.md](../SUSTAINABILITY.md) remain consistent.

## Architecture and Editing Guidance
- Treat this as a standards/spec repository, not an application codebase.
- Prefer additive, explicit language over broad rewrites.
- Keep terminology aligned with the three-pillar model and existing tone.
- Preserve portability: avoid tool-specific assumptions in standards text unless explicitly requested.

## Search Minimization Guidance
Trust this file and [AGENTS.md](../AGENTS.md) first.
Only perform broader repository searches if:
- The requested task references files not documented here.
- The documented command behavior changes.
- New build/test/lint/tooling files are introduced.
