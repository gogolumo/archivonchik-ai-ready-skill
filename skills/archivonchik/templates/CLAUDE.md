# CLAUDE.md

## Startup behavior

At the start of every session:

1. Read `docs/ai-context/CURRENT_STATE.md` if it exists.
2. Read `docs/ai-context/NEXT_STEPS.md` if it exists.
3. Read `docs/ai-context/DO_NOT_TOUCH.md` if it exists.
4. Read `docs/ai-context/session-memory/LAST_SESSION.md` if it exists.
5. Summarize the current project state before editing.

## Working rules

- Prefer minimal changes.
- Verify commands from project files before running them.
- Ask before destructive commands.
- Update project memory after durable decisions or meaningful changes.
