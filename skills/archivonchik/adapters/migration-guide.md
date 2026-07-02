# Adapter Migration Guide

## CLAUDE.md to AGENTS.md

Move general project rules into `AGENTS.md`. Keep Claude-specific startup behavior in `CLAUDE.md`.

## AGENTS.md to Copilot instructions

Keep only the short essentials: overview, commands, style, safety, tests.

## Tool rules to Archivonchik

Move durable project facts into `docs/ai-context/`.

## Golden rule

One fact should live in one primary place. Other files should point to it, not duplicate it.
