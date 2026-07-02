# Context Linting

Context linting checks whether AI instructions are useful, current, and safe.

## Smells

- Context bloat.
- Repeated instructions.
- Conflicting rules.
- Outdated commands.
- Missing test command.
- Unsafe command.
- Secret leakage.
- Skill leakage: tool-specific instructions copied everywhere.
- Phantom paths: instructions mention files that no longer exist.

## Output

Produce a context health score and actionable fixes.
