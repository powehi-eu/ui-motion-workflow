---
name: ui-motion-workflow
description: Orchestrate UI direction, motion component selection, implementation, and browser validation for polished frontend work. Use when Codex needs to improve a visual surface with animation or interactive polish; when a request mixes design intent, component choice, and real-browser verification; when `ui-ux-pro-max`, `react-bits`, `magicui`, or `motion-primitives` should be chained together; or when a localhost UI needs a motion-aware iteration loop rather than a single isolated code change.
---

# UI Motion Workflow

Use this skill as the top-level coordinator for motion-aware UI work in Codex.

Do not replace specialized skills with this orchestrator. Use it to decide sequence, scope, and handoff.

## Core Flow

1. Read the target surface in the host codebase and understand the user's goal.
2. Decide whether the request needs:
   - direction first
   - implementation first
   - validation only
3. If visual direction or motion tone is unclear, use `ui-ux-pro-max` first.
4. If a concrete animated implementation is needed, choose the right provider:
   - `react-bits` for expressive or high-impact motion components
   - `magicui` for product-friendly animated UI components
   - `motion-primitives` for lower-level motion patterns inside an existing local component
5. Integrate the selected approach into the host project using its existing conventions.
6. Validate the result in the browser on the real localhost surface.
7. Iterate until the motion feels coherent, usable, and appropriately restrained.

## Decision Rules

Read [references/decision-tree.md](references/decision-tree.md) when deciding which phase to enter first.

Default decisions:

- Use `ui-ux-pro-max` first when the user wants a better feel, stronger polish, better visual hierarchy, or a motion direction but has not chosen an implementation.
- Use `react-bits` first when the user explicitly wants a bold animated component, hero effect, ambient background, or React Bits specifically.
- Use `magicui` first when the user wants polished UI components that should still feel product-ready and structured.
- Use `motion-primitives` first when the user wants motion embedded into an existing component instead of importing a distinct visual block.
- Go directly to browser validation when the code change already exists and the main question is whether it looks right or regressed.

## Skill Chaining

### With `ui-ux-pro-max`

Use `ui-ux-pro-max` to establish:

- motion intensity
- visual tone
- editorial vs playful vs technical feel
- typography and color direction that affect motion choices
- constraints around clarity and restraint

Expected output from this phase:

- a concise direction summary
- a shortlist of suitable motion patterns
- explicit anti-patterns to avoid

### With `react-bits`

Use `react-bits` to translate the direction into:

- a concrete component shortlist
- exact `JS/TS` and `CSS/TW` variant choice
- dependency notes
- local source paths
- integration cautions

If `ui-ux-pro-max` already established a direction, preserve it. Do not choose the most dramatic React Bits option unless the direction explicitly calls for it.

### With `magicui`

Use `magicui` when the surface should feel polished and motion-aware without becoming theatrically animated.

Typical fits:

- cards
- badges
- buttons
- feature sections
- product UI blocks

Expected output from this phase:

- a shortlist of product-friendly components
- implementation notes that fit modern React, Tailwind, and TypeScript stacks
- cautions about adapting the component to the host design system

### With `motion-primitives`

Use `motion-primitives` when the right answer is a motion behavior rather than a prebuilt visual block.

Typical fits:

- reveal patterns
- hover transitions
- layered entrance motion
- subtle interaction feedback
- reusable motion recipes inside existing components

Expected output from this phase:

- a motion pattern choice
- adaptation guidance for the host component
- notes on keeping the effect subtle and composable

## Browser Validation

Use browser validation to judge the real output, not only the source diff.

Always check for:

- visual balance
- motion intensity
- readability during motion
- responsive behavior
- interaction comfort
- whether the effect competes with surrounding content

Read [references/validation-checklist.md](references/validation-checklist.md) when validating the result.

## Recommendation Output

When the task is advisory, return:

- the chosen phase order
- the chosen direction summary
- the chosen component or implementation pattern
- the reason it fits
- the specific variant or integration path
- the browser checks that should confirm success

## Implementation Output

When the task includes code changes:

- preserve the host codebase conventions
- keep motion scoped to one focal layer when possible
- avoid stacking multiple strong effects unless the page is intentionally theatrical
- prefer subtle, legible motion for product UI and denser interfaces
- prefer `magicui` or `motion-primitives` over `react-bits` when the host surface is product-dense and system-like

## Pattern Mapping

Read [references/pattern-mapping.md](references/pattern-mapping.md) for quick mappings between user intent, design direction, and likely motion solutions.
