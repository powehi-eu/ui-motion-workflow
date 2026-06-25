# ui-motion-workflow

Open-source orchestrator for UI direction, motion integration, and browser validation.

## What It Is

`ui-motion-workflow` is an agent-facing workflow layer for building polished, motion-aware interfaces.

It orchestrates three responsibilities:

1. UI direction and motion intent
2. motion component selection and integration
3. browser-based validation of the real result

The project is agent-agnostic by design.

The reference implementation starts with Codex, but the workflow is designed to be portable to environments such as Claude Code, Cursor, and VS Code-based agent setups.

## Core Idea

The project does not try to replace:

- design intelligence systems
- component libraries
- browser automation or validation tools

Instead, it coordinates them.

Example orchestration flow:

1. establish the visual direction and motion intensity
2. choose a concrete implementation strategy
3. integrate the selected motion component into the host codebase
4. validate the result in a real browser
5. iterate until the motion feels intentional and coherent

## Reference Workflow

Current reference stack:

- `ui-ux-pro-max` for visual direction and motion tone
- `react-bits` for expressive animated React components and showcase effects
- `magicui` for production-friendly UI components with polished motion
- `motion-primitives` for lower-level motion patterns and composable animation building blocks
- browser validation for real output checks on localhost

This stack is a reference implementation, not a hard requirement.

## Provider Roles

Use providers by role, not just by popularity.

- `react-bits`
  Best for bold motion, ambient backgrounds, animated hero treatments, and visually expressive showcase pieces.
- `magicui`
  Best for polished UI components that feel closer to design-system-ready product surfaces.
- `motion-primitives`
  Best when the right answer is not a prebuilt block, but a clean motion pattern embedded into an existing local component.

In other words:

- `react-bits` = wow components
- `magicui` = product-friendly animated UI blocks
- `motion-primitives` = composable micro-motion patterns

## Principles

- Keep the core workflow generic and reusable
- Treat integrations as adapters, not as the product itself
- Prefer intentional motion over decorative noise
- Preserve host codebase conventions during integration
- Validate in the browser, not only in source

## Repository Structure

```text
ui-motion-workflow/
|-- docs/
|   |-- architecture.md
|   |-- codex-usage.md
|   |-- providers.md
|   `-- roadmap.md
|-- providers/
|   |-- README.md
|   |-- magicui.md
|   |-- motion-primitives.md
|   `-- react-bits.md
|-- plugins/
|   `-- ui-motion-workflow/
|       `-- .codex-plugin/plugin.json
|-- implementations/
|   |-- claude-code/
|   |   |-- CLAUDE.md
|   |   `-- README.md
|   |-- codex/
|   |   `-- README.md
|   |-- cursor/
|   |   |-- README.md
|   |   `-- ui-motion-workflow.mdc
|   `-- vscode/
|       |-- README.md
|       `-- copilot-instructions.md
|-- examples/
|   |-- existing-component-enhancement.md
|   |-- README.md
|   |-- dashboard-motion-polish.md
|   `-- marketing-hero-provider-selection.md
`-- LICENSE
```

## Implementation Adapters

Current adapter pack:

- `implementations/codex`
  Reference skill-first implementation for Codex, with an optional repo-scoped plugin artifact.
- `implementations/claude-code`
  Instruction pack for a `CLAUDE.md`-style orchestration workflow.
- `implementations/cursor`
  Cursor-oriented rule file and usage notes for chaining direction, provider choice, and validation.
- `implementations/vscode`
  VS Code-oriented workspace instructions for agent or chat-driven UI motion work.

The non-Codex adapters are intentionally lightweight and text-first. They preserve the workflow contract without pretending that every environment exposes the same plugin model.

## Where To Start

If you are exploring the repository for the first time:

- read `docs/architecture.md` for the workflow model
- read `docs/multi-agent-usage.md` for portability rules
- read `docs/providers.md` for provider positioning
- open `implementations/` for environment-specific adapters

If you want the Codex-first setup, start with:

- `docs/codex-usage.md`

## Initial Roadmap

1. document the generic workflow clearly
2. formalize the Codex reference implementation
3. support multiple motion/component providers in the reference stack
4. define adapter patterns for other agent environments
5. add practical examples
6. package optional distributions later if useful

## Before And After Example

Using `seryvon-website` as a concrete test bed, we can show the difference between:

- `before orchestrator`
  A version shaped mainly through UI direction alone.
- `after orchestrator`
  A version improved through the full workflow: direction review, provider choice, implementation, and browser validation.

Before:

![Seryvon before orchestrator hero](docs/seryvon-before-orchestrator-hero.png)

![Seryvon before orchestrator proof](docs/seryvon-before-orchestrator-proof.png)

![Seryvon before orchestrator compare](docs/seryvon-before-orchestrator-compare.png)

After:

![Seryvon after orchestrator hero](docs/seryvon-after-orchestrator-hero.png)

![Seryvon after orchestrator proof](docs/seryvon-after-orchestrator-proof.png)

![Seryvon after orchestrator compare](docs/seryvon-after-orchestrator-compare.png)

The result feels more orchestrated because the page now has a clearer narrative sequence instead of a set of polished but mostly parallel sections.

The hero now explicitly frames the product journey as Get found, Get cited, and Get chosen, which makes the five-pillar story easier to understand immediately. The audit panel also has clearer product signals with Crawl, Score, and Proof, so the visual proof feels connected to the product workflow rather than decorative.

Motion is more intentional: section reveals are staggered, bar fills progress in sequence, and hover states are restrained. The animation supports reading order instead of competing with the content.

The page rhythm is tighter too. The first viewport now hints at the proof metrics on desktop and mobile, CTAs are more legible, and the Pro / Team offer is visually prioritized without making the pricing section feel noisy. Overall, the page reads less like individual nice sections and more like one guided product argument.
## Public Roadmap

Short version:

- improve install guidance per environment
- add stronger real-world examples and screenshots
- refine browser-validation workflows
- keep the core orchestration portable while expanding adapters

See `docs/roadmap.md` for the fuller roadmap.

## Acknowledgements

`ui-motion-workflow` builds on an open-source ecosystem rather than replacing it.

Special thanks to the maintainers and contributors behind projects in the reference stack and surrounding workflow, including `ui-ux-pro-max`, `react-bits`, `magicui`, and `motion-primitives`.

For explicit attribution and reuse notes, see `docs/acknowledgements.md`.

## License

MIT

## Codex Installation

This repository includes a repo-scoped Codex plugin artifact:

```text
plugins/ui-motion-workflow/
```

and a repo-scoped marketplace file:

```text
.agents/plugins/marketplace.json
```

For a local checkout, the usual flow is:

1. add the repo marketplace root to Codex
2. install `ui-motion-workflow` from that marketplace

See [docs/codex-usage.md](docs/codex-usage.md) for the Codex-oriented workflow details.







