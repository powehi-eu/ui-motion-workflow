# ui-motion-workflow

Use this workflow when the task is about UI polish, motion direction, animated component choice, or browser-backed visual validation.

Act as an orchestrator rather than as a single-library recommender.

## Core Flow

1. Read the target surface and understand the user goal.
2. Decide whether the task needs:
   - direction first
   - implementation first
   - validation only
3. If visual direction or motion tone is unclear, establish a concise direction before selecting any implementation.
4. Choose the best provider:
   - `react-bits` for bold hero motion, ambient backgrounds, and expressive showcase effects
   - `magicui` for polished product-style UI blocks
   - `motion-primitives` for embedded motion behaviors inside existing components
5. Integrate the selected approach using the host codebase's conventions.
6. Validate the result in a real browser when a live surface is available.
7. Iterate until the motion feels intentional, readable, and proportionate to the surrounding UI.

## Selection Rules

- Prefer direction-first when the request asks for a better feel, stronger polish, or clearer visual hierarchy.
- Prefer implementation-first when the user already chose the provider or the design intent is obvious.
- Prefer validation-only when the main question is whether an existing motion change actually works.

## Provider Bias

- Use `react-bits` for visually expressive landing sections and showcase moments.
- Use `magicui` when the result should still feel product-ready and structured.
- Use `motion-primitives` when the best answer is a subtle motion pattern inside an existing local component.

## Validation Rules

Do not stop at source changes alone when a browser is available.

Always check:

- visual balance
- motion intensity
- readability during movement
- mobile behavior
- interaction comfort
- whether the effect competes with nearby content

## Output Shape

When the task is advisory, return:

- chosen phase order
- direction summary
- provider decision
- reason the provider fits
- validation checks to confirm success

When the task includes implementation, preserve local conventions and keep motion scoped to one focal layer when possible.
