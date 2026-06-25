# Codex Reference Implementation

This folder is reserved for the first concrete implementation of `ui-motion-workflow`.

The Codex implementation should act as the reference adapter for the generic workflow.

## Goals

- express the workflow in Codex-native primitives
- orchestrate specialized skills instead of duplicating them
- keep the core project agent-agnostic

## Expected Contents

Possible future contents:

- orchestrator skill
- optional plugin wrapper
- implementation notes for chaining browser validation

Current contents:

- `ui-motion-workflow/` skill orchestrator
- provider adapter notes can be aligned with the generic `providers/` folder in the repo
- repo-scoped plugin artifact under `../../plugins/ui-motion-workflow/`

Neighbor adapters in this repository:

- `../claude-code`
- `../cursor`
- `../vscode`

## Reference Stack

The initial Codex reference stack is expected to use:

- `ui-ux-pro-max`
- `react-bits`
- `magicui`
- `motion-primitives`
- browser validation tooling

Those are implementation choices, not part of the generic core contract.
