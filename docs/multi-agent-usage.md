# Multi-Agent Usage

## Purpose

This document explains how `ui-motion-workflow` maps to multiple agent environments without changing the underlying workflow contract.

## Shared Contract

Every adapter in this repository should preserve the same sequence:

1. read the target surface and understand the request
2. decide whether direction is needed first
3. choose the right motion provider
4. implement using host-project conventions
5. validate in a real browser when possible
6. iterate until the motion is coherent

## Adapter Strategy

The project supports multiple environments in different ways:

- Codex
  Native skill-first implementation plus optional repo-scoped plugin packaging.
- Claude Code
  Text-first orchestration via a `CLAUDE.md` instruction file.
- Cursor
  Rule-driven orchestration with a reusable Cursor rule file.
- VS Code
  Workspace instruction file for chat or agent-assisted coding flows.

## What Stays Constant

Across all adapters:

- `ui-ux-pro-max` is used when direction is unclear
- `react-bits` is favored for bold or showcase motion
- `magicui` is favored for polished product-like UI blocks
- `motion-primitives` is favored for embedded motion behaviors in existing components
- browser validation remains the final quality gate whenever the runtime can support it

## What Changes

What changes per environment is only the wrapping format:

- plugin or skill packaging
- rule or instruction file syntax
- how the agent is invoked
- how browser checks are connected to the local workflow

## Practical Rule

Do not force a fake universal plugin format.

Use the most natural artifact for each environment, while keeping the orchestration behavior consistent.
