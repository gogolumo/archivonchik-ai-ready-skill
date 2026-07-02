---
name: archivonchik
description: Use this skill when making any codebase AI-ready for Claude Code or other coding agents. Helps analyze repositories, create AGENTS.md and CLAUDE.md, build project memory, continue work across sessions, lint AI context, discover build/test commands, classify command safety, run Build Doctor, prepare PR summaries, and create safe workflows for features, bug fixes, refactors, reviews, tests, documentation, releases, and onboarding.
---

# Archivonchik

Archivonchik turns a repository into an AI-ready project.

Use this skill when the user asks to:

- make a repository AI-ready;
- create or improve `AGENTS.md`, `CLAUDE.md`, or Copilot instructions;
- continue from previous work;
- preserve project memory across Claude Code sessions;
- run Build Doctor;
- lint project context;
- discover build/test/lint commands;
- classify a command as safe/caution/dangerous;
- review a change;
- generate tests;
- prepare a PR summary;
- onboard a developer or coding agent.

## Core loop

Always work through:

```text
Understand → Plan → Change → Verify → Remember
```

## Required startup behavior

When Archivonchik is invoked inside a repository:

1. Inspect the project structure before editing.
2. Identify the stack and package manager if possible.
3. Look for existing context files:
   - `AGENTS.md`
   - `CLAUDE.md`
   - `.github/copilot-instructions.md`
   - `docs/ai-context/*`
4. Read project memory if present:
   - `CURRENT_STATE.md`
   - `NEXT_STEPS.md`
   - `DECISIONS.md`
   - `KNOWN_BUGS.md`
   - `DO_NOT_TOUCH.md`
   - `session-memory/LAST_SESSION.md`
5. Choose the correct playbook.
6. Avoid creating huge or duplicated instruction files.

## Routing

Use these files as needed:

- Repository analysis: `reference/REPOSITORY_ANALYSIS.md`, `playbooks/repository-intake.md`
- Project memory: `reference/PROJECT_MEMORY.md`, `playbooks/update-project-memory.md`
- Session continuity: `reference/SESSION_CONTINUITY.md`, `playbooks/session-start.md`, `playbooks/session-end.md`
- Context compiler: `reference/CONTEXT_ENGINEERING.md`, `reference/AGENTS_MD.md`, `reference/CLAUDE_MD.md`, `reference/COPILOT_INSTRUCTIONS.md`
- Context linting: `reference/CONTEXT_LINTING.md`, `playbooks/context-lint.md`
- Command safety: `reference/COMMAND_SAFETY.md`, `playbooks/command-safety-review.md`
- Build/test discovery: `reference/BUILD_TEST_DISCOVERY.md`
- Build Doctor: `playbooks/build-doctor.md`
- Task workflows: `playbooks/feature-workflow.md`, `playbooks/bugfix-workflow.md`, `playbooks/refactor-workflow.md`, `playbooks/code-review-workflow.md`
- Stack-specific behavior: `profiles/*`
- Output templates: `templates/*`
- Other agent adapters: `adapters/*`
- Common usage recipes: `recipes/*`
- Showcase examples and sample reports: `showcase/*`

## Strong rules

- Do not store secrets, API keys, tokens, passwords, private keys, or personal data in project memory.
- Do not save entire chat transcripts.
- Do not create bloated context files.
- Do not run dangerous commands without explaining risk and asking for confirmation.
- Do not assume commands are correct; verify from project files.
- Do not edit high-risk files listed in `DO_NOT_TOUCH.md` without confirmation.
- Prefer minimal, project-specific instructions over generic advice.
- After meaningful work, update project memory only with durable facts.
