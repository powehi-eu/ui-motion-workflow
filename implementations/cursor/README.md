# Cursor Adapter

## Purpose

This folder provides a Cursor-oriented adaptation of `ui-motion-workflow`.

The main artifact is a reusable rule file that can be adapted into a repository-level Cursor rules setup.

## Included Artifact

- `ui-motion-workflow.mdc`
  A Cursor rule focused on sequencing direction, provider choice, implementation, and browser validation.

## Recommended Usage

Use this adapter when you want Cursor to:

- classify whether a UI task needs direction or implementation first
- choose between `react-bits`, `magicui`, and `motion-primitives`
- avoid over-animating dense product surfaces
- keep browser validation as the final quality gate

## Practical Note

Treat the rule file as a portable starter. Teams can merge it into existing project rules rather than forcing a separate isolated setup.
