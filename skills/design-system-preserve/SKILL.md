---
name: design-system-preserve
description: Preserve the native look of an existing UI-library component while making small product-specific adjustments. Use when restyling components from Nuxt UI, shadcn, Radix, Tailwind UI, or similar design systems; when a component started looking "ugly", "off-brand", "overstyled", or "not like the docs"; or when changes should stay close to the stock component while adjusting only color, placement, or one contrast layer.
---

# Design System Preserve

## Goal

Keep the component looking like the library designed it.

Do **not** redesign a design-system component unless the user explicitly asks for a redesign.

## Default method

1. **Start from stock**
   - Identify the library component and its native variant.
   - Mentally reset to the docs example before making new changes.

2. **Only change the minimum**
   Allowed by default:
   - color / tint
   - placement / offset
   - one subtle contrast layer if the background is noisy

   Not allowed by default unless explicitly required:
   - radius
   - spacing scale
   - internal layout
   - typography scale
   - shadow language
   - border thickness
   - icon sizing

   If you need more than that, stop and ask what kind of move this really is:
   - **normalize** back toward stock?
   - **quieter** because it got too loud/heavy?
   - **clarify** because hierarchy is weak?

   Most design-system fixes are one of those three — not a redesign.

3. **Preserve geometry**
   - Keep the library's proportions, padding rhythm, corner radius, and visual balance.
   - If you need to force `display`, `gap`, `padding`, or `border-radius`, stop and verify that the component still matches the docs.

4. **Compare against the docs**
   - Ask: does this still read as the same component family?
   - If the change makes the component look homemade, back out and retry with fewer overrides.
   - If you are solving a visibility problem, prefer this order:
     1. placement
     2. hierarchy clarification
     3. slight tint
     4. one contrast layer

   Do not jump straight to heavier shadows, larger radius, or custom background effects.

5. **One-axis edits**
   - Change one axis at a time:
     1. placement
     2. color
     3. contrast
   - Verify after each axis instead of stacking many style changes.

## Anti-patterns

Avoid these unless the user explicitly wants a redesign:
- stacking custom background + border + shadow + blur + radius + spacing overrides
- turning a compact alert into a banner/blob/strip
- fixing visibility by making the whole component louder instead of more legible
- editing on top of bad edits instead of resetting to stock behavior
- introducing premium-looking noise (glass, glow, gradient, heavy blur) just because the component felt boring
- changing multiple geometry variables at once and then calling the result "closer to the docs"

## Reset rule

If the component stops looking native:
1. revert mentally to stock component behavior
2. keep only the product requirement
3. reapply the smallest possible override set

## For map overlays

When a design-system component sits on top of a busy map/image:
- first try **placement**
- then try a **slight tint**
- then try a **light contrast layer**
- avoid heavy glassmorphism and oversized shadows unless the base component truly disappears

## Output standard

When done, the component should answer **yes** to all three:
- Does it still look like the library component?
- Is the requested change visible?
- Did we avoid unnecessary style overrides?
