# Cursor Adapter

Use this when preparing a repository for Cursor.

## Output target

```text
.cursor/rules/
```

## Include

- project overview;
- stack and package manager;
- build/test/lint commands;
- risk zones;
- security rules;
- testing expectations.

## Avoid

- copying the whole README;
- duplicating AGENTS.md;
- long logs;
- secrets;
- Claude-only startup instructions.

Cursor rules should point to `docs/ai-context/` instead of duplicating long context.
