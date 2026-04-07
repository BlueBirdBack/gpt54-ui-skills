---
name: ui-review-loop
description: Review and improve UI by comparing live screenshots against component docs and a taste reference. Use when a UI looks ugly, off, cramped, overstyled, too dark, too wide, badly aligned, or "not like the docs"; when iterating on overlays, panels, alerts, cards, modals, forms, or dashboards; or when GPT-5.4 needs a stricter visual critique loop instead of greedy local patching.
---

# UI Review Loop

## Goal

Improve UI judgment with a tight visual review loop.

This skill is for **reviewing and refining** a UI, not blindly patching it.
If the UI uses a design-system component, pair this skill with `design-system-preserve`.

## Inputs to compare

Use these sources in order:
1. **Component truth** — the library docs example (Nuxt UI, shadcn, etc.)
2. **Taste reference** — e.g. GStack design-review
3. **Reality** — the live screenshot

Never judge from code alone if a screenshot can be taken.

## Review loop

1. **State the role**
   - What is this element supposed to do?
   - alert, panel, overlay, toolbar, header, card, modal, etc.

2. **Compare docs vs live**
   - What feels worse in live than in the docs?
   - What changed from the component's native look?

3. **Classify the failure mode**
   Use the smallest useful label:
   - too dark
   - too wide
   - too cramped
   - overstyled
   - wrong radius
   - wrong hierarchy
   - wrong spacing rhythm
   - weak contrast
   - too loud / theatrical
   - poor placement
   - text wrap / header crush

4. **Pick one axis only**
   Change only one of:
   - placement
   - width
   - spacing
   - color/tint
   - contrast layer
   - typography hierarchy

5. **Patch minimally**
   - prefer the smallest possible fix
   - avoid stacked overrides
   - if multiple things look wrong, fix the most damaging one first

6. **Re-check with screenshot**
   - if better, continue only if needed
   - if worse, mentally reset and retry with a smaller change

## Hard rules

- Screenshot first, judgment second
- One-axis edits beat multi-axis edits
- If the component starts looking homemade, back out
- Do not confuse "more visible" with "better"
- Do not keep layering edits on top of a bad direction

## Output standard

When reporting, say:
- what looked wrong
- what single fix you applied
- whether the new screenshot is actually better
- what still remains, if anything

## When to stop

Stop when all are true:
- it looks clearly better than the previous version
- it still belongs to the same design language
- no obvious wrapping/cramping/contrast issue remains
- the next change would be polish, not repair
