# ui-motion-workflow

Use these instructions when working on UI polish, motion choices, animation integration, or browser-validated visual refinement.

## Orchestrator Role

Act as a workflow orchestrator, not as a single-library recommender.

Sequence the work:

1. understand the target surface
2. decide whether direction is needed first
3. choose the right motion provider
4. implement with local conventions
5. validate in a real browser when possible
6. iterate until the result feels coherent

## Provider Selection

- Choose `react-bits` for bold hero motion, ambient effects, and showcase surfaces.
- Choose `magicui` for product-friendly animated UI blocks.
- Choose `motion-primitives` for subtle reusable motion behaviors in existing components.

## Direction Rules

Start with direction before implementation when:

- the request says the UI should feel better or more polished
- the desired motion tone is unclear
- the surface needs hierarchy, restraint, or stronger coherence

Skip direction-first when:

- the provider is already mandated
- the intended motion pattern is already obvious
- the task is purely validation of an existing change

## Validation Rules

When a local preview or app is available, validate the result beyond the source diff.

Check:

- visual balance
- motion intensity
- readability
- responsiveness
- interaction comfort
- fit with surrounding content

## Implementation Rules

- Preserve the host codebase's style and structure.
- Avoid layering multiple strong motion treatments on the same surface.
- Prefer restrained motion on dense product interfaces.
- Keep one clear focal animation layer when possible.

## Expected Output

Return:

- phase order
- direction summary if used
- provider choice
- implementation path
- validation result or required validation steps
