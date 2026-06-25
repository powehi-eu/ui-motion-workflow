# Marketing Hero Provider Selection

## Scenario

User request:

> Make the homepage hero feel more premium and alive, but do not make it look gimmicky.

Host constraints:

- React app
- TypeScript
- Tailwind
- hero already exists structurally
- brand tone should remain premium and readable

## Workflow Decision

### Step 1: UI direction

Start with `ui-ux-pro-max`.

Desired output:

- premium
- restrained
- editorial
- one focal motion layer only
- avoid noisy cursor effects or overloaded backgrounds

### Step 2: Provider routing

Now compare providers.

#### `react-bits`

Good candidates:

- `BlurText`
- `SoftAurora`
- `GlassSurface`

Why it fits:

- excellent for premium hero motion
- strong visual identity

Risk:

- easy to overdo if both text and background are highly animated

#### `magicui`

Good candidates:

- polished hero-supporting UI blocks
- component-level motion that keeps the page structured

Why it fits:

- safer if the hero already has strong visual hierarchy and only needs elegant polish

Risk:

- may feel less distinctive if the brief really needs a standout signature

#### `motion-primitives`

Good candidates:

- subtle text reveal
- entry timing refinement
- button hover/state motion

Why it fits:

- best if the hero structure is already correct and only needs motion refinement

Risk:

- may be too understated if the current hero feels flat because it lacks a stronger visual moment

## Recommendation

Recommended primary path:

1. `ui-ux-pro-max`
2. `react-bits` for one focal motion layer
3. `motion-primitives` for secondary micro-motion if needed
4. browser validation

Concrete interpretation:

- use `react-bits` for the hero headline or one ambient background treatment
- use `motion-primitives` for CTA hover or subtle content reveal
- do not stack multiple dramatic effects at once

## Why Not `magicui` First Here?

`magicui` is still a valid option, but for this specific brief it is slightly less likely to create the premium “hero moment” the user is asking for.

If the same user had asked:

> Make this feature section cleaner, more polished, and slightly more alive

then `magicui` would likely become the first provider choice.

## Validation Focus

After implementation, check:

- headline readability during motion
- whether the background competes with CTA text
- whether the page still feels premium rather than flashy
- whether mobile hero density remains comfortable
