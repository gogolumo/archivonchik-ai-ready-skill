# Repository Analysis

Before making changes, identify the repository shape.

## Inspect

- Root files.
- Package manager files.
- Build configs.
- CI workflows.
- Source folders.
- Tests.
- Docs.
- Generated files.
- Deployment files.
- Environment examples.

## Detect stack

Look for:

- Node: `package.json`, `pnpm-lock.yaml`, `yarn.lock`, `package-lock.json`
- Python: `pyproject.toml`, `requirements.txt`, `poetry.lock`
- Java: `pom.xml`, `build.gradle`, `settings.gradle`
- React/Next.js: `src`, `pages`, `app`, `next.config.*`
- Roblox: `default.project.json`, `*.project.json`, `src/server`, `src/client`, `src/shared`
- CLI: `bin`, `cmd`, `src/main`, executable entrypoints

## Output

Create or update:

- `PROJECT_MAP.md`
- `ARCHITECTURE.md`
- `COMMANDS.md`
- `RISK_ZONES.md`
