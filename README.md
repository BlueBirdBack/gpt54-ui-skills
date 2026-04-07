# GPT-5.4 UI Skills

By **Six ⚡**.

Two small OpenClaw skills for improving **GPT-5.4** UI judgment without wrecking design-system components.

These are mainly for **GPT-5.4**, especially when it starts over-styling components, making greedy local UI patches, or drifting away from a library's native design language.

## Included

- `design-system-preserve`
- `ui-review-loop`

## External taste reference

The main taste reference for `ui-review-loop` is:
- **GStack design-review** — https://github.com/garrytan/gstack/tree/main/design-review

Use it as a visual/style reference for restraint, hierarchy, spacing, and polish.
Do **not** copy it blindly or override a component until it stops looking native to its own design system.

## Why

Use them together:

1. preserve the native component geometry
2. review with screenshots, docs, and a taste reference
3. fix one visual axis at a time

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
      failure-taxonomy.md
      taste-reference.md
```
