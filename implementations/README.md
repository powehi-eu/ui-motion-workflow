# Implementations

## Purpose

This folder contains environment-specific adapters for `ui-motion-workflow`.

The workflow contract stays the same across adapters:

1. understand the target surface
2. decide whether direction is needed first
3. choose the right motion provider
4. implement with local conventions
5. validate in a real browser
6. iterate until the motion feels coherent

## Available Adapters

- `codex`
  Reference implementation with a native skill and optional repo-scoped plugin packaging.
- `claude-code`
  Text-first `CLAUDE.md` instruction pack.
- `cursor`
  Rule-based adaptation with a reusable Cursor rule file.
- `vscode`
  Workspace instruction pack for VS Code-based AI coding flows.

## Rule

Do not try to force the same packaging model across every environment.

Use native artifacts where possible, and keep the workflow itself stable.
