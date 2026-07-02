# Context Engineering

Context engineering is the practice of giving an AI agent the right project information at the right time.

## Good context

- Specific to this repository.
- Short enough to read quickly.
- Updated when commands or architecture change.
- Separates durable facts from temporary session notes.
- Avoids duplicated rules.

## Bad context

- Long generic advice.
- Contradictory instructions.
- Outdated commands.
- Hidden secrets.
- Full logs.
- Random conversation summaries.

## Archivonchik approach

Use layered context:

1. `AGENTS.md` for general agent instructions.
2. `CLAUDE.md` for Claude-specific startup behavior.
3. `docs/ai-context/*` for durable project memory.
4. Session memory only for recent continuity.
