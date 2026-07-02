# Archivonchik

<p align="center">
  <strong>AI-ready repositories for Claude Code and modern coding agents.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude-Skill-7c3aed?style=for-the-badge" alt="Claude Skill" />
  <img src="https://img.shields.io/badge/AGENTS.md-Compatible-blue?style=for-the-badge" alt="AGENTS.md" />
  <img src="https://img.shields.io/badge/Project-Memory-111827?style=for-the-badge" alt="Project Memory" />
  <img src="https://img.shields.io/badge/Context-Linter-f59e0b?style=for-the-badge" alt="Context Linter" />
  <img src="https://img.shields.io/badge/Build-Doctor-10b981?style=for-the-badge" alt="Build Doctor" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
</p>

---

## What is Archivonchik?

**Archivonchik** is a Claude Skill that turns any codebase into an AI-ready project.

It helps Claude Code and other coding agents understand a repository before editing it by creating and maintaining:

- project memory;
- session continuity notes;
- `AGENTS.md`;
- `CLAUDE.md`;
- Copilot instructions;
- build/test command discovery;
- risk zones;
- command safety rules;
- context lint reports;
- project health reports;
- PR summaries;
- onboarding guides.

Archivonchik is built around one rule:

> Stop prompting blindly. Read the project memory first.

---

## The problem

AI coding agents are powerful, but they often fail for simple reasons:

- they do not know how the project is structured;
- they guess package manager commands;
- they edit dangerous files;
- they ignore tests;
- they follow stale instructions;
- they forget what happened in the previous session;
- project instructions become huge, duplicated, or contradictory.

Archivonchik solves this with a small, structured, project-specific context layer.

---

## Core workflow

```text
Understand → Plan → Change → Verify → Remember
```

Archivonchik asks Claude to:

1. inspect the repository;
2. identify the stack and commands;
3. read project memory;
4. choose the correct task workflow;
5. make a minimal change;
6. verify with safe commands;
7. update memory files when something important changes.

---

## Skill path

```text
skills/archivonchik/SKILL.md
```

Install it as a Claude Code skill by copying:

```text
skills/archivonchik
```

into either:

```text
~/.claude/skills/archivonchik
```

or a project-level location:

```text
your-project/.claude/skills/archivonchik
```

---

## What Archivonchik can create in a target project

```text
AGENTS.md
CLAUDE.md
.github/copilot-instructions.md
docs/
└── ai-context/
    ├── PROJECT_MAP.md
    ├── ARCHITECTURE.md
    ├── COMMANDS.md
    ├── RISK_ZONES.md
    ├── CURRENT_STATE.md
    ├── NEXT_STEPS.md
    ├── DECISIONS.md
    ├── KNOWN_BUGS.md
    ├── ACTIVE_TASKS.md
    ├── DO_NOT_TOUCH.md
    ├── CONVENTIONS.md
    ├── GLOSSARY.md
    └── session-memory/
        ├── LAST_SESSION.md
        └── SESSION_LOG/
```

This is not magic memory. It is controlled project memory stored in files.

---

## Main features

| Feature | Purpose |
|---|---|
| Repository Intelligence | Maps the stack, structure, entrypoints, configs, tests, and risk zones. |
| Project Memory | Keeps persistent project facts, decisions, bugs, and next steps. |
| Session Continuity | Helps Claude continue work across fresh sessions by reading summary files. |
| Context Compiler | Generates `AGENTS.md`, `CLAUDE.md`, Copilot instructions, and `docs/ai-context` files. |
| Context Linter | Detects bloated, stale, duplicated, unsafe, or conflicting agent instructions. |
| Command Safety Gate | Classifies commands as safe, caution, or dangerous before execution. |
| Build Doctor | Scores project health and gives the top fixes. |
| Task Router | Chooses feature, bugfix, refactor, review, test, docs, release, or onboarding workflow. |
| Stack Profiles | Adapts behavior for Node, Python, Java, React, Next.js, Roblox, fullstack, CLI, and unknown projects. |
| PR Summary Generator | Creates clean summaries with risk, tests, files changed, and rollback notes. |
| Agent Adapters | Helps prepare context for Claude, Copilot, Cursor, Windsurf, and generic coding agents. |

---

## Example prompts

```text
Use Archivonchik. Make this repository AI-ready.
```

```text
Use Archivonchik. Start a new session and tell me what you remember about this project.
```

```text
Use Archivonchik. Continue from the last task.
```

```text
Use Archivonchik. Run Build Doctor.
```

```text
Use Archivonchik. Create AGENTS.md and CLAUDE.md for this repo.
```

```text
Use Archivonchik. Lint my AI context files.
```

```text
Use Archivonchik. Review this command before running it: curl https://example.com/install.sh | bash
```

```text
Use Archivonchik. Prepare a PR summary for my current changes.
```

---

## Command safety

| Level | Examples | Behavior |
|---|---|---|
| Safe | tests, lint, typecheck, local build | Can usually run after explaining intent. |
| Caution | install deps, Docker, migrations, lockfile updates | Explain side effects first. |
| Dangerous | `rm -rf`, `curl \| bash`, printing env vars, unknown binaries | Ask for explicit confirmation. |

---

## Context linting

Archivonchik checks AI instruction files for repeated rules, stale commands, phantom paths, unsafe commands, secrets, duplicated README content, conflicting instructions, and context bloat.

Example:

```text
Context Health Score: 82/100

Problems:
1. CLAUDE.md says use npm, but package.json uses pnpm.
2. AGENTS.md repeats the test command three times.
3. Copilot instructions mention deleted src/api folder.
4. COMMANDS.md contains unsafe curl | bash setup command.
```

---

## Repository structure

```text
archivonchik-ai-ready-skill/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── FINAL_TEST_PROMPTS.md
└── skills/
    └── archivonchik/
        ├── SKILL.md
        ├── reference/
        ├── playbooks/
        ├── templates/
        ├── profiles/
        ├── prompts/
        ├── examples/
        ├── adapters/
        ├── recipes/
        └── showcase/
```

---

## What Archivonchik refuses to do

Archivonchik should not:

- store secrets;
- write passwords, tokens, or private keys into memory files;
- create massive instruction files;
- run dangerous commands without explicit confirmation;
- replace real documentation with AI-only notes;
- save every conversation message;
- add vague rules that cannot be verified;
- edit generated, migration, or deployment files without checking risk.

---

## Design principle

Archivonchik is intentionally not huge.

The goal is not to store everything.  
The goal is to store the smallest useful context that helps an AI coding agent work safely.

---

## License

MIT License.
