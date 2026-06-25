# Providers

## Purpose

This document explains how `ui-motion-workflow` should choose between the current motion/component providers in the reference stack.

The goal is not to rank providers globally. The goal is to route the request to the provider that best matches the surface, the tone, and the implementation constraints.

## Provider Summary

### `react-bits`

Use when the UI needs:

- strong visual presence
- showcase-style motion
- animated hero treatments
- ambient or cinematic backgrounds
- memorable interaction effects

Best fit:

- landing pages
- hero sections
- promotional blocks
- expressive demos

Tradeoff:

- can become visually dominant quickly
- requires more restraint on dense product surfaces

### `magicui`

Use when the UI needs:

- polished component-level motion
- stronger product-readiness
- modern UI blocks that still feel structured
- motion that complements layout rather than dominating it

Best fit:

- cards
- sections
- navigation
- feature grids
- product-marketing hybrids

Tradeoff:

- usually less visually distinctive than the boldest `react-bits` choices

### `motion-primitives`

Use when the UI needs:

- embedded motion in an existing local component
- micro-motion rather than imported visual blocks
- reusable animation recipes
- lower-level control over timing and behavior

Best fit:

- existing product UI
- component refactors
- subtle reveals
- hover, entry, and state transitions

Tradeoff:

- more implementation work
- less “instant wow” than prebuilt component libraries

## Selection Heuristics

### Choose `react-bits` if:

- the surface is a hero or showcase zone
- the user wants a bold visual signature
- the page can support one strong motion layer
- a prebuilt dramatic effect is acceptable

### Choose `magicui` if:

- the surface is still user-facing and polished, but should remain product-like
- the request is component-oriented rather than effect-oriented
- the result should feel easier to absorb inside a broader design system

### Choose `motion-primitives` if:

- the host component is already structurally correct
- the missing piece is the motion behavior itself
- subtlety and composability matter more than spectacle
- introducing a new imported visual block would be heavier than needed

## Priority Rule

When multiple providers could work:

1. prefer the least disruptive provider that still satisfies the design intent
2. prefer `magicui` or `motion-primitives` on dense product interfaces
3. prefer `react-bits` on marketing or showcase surfaces

## Anti-Patterns

- Do not use `react-bits` by default for every motion task.
- Do not use `motion-primitives` when a clean product-ready component library answer already exists.
- Do not use `magicui` if the design direction explicitly calls for a more theatrical, ambient, or experimental effect.

## Relationship with `ui-ux-pro-max`

`ui-ux-pro-max` should define:

- tone
- motion intensity
- visual constraints
- anti-patterns

Provider selection should happen after that direction is clear whenever possible.
