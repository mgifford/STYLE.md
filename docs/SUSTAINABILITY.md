# Sustainability Commitment (SUSTAINABILITY.md)

## 1. Scope and Commitment
This repository treats sustainability as a quality requirement for standards design, writing, and operational process.

Current commitment for this docs-first project:
- Reduce avoidable digital waste in content and workflow choices.
- Prefer lightweight, durable documentation over complex tooling.
- Use deterministic automation before AI-assisted generation where possible.
- Make sustainability tradeoffs explicit in major documentation decisions.

## 2. Relationship to Other Pillars (Overlap Management)
This file is the sustainability baseline. To reduce duplication:
- [ACCESSIBILITY.md](./ACCESSIBILITY.md) defines accessibility commitments and guardrails.
- [AGENTS.md](./AGENTS.md) defines operational behavior for coding agents.
- [STYLES.md](./STYLES.md) defines writing and design standards.
- [SUSTAINABILITY.md](./SUSTAINABILITY.md) defines environmental and compute-efficiency constraints.

When guidance overlaps, use this precedence:
1. Explicit user instructions.
2. ACCESSIBILITY.md for inclusion and usability requirements.
3. SUSTAINABILITY.md for efficiency and environmental constraints.
4. AGENTS.md for agent workflow behavior.
5. STYLES.md for style and design conventions.

## 3. Practical Adoption Options
Teams adopting this repository can choose one of these modes:

### Option A: Minimal (fastest)
- Keep this SUSTAINABILITY.md in repo root.
- Reference it from README and AGENTS instructions.
- Use manual review to avoid unnecessary process and tooling overhead.

### Option B: Balanced (recommended)
- Option A, plus:
- Track sustainability-related issues with a dedicated `sustainability` label.
- Require a short sustainability impact note in pull requests for major changes.
- Record known sustainability constraints and review dates.

### Option C: Strict (highest rigor)
- Option B, plus:
- Add automated checks for docs size growth, link hygiene, and workflow efficiency.
- Define release-blocking criteria for major sustainability regressions.
- Maintain living sustainability metrics with owners and review cadence.

## 4. Contributor Requirements (Guardrails)
All contributions should:
- Prefer simpler, lower-overhead approaches when outcomes are equivalent.
- Avoid introducing tooling that increases maintenance or compute cost without clear value.
- Keep changes scoped and incremental to reduce rework and automation churn.
- Document meaningful tradeoffs when choosing heavier processes.

For larger changes, contributors should also:
- State expected sustainability impact (`improves`, `neutral`, or `regresses`).
- Note whether AI assistance was necessary and why.

## 5. AI Usage and Compute Policy
Default stance:
- Prefer non-AI and deterministic methods first.
- Use AI when it clearly reduces overall lifecycle effort and rework.
- Keep prompts focused and avoid repeated broad-context runs.

Operational requirements:
- Do not run expensive checks when inputs are unchanged.
- Avoid always-on heavy workflows for documentation-only updates.
- Cache reusable outputs where practical.
- Disclose meaningful AI assistance in pull requests.

## 6. Validation Approach
Current repository state is documentation-only with no dedicated sustainability CI pipeline.

Validated checks currently available:
- Manual review for unnecessary complexity or process overhead.
- Repository consistency checks across README, STYLE, AGENTS, ACCESSIBILITY, and SUSTAINABILITY files.
- Git diff inspection before merge.

If automation is added later, document exact commands, thresholds, and failure criteria here.

## 7. Known Limitations
Current limitations:
- No formal sustainability metrics baseline has been established.
- No automated CI guardrails currently measure sustainability outcomes.
- Tradeoff tracking is manual and depends on contributor discipline.

## 8. Continuous Improvement
This file is living documentation and should evolve as repository practices mature.

Planned improvement path:
- Add baseline metrics for documentation size and workflow efficiency.
- Add scoped automation with path filtering to minimize unnecessary compute.
- Add periodic review cadence for sustainability debt and remediation.

Last updated: 2026-03-18
