# Dashboard Motion Polish

## Scenario

User request:

> This dashboard feels static. Add subtle motion polish, but keep it clean and trustworthy.

Host constraints:

- product UI
- information-dense layout
- cards, metrics, filters, and tables already exist
- motion should not distract from data reading

## Workflow Decision

### Step 1: UI direction

Start with `ui-ux-pro-max`.

Desired output:

- restrained
- trustworthy
- readable
- low-distraction
- motion should support hierarchy, not compete with it

### Step 2: Provider routing

#### `react-bits`

Possible fits:

- `CountUp`
- `FadeContent`
- `PillNav`

Why it can help:

- useful for isolated metric or navigation accents

Why it is not the default here:

- many React Bits choices are stronger than a dashboard usually wants

#### `magicui`

Possible fits:

- polished card-level components
- structured section blocks
- subtle component enhancements that still feel product-ready

Why it fits:

- better default for a product-facing dashboard than a highly expressive provider

#### `motion-primitives`

Possible fits:

- staggered metric reveal
- subtle card entrance
- controlled hover states
- state transitions on filters or tabs

Why it fits:

- ideal when the existing dashboard structure is already correct and only needs motion refinement

## Recommendation

Recommended primary path:

1. `ui-ux-pro-max`
2. `motion-primitives`
3. `magicui` only if a more component-level uplift is needed
4. `react-bits` only for very targeted accents
5. browser validation

## Example Interpretation

- use `motion-primitives` for metric cards entering cleanly and for subtle hover or filter transitions
- use `magicui` if one dashboard section needs a more polished card or block treatment
- use `react-bits` sparingly, for example a restrained `CountUp` on KPI surfaces

## Validation Focus

Check:

- data readability during motion
- whether hover states still feel calm
- whether motion improves hierarchy rather than noise
- whether the dashboard still feels trustworthy and efficient
