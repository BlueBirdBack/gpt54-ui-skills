# GPT-5.4 UI Skills

By **Six ⚡**.

Two small OpenClaw skills for improving **GPT-5.4** UI judgment without wrecking design-system components.

These are mainly for **GPT-5.4**, especially when it starts over-styling components, making greedy local UI patches, or drifting away from a library's native design language.

This repo now also borrows selectively from **pbakaus/impeccable** — mainly its stronger vocabulary for design moves like *clarify*, *quieter*, *arrange*, *typeset*, *normalize*, and *harden*. The goal is to make UI critique more precise without turning this repo into a clone of `impeccable`.

## Included

- `design-system-preserve`
- `ui-review-loop`

## External taste reference

The main taste references for `ui-review-loop` are:
- **GStack design-review** — https://github.com/garrytan/gstack/tree/main/design-review
- **pbakaus/impeccable** — https://github.com/pbakaus/impeccable

Use them as taste references for restraint, hierarchy, spacing, typography, and polish.
Do **not** copy them blindly or override a component until it stops looking native to its own design system.

What we want from `impeccable` specifically:
- better naming for design moves
- stronger anti-slop taste rules
- better judgment about layout rhythm, typography, and visual calm

What we do **not** want to import blindly:
- repo architecture complexity
- duplicated truth across docs/configs
- provider/distribution drift

## Why

Use them together:

1. preserve the native component geometry
2. review with screenshots, docs, and a taste reference
3. classify the problem with a sharper design-move vocabulary
4. fix one visual axis at a time

## Best fit

These skills are primarily intended for:
- **GPT-5.4**
- design-system component refinement
- screenshot-based UI review loops
- preventing overstyled / homemade-looking UI changes

## Layout

```text
skills/
  design-system-preserve/
    SKILL.md
  ui-review-loop/
    SKILL.md
    references/
      checklist.md
      design-moves.md
      failure-taxonomy.md
      taste-reference.md
```
