# Design moves

Borrowed selectively from **pbakaus/impeccable**.

These are not separate skills here.
They are a tighter vocabulary for choosing the right kind of fix before touching code.

## clarify
Use when:
- hierarchy is weak
- the important thing is not obvious
- title/meta/action emphasis is inverted

Typical fixes:
- stronger spacing hierarchy
- more obvious grouping
- clearer emphasis on one primary element

Do **not** default to louder color for this.
Often the real fix is spacing or typographic contrast.

## quieter
Use when:
- UI feels heavy, muddy, or theatrical
- too many effects are fighting at once
- a component became louder instead of clearer

Typical fixes:
- reduce contrast harshness
- remove one decorative layer
- soften over-dark surfaces
- use calmer neutrals and less visual shouting

This is one of the most useful moves for GPT-5.4.

## arrange
Use when:
- placement is wrong
- width is wrong
- layout rhythm is weak
- everything became a repetitive card grid

Typical fixes:
- narrow the working width
- improve left alignment / composition
- introduce better grouping rhythm
- reduce monotony before changing color

## typeset
Use when:
- text is mushy or crushed
- headings and body copy feel too similar
- measure is too wide
- dense UI became hard to scan

Typical fixes:
- tighten the size ladder
- improve line height and measure
- reduce noisy all-caps / badge spam
- make labels quieter and key text clearer

## normalize
Use when:
- the UI drifted from the design system or docs
- custom overrides accumulated
- the component no longer looks native

Typical fixes:
- return toward stock component behavior
- remove geometry drift
- reapply only the smallest product-specific override

## harden
Use when:
- overflow breaks the layout
- empty/error/loading states are missing
- internationalization or long text will break the UI

Typical fixes:
- add truncation/wrapping rules
- test extreme inputs
- handle empty/error/loading states explicitly

## Choosing the move
Ask:
1. Is this primarily hierarchy? → **clarify**
2. Is it too heavy or too loud? → **quieter**
3. Is layout/placement the main problem? → **arrange**
4. Is text density/measure the problem? → **typeset**
5. Did it drift from the design system? → **normalize**
6. Will it break in real use? → **harden**

Pick the smallest fitting move first.
Do not combine three moves unless the first screenshot after the first move still shows a clearly separate remaining problem.
