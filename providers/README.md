# Providers

This folder defines the provider layer used by `ui-motion-workflow`.

Providers are not the workflow itself. They are the specialized implementation sources the workflow can route into once direction is clear.

## Current Providers

- [react-bits.md](react-bits.md)
- [magicui.md](magicui.md)
- [motion-primitives.md](motion-primitives.md)

## Contract

Each provider should be documented in terms of:

- best-fit surfaces
- strengths
- risks
- when it should be preferred
- when it should be avoided
- how it complements `ui-ux-pro-max`

## Selection Principle

Choose the provider that delivers the intended motion with the least disruption to the host codebase.
