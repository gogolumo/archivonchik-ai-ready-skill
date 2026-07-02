# Context Lint Sample Report

Score:

```text
82/100
```

Issues:

| Severity | File | Problem | Fix |
|---|---|---|---|
| High | `CLAUDE.md` | Says use npm, but repo has `pnpm-lock.yaml`. | Use pnpm. |
| Medium | `AGENTS.md` | Repeats testing rules. | Keep one testing section. |
| High | `COMMANDS.md` | Contains `curl | bash`. | Mark dangerous and ask confirmation. |
