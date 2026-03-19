# Multi-brand starter profiles

Use these profiles when a project needs more than one reusable style system.
Each profile includes portable token, component, voice, and AI enforcement files.

## Profiles

- `civic-clarity/`: public-interest and service-delivery style with high readability defaults
- `developer-lab/`: technical product style optimized for developer workflows and dense information
- `ai-browser-test/`: warm parchment / deep forest palette, expressive serif + geometric sans typography, browser brand tokens, developer-audience voice — derived from [mgifford/ai-browser-test](https://github.com/mgifford/ai-browser-test)

## How to use

1. Pick one profile as your active brand baseline.
2. Copy that profile into your project as `brand-pack/`.
3. Declare the selected profile in `STYLES.md`.
4. Require agents to follow the selected profile in `AGENTS.md`.
5. Keep token names stable when adapting values for local brand identity.
