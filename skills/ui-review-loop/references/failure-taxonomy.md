# UI failure taxonomy

## Common failure modes
- **too dark** — readability OK, but the surface feels muddy/heavy
- **too wide** — element sprawls and loses hierarchy
- **too cramped** — controls/title collide or wrap awkwardly
- **overstyled** — too many custom layers, shadows, borders, tints, effects
- **wrong radius** — corners no longer match the design system
- **wrong hierarchy** — title/meta/control emphasis is inverted
- **weak contrast** — hard to read or easy to miss
- **too loud** — high contrast but crude/theatrical
- **poor placement** — correct styling, wrong location
- **header crush** — title and controls fighting for one line
- **card monotony** — everything became identical cards/grids with no rhythm
- **centered-everything drift** — content lost structure by being centered and symmetrical by default
- **typography mush** — too many font sizes too close together, weak measure, weak leading
- **internal-tool heaviness** — black slabs, over-dense chrome, oppressive darkness
- **false premium** — gradients, glass, glow, or blur used as a substitute for hierarchy

## Fix order
1. layout/width problems
2. placement/composition problems
3. hierarchy/spacing problems
4. typography problems
5. tint/contrast problems
6. polish

## Reset signal
If you have touched radius + padding + shadow + border + background + layout in one pass, reset mentally and start over with one-axis edits.
