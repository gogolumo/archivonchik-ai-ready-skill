# Session Continuity

Archivonchik cannot create magical model memory. It creates file-based project memory that Claude can read at the start of future sessions.

## Session start

Read:

- `CURRENT_STATE.md`
- `NEXT_STEPS.md`
- `LAST_SESSION.md`
- `DECISIONS.md`
- `DO_NOT_TOUCH.md`

Then summarize what is known in 5 bullets.

## Session end

Write:

- What changed.
- Files touched.
- Tests run.
- Bugs found.
- Decisions made.
- Next steps.

Keep summaries short.
