# fig-10-the-only-link

Replaces `fig-5-two-sides-one-broker`. Site numbering is append-only, so this is **Fig. 10**.

## The one sentence

The two sides never see each other. A person at ConvergX is the only thing that joins them.

## Why the old one failed and what this does instead

Fig. 5 was two identical circles and a line: a symmetric connection diagram. It could not say who
was asking, and the "person" was a dot on a wire between equals. This plate is asymmetric on
purpose: ONE dashed line arrives from the left (the side asking), FIVE dashed lines converge from
the right (member companies), and every one of them stops at a single dot on an unbroken solid
vertical line. The line is the screen. The dot is the person. Nothing crosses the screen except
at the dot, so anonymity is drawn, not captioned.

## Strings, ship character for character

**aria-label** (on the `<svg>`):

    Diagram: an unbroken solid vertical line divides the drawing. From the left, one dashed line arrives at a single dot on that line, labelled a person at ConvergX. From the right, five dashed lines converge on the same dot. Every line stops at the dot. Nothing crosses the vertical line anywhere else.

**Labels** (four, uppercase in the DOM): `THE SIDE ASKING`, `MEMBER COMPANIES`,
`A PERSON AT CONVERGX`, `NOTHING ELSE CROSSES`.

## Geometry (artboard units)

| | |
|---|---|
| viewBox | `80 34 1440 630`. Root getBBox in headless Chromium: x 100, y 58.2, w 1400, h 583.4. Pad is 20 each side, rounded outward to whole units on top and bottom. No `width` or `height` attribute. |
| The screen | solid, `(800,60)` to `(800,640)`, stroke 2, `pathLength="1"` for the site draw-on |
| The side asking | one dashed line, `(100,350)` to `(792,350)`, stroke 1.5, dash `4 9` |
| Member companies | five dashed cubic curves from x 1500 at y 110, 230, 350, 470, 590, all landing at `(808,350)` |
| The person | one dot, `(800,350)` r 10, on the screen line |
| Labels | font-size 24, letter-spacing 3, monospace stack. At 660px render the plate scales 0.458, so labels land at 11px. |

Every stroke and fill is `currentColor` or `none`, as presentation attributes, so the file reads
standalone on any ground. The site classes (`fig-solid`, `fig-dash`, `fig-dot`, `fig-label`) are
also on every element; when inlined, styles.css section 20 overrides the attributes and the
reveal plays in DOM order (solid, dashed, dot, labels). Keep that order.

## Do not change

- Do not break the vertical line at the dot. A gap turns the screen into a gate that things pass
  through, which is the opposite claim. The dot sits ON an unbroken line.
- Do not let any dashed line reach past x 792 on the left or x 808 on the right. They end at the
  person, never at the other side.
- Do not equalise the sides. One line in, five lines in is the point. Any count above one on the
  right is fine; one on the left is fixed.
- Dot radius 10, not the family's 6. On a solid line a 6 disappears at 660px. Checked in the render.
- No arrowheads. Direction and force are not claimed.

## Verify

Rendered 2026-09-14 in headless Chromium at 660px wide on black and on white. All four labels
legible, the dot visible on both grounds, no colour literal in the file.
