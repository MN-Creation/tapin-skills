---
name: tapin-wave-commissioning
description: How the TapIn CEO commissions implementation work from a ratified design brief. Use whenever you file an implementation Issue against a brief — especially when the brief introduces a new putter family, head type, parameter set, or other Director-visible deliverable. Defines the parallel-issue commissioning rule that prevents kernel-only false-closes.
---

# TapIn wave commissioning

## When to use

You (the CEO) have a ratified design brief from GolfPro. The brief is approved and
ready for implementation. You are about to file the Issue(s) that turn the brief
into shipped code.

## The parallel-issue rule

**For every brief implementation Issue you file against the Geometry Engineer (or
any kernel-side engineer), file a parallel UI-surfacing Issue against the
Full-Stack Engineer at the same time.** Both Issues have `parentId = <design brief
Issue>`. The brief's parent Issue does NOT close until both child Issues close.

### Why

[TAP-188](/TAP/issues/TAP-188) shipped a tour-blade head family at the kernel + API
+ container level but the UI head-family picker still hardcoded `mallet | blade`.
The Director could not reach the deliverable through Studio. Kernel-only
commissioning produces a false-close: the agent's definition of done is internally
consistent (PR merged, container redeployed) but the deliverable-as-Director-sees-
it is unreachable.

### Exceptions

Skip the parallel UI Issue **only** if the brief itself includes an explicit §12
kernel-only opt-out with a documented alternative verification path (see GolfPro's
`putter-design-brief-format` §12). If the brief is silent on UI exposure, default
to filing the parallel Issue and ask GolfPro to amend the brief.

## Issue templates

### Kernel implementation Issue (GE)

- **Title:** `Implement: <brief title>`
- **Parent:** the brief Issue
- **Goal:** the originating brief's goal
- **Body:** brief reference + acceptance criteria from brief
- **Blocks:** the parallel UI Issue (the UI Issue cannot land until the kernel
  Issue's API surface is stable)

### Parallel UI surfacing Issue (FSE)

- **Title:** `Studio UI: surface <brief deliverable>`
- **Parent:** same brief Issue
- **Goal:** same goal
- **Body:** copy the brief's §12 *Studio UI exposure* section verbatim into the
  Issue body, plus the Director smoke step
- **Blocked by:** the kernel Issue's PR (so FSE waits for the API surface)

## Merge-gate coordination

When the Code Reviewer is about to approve the kernel PR and raise the Director
merge-gate confirmation, the CR merge-gate prompt MUST reference the parallel UI
Issue and ask: *"Has the UI-surfacing Issue ([TAP-N]) also landed? If not, the
kernel PR may merge but the Director smoke will fail until the UI Issue ships."*

This is captured in CR's `code-review-checklist` skill. When you file the kernel
Issue, include a reference to the parallel UI Issue ID so CR can find it without
searching.

## Brief parent closure

The brief Issue's parent (or the wave epic, if there is one) does NOT close to
`done` until BOTH:

1. Kernel Issue is `done` with `gh pr view --json merged == true`
2. UI surfacing Issue is `done` with `gh pr view --json merged == true` AND the
   Director has confirmed the smoke path works

If either fails, the brief is `in_review` or `blocked`, not `done`.

## Origin

[TAP-190](/TAP/issues/TAP-190), filed by the Director on 2026-05-23 after the
[TAP-188](/TAP/issues/TAP-188) audit. Sibling rule to the post-merge `gh pr view
--json merged` guardrails ([TAP-158](/TAP/issues/TAP-158), [TAP-159](/TAP/issues/TAP-159),
[TAP-164](/TAP/issues/TAP-164), [TAP-167](/TAP/issues/TAP-167)) — those guard
against the first false-close shape (PR not merged); this guards against the
second shape (kernel-only, no UI surface).
