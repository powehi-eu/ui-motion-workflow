# Install

## Purpose

This document explains how to install the repo-scoped Codex plugin artifact shipped with this repository.

For Claude Code, Cursor, and VS Code variants, see the adapter files under `implementations/`.

## Repository Layout

The installable Codex pieces live here:

- plugin: `plugins/ui-motion-workflow`
- marketplace: `.agents/plugins/marketplace.json`

## Local Install Flow

From a local checkout of this repository:

1. Add the repository marketplace root to Codex.
2. Install `ui-motion-workflow` from that marketplace.
3. Start a new thread when testing updated skills or plugin contents.

## Marketplace Root

Use the repository root as the marketplace root because it contains:

- `.agents/plugins/marketplace.json`
- `plugins/ui-motion-workflow`

## Typical Commands

```bash
codex plugin marketplace add <path-to-ui-motion-workflow-repo>
codex plugin add ui-motion-workflow@personal
```

If the marketplace name changes later, read it from:

```text
.agents/plugins/marketplace.json
```

## Update Flow

When the plugin changes:

1. update the repo
2. reinstall the plugin from the configured marketplace
3. test from a new thread so Codex picks up updated skill contents

## Notes

- This repository uses a repo-scoped marketplace, not the default personal marketplace under the home directory.
- The Codex implementation is a reference adapter for the broader `ui-motion-workflow` project.
- The other adapters in this repository are instruction-first artifacts rather than Codex-style plugins.
