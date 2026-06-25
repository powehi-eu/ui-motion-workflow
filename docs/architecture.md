# Architecture

## Positioning

`ui-motion-workflow` is a workflow orchestrator, not a component library and not a browser tool.

It sits above specialized systems and coordinates them.

## Layers

### 1. Core Workflow

The core workflow is portable and should stay independent from any single agent runtime.

Responsibilities:

- define the decision sequence
- define handoff boundaries between tools or skills
- define validation expectations

### 2. Integration Adapters

Adapters bind the workflow to a specific environment.

Examples:

- Codex skill or plugin implementation
- Claude Code instruction pack
- Cursor-oriented prompt or rule set
- VS Code workspace instruction set

Responsibilities:

- expose the workflow in the target environment's format
- map local tools and conventions to the core workflow

Adapter examples in this repository:

- `implementations/codex`
- `implementations/claude-code`
- `implementations/cursor`
- `implementations/vscode`

### 3. Provider Modules

Provider modules are the specialized capability layers the workflow can call into.

Examples in the current reference stack:

- UI direction provider
- expressive component provider
- product component provider
- motion primitive provider
- browser validation provider

Provider modules may change over time without changing the workflow identity.

## Reference Execution Model

```text
User request
    ->
Workflow classifier
    ->
UI direction phase
    ->
Motion implementation phase
    ->
Browser validation phase
    ->
Iteration loop
    ->
Final recommendation or integrated result
```

## Decision Boundaries

### UI Direction Phase

Use when:

- the tone is unclear
- the surface needs a motion strategy
- the team needs visual coherence before implementation

Outputs:

- direction
- motion intensity
- visual constraints
- shortlist criteria

### Motion Implementation Phase

Use when:

- a concrete motion treatment is needed
- an existing UI direction must be translated into components
- the host codebase needs actual source-level integration

Outputs:

- component choice
- variant choice
- dependency notes
- source mapping

Typical provider split:

- use an expressive component provider for high-impact motion surfaces
- use a product component provider for more system-friendly UI sections
- use a motion primitive provider when motion should be embedded into existing local components rather than introduced as a standalone imported block

### Browser Validation Phase

Use when:

- real rendering matters
- motion quality must be judged visually
- regressions or visual imbalance need confirmation

Outputs:

- observed issues
- pass/fail checks
- iteration targets

## Open Source Boundary

The public architecture should remain:

- generic
- MIT-compatible
- brand-neutral
- portable

Brand-specific overlays should remain outside the core repository or clearly separated as examples.

## Portability Rule

The workflow logic should stay more stable than any one editor or agent runtime.

That means:

- keep the phase model identical across adapters
- allow each adapter to express different install or instruction formats
- avoid pretending that Codex plugins, Cursor rules, and editor instructions are equivalent artifacts
- treat browser validation as a mandatory behavioral phase even when the local browser tooling differs
