# Build and Test Discovery

Find commands from repository files instead of guessing.

## Sources

- `package.json` scripts.
- `Makefile`.
- `pyproject.toml`.
- `tox.ini`.
- `pytest.ini`.
- `pom.xml`.
- `build.gradle`.
- `.github/workflows/*`.
- README setup section.
- Docker compose files.

## Output

Create `COMMANDS.md` with:

- install command;
- dev command;
- test command;
- lint command;
- build command;
- typecheck command;
- known caveats.
