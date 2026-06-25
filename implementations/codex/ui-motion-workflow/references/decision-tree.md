# Decision Tree

## Start Here

Classify the request before choosing tools.

## 1. Is the problem mainly about visual direction?

Use `ui-ux-pro-max` first if the user is saying things like:

- "make this feel more premium"
- "improve the polish"
- "the section feels flat"
- "I want motion but not too much"
- "recommend a better interaction style"

Then move to `react-bits` only after a direction is clear.

## 2. Is the problem mainly about concrete implementation?

Use `react-bits` first if the user is saying things like:

- "add a React Bits component here"
- "pick the right animated hero text"
- "I want a glass card / animated nav / ambient background"
- "which React Bits component fits this section?"

If the result still needs stronger coherence, backfill direction with `ui-ux-pro-max`.

## 3. Is the code already changed and now needs real validation?

Go to browser validation first if the user is effectively asking:

- "does this look right?"
- "check the localhost result"
- "validate the motion"
- "see whether this regressed"

## 4. Is the request mixed?

If the request blends feel + implementation + verification, use the full orchestrated flow:

1. `ui-ux-pro-max`
2. choose provider:
   - `react-bits`
   - `magicui`
   - `motion-primitives`
3. implementation in host repo
4. browser validation

## Provider Routing

Choose `react-bits` when:

- the surface is hero-like
- the effect is meant to be visually memorable
- ambient motion or a showcase component is appropriate

Choose `magicui` when:

- the surface is part of a product UI
- the team wants more structure and less spectacle
- the desired output is closer to a polished UI block than an effect demo

Choose `motion-primitives` when:

- the host already has the right component shape
- only the motion layer is missing
- subtle or composable motion is preferred over importing a new visual block

## Default Bias

When uncertain:

- direction before implementation
- implementation before browser polish
- browser validation before final signoff
