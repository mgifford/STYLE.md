## 7. Brand portability kit

This project uses a portable brand kit to keep consistency across repositories.

### 7.1 Token compatibility

- Reuse token names (`--bg`, `--text`, `--muted`, `--line`, `--card`, `--button`) across all derived projects.
- Derived projects may change token values but should not rename token keys.

### 7.2 Component compatibility

- Reuse stable component contracts for hero, notice, cards, and prose blocks.
- Document any new reusable component in `brand-pack/components.md` with required classes and usage rules.

### 7.3 Agent enforcement

- `AGENTS.md` must explicitly require adherence to brand tokens and component contracts.
- AI-generated UI changes must prefer existing components before adding new ones.
