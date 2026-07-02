# Command Safety

Classify commands before running them.

## Safe

- Tests.
- Linters.
- Type checks.
- Local builds.
- Read-only inspection commands.

Examples:

```bash
pnpm test
pytest
mvn test
git status
```

## Caution

- Installing dependencies.
- Updating lockfiles.
- Running migrations.
- Starting Docker.
- Writing files outside the repo.

## Dangerous

- Deleting recursively.
- Piping remote scripts to shell.
- Printing environment variables.
- Committing secrets.
- Running unknown binaries.

Ask for confirmation before dangerous commands.
