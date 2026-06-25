# Codex Usage

## Purpose

This document explains how to use `ui-motion-workflow` as a practical Codex-first implementation.

The goal is not to restate the full architecture. The goal is to show how a Codex agent should actually execute the workflow in day-to-day UI work.

## Recommended Codex Stack

Reference stack:

- `ui-motion-workflow` as the orchestrator
- `ui-ux-pro-max` for direction
- `react-bits`, `magicui`, or `motion-primitives` as providers
- browser validation on localhost

## Repo-Scoped Plugin Install

This repository includes a Codex plugin artifact at:

```text
plugins/ui-motion-workflow
```

and a repo-scoped marketplace at:

```text
.agents/plugins/marketplace.json
```

Typical local install flow:

1. add the marketplace root for this repository to Codex
2. install `ui-motion-workflow` from that marketplace

The exact marketplace name is defined in the marketplace file.

## Typical Prompt Shapes

Good prompts:

- `Use $ui-motion-workflow to improve the hero motion on this page and validate it in the browser.`
- `Use $ui-motion-workflow to choose the right provider for this dashboard and implement subtle motion polish.`
- `Use $ui-motion-workflow to enhance this existing card component without changing its layout.`

## Suggested Execution Loop

1. Read the target code or page
2. Decide whether direction is needed first
3. Route to the right provider
4. Implement in the host codebase
5. Validate on localhost
6. Iterate until the result is coherent

## Provider Bias in Codex

In Codex, a useful default bias is:

- `react-bits` for hero or marketing surfaces
- `magicui` for polished product-oriented component blocks
- `motion-primitives` for upgrading existing local components

## Browser Validation Pattern

When localhost is available, use browser checks as a required final step for motion-heavy changes.

Validation questions:

- Does the effect look better in motion than it did in source?
- Is it too strong for the surrounding UI?
- Does mobile or narrow width break the intended feel?
- Is readability preserved during motion?

## What This Should Produce

A good Codex run using this workflow should end with:

- a clear phase order
- an explicit provider decision
- an implementation aligned with local code conventions
- a browser-backed judgment rather than a source-only guess

## When To Skip Parts

Skip `ui-ux-pro-max` when the direction is already obvious.

Skip provider exploration when the exact provider is already mandated by the user.

Skip browser validation only when a live surface is unavailable, and call that out explicitly.
