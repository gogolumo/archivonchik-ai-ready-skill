# Build Doctor Sample Report

| Area | Score | Notes |
|---|---:|---|
| Architecture | 7/10 | Clear source layout, service boundaries not documented. |
| Testing | 4/10 | Tests exist, command is not documented. |
| Security | 6/10 | No secrets found, deploy script risk undocumented. |
| AI-readiness | 3/10 | No AGENTS.md, CLAUDE.md, or project memory. |
| Docs | 5/10 | README lacks setup details. |
| Release readiness | 4/10 | No release checklist or rollback notes. |

Top fixes:

1. Add `AGENTS.md`.
2. Add `CLAUDE.md`.
3. Document commands.
4. Mark deploy script as caution.
5. Add session memory files.
