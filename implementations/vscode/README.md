# VS Code Adapter

## Purpose

This folder provides a VS Code-oriented adaptation of `ui-motion-workflow`.

The main artifact is a workspace instruction file that can be reused in VS Code chat or agent-assisted coding setups.

## Included Artifact

- `copilot-instructions.md`
  A reusable instruction file for motion-aware UI orchestration in editor-native chat workflows.

## Recommended Usage

Use this adapter when you want VS Code-based AI assistance to:

- reason about direction before implementation when needed
- choose the right provider for the surface
- preserve local code conventions
- finish with browser-backed validation rather than source-only confidence

## Practical Note

This adapter is intentionally generic to VS Code-based workflows. Teams can adapt it to their preferred extension stack without changing the workflow itself.
