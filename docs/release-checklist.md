# Release Checklist

## Purpose

Use this checklist before publishing a tagged release of `ui-motion-workflow`.

## Checklist

1. Confirm the repository still reflects the portable workflow contract in `docs/architecture.md`.
2. Confirm adapter documentation exists for every environment advertised in `README.md`.
3. Confirm provider positioning is still coherent across `docs/providers.md` and `providers/`.
4. Confirm the Codex implementation paths are still valid:
   - `implementations/codex/`
   - `plugins/ui-motion-workflow/`
   - `.agents/plugins/marketplace.json`
5. Confirm new adapters do not claim unsupported plugin or packaging behavior.
6. Confirm examples still map cleanly to the documented provider roles.
7. Review `README.md`, `INSTALL.md`, and `CONTRIBUTING.md` for onboarding clarity.
8. Create or update the release notes summary.

## Suggested First Release Scope

A sensible `v0.1.0` for this repository is:

- generic workflow documented
- Codex reference implementation present
- Claude Code, Cursor, and VS Code adapters documented
- core provider positioning documented
- practical examples included

## Non-Goals For Early Releases

Avoid blocking early releases on:

- universal plugin packaging across all runtimes
- exhaustive examples for every UI pattern
- deep automation before the workflow contract is stable
