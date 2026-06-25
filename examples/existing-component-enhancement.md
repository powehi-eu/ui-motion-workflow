# Existing Component Enhancement

## Scenario

User request:

> This pricing card is structurally fine, but it feels dead. Add subtle motion without changing the layout.

Host constraints:

- existing React component already matches the layout requirements
- styling is already aligned with the local design system
- motion must feel premium and controlled
- no new visually dominant block should replace the component

## Workflow Decision

### Step 1: UI direction

Start with `ui-ux-pro-max` only if the intended tone is unclear.

Desired output:

- restrained
- premium
- responsive to interaction
- motion should reinforce hierarchy, not redraw attention constantly

If the tone is already known, skip straight to provider routing.

### Step 2: Provider routing

#### `motion-primitives`

Best fit here.

Why:

- the component structure is already correct
- only the motion layer is missing
- hover, entry, and emphasis behaviors can be added without importing a whole new block

Good use cases:

- slight entrance reveal
- hover elevation or glow
- CTA emphasis timing
- layered micro-motion between card elements

#### `magicui`

Possible fallback if the existing component is fine structurally but still lacks a more polished component treatment that is close to the same shape.

Why it is not the default:

- the request says not to change layout significantly
- `magicui` is better when a stronger block-level upgrade is acceptable

#### `react-bits`

Usually not the right first choice here.

Why:

- the request is refinement-oriented, not spectacle-oriented
- importing a more expressive animated component would likely overshoot the brief

## Recommendation

Recommended path:

1. inspect the existing component
2. confirm tone with `ui-ux-pro-max` if needed
3. use `motion-primitives`
4. implement directly in the local component
5. validate on localhost

## Validation Focus

Check:

- the component still feels like the same component
- motion improves perceived quality
- hover or reveal states do not feel noisy
- no layout shift is introduced
- the CTA remains the clearest actionable element
