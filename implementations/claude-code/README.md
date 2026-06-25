# Claude Code Adapter

## Purpose

This folder provides a Claude Code-oriented adaptation of `ui-motion-workflow`.

Unlike the Codex variant, this adapter is intentionally text-first. The main artifact is a reusable `CLAUDE.md` instruction file that can be copied into a repository or merged into an existing Claude Code setup.

## Included Artifact

- `CLAUDE.md`
  A ready-to-adapt orchestration prompt that preserves the `ui-motion-workflow` phase model.

## Recommended Usage

Use this adapter when you want Claude Code to:

- decide whether design direction is needed first
- choose between `react-bits`, `magicui`, and `motion-primitives`
- implement motion with local codebase conventions
- validate on a real running surface when browser tooling is available

## Practical Note

Treat this as an instruction pack, not as a fake plugin.

Claude Code may evolve its preferred repo conventions over time, but the workflow contract in `CLAUDE.md` should stay stable even if the surrounding setup changes.
