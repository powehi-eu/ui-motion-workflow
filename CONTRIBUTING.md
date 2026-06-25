# Contributing

## Purpose

Thank you for contributing to `ui-motion-workflow`.

This project is intended to stay:

- portable across agent environments
- focused on orchestration rather than library duplication
- practical for real UI implementation and browser validation work

## Contribution Priorities

High-value contributions usually improve one of these areas:

- workflow clarity
- provider selection guidance
- environment adapters
- browser validation patterns
- real examples with clear before-and-after reasoning

## Editorial Principles

Please keep contributions aligned with the project's public direction:

- keep the core workflow agent-agnostic
- avoid Powehi-specific business logic in the public core
- avoid turning the project into a component library
- prefer adapter-specific files over forcing one packaging model everywhere

## Adapter Philosophy

Not every environment should use the same artifact shape.

In this repository:

- Codex can use a native skill and optional plugin packaging
- Claude Code can use a `CLAUDE.md` instruction pack
- Cursor can use rule-based files
- VS Code can use workspace instruction files

Consistency should come from the workflow behavior, not from pretending all runtimes support the same install model.

## Contribution Process

1. Start from the workflow contract in `docs/architecture.md` and `docs/multi-agent-usage.md`.
2. Update the relevant adapter or provider documentation.
3. Keep examples concrete and implementation-oriented.
4. Prefer small, well-scoped pull requests.

## Good Changes

Examples of strong contributions:

- a better decision rule for choosing between `react-bits` and `magicui`
- a cleaner browser validation checklist
- a new example showing motion refinement on an existing component
- a clearer adapter guide for a specific agent environment

## License

By contributing to this repository, you agree that your contributions will be licensed under the MIT License.
