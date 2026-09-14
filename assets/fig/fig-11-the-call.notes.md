# fig-11-the-call

Replaces `fig-6-vetting-aperture`. Site numbering is append-only, so this is **Fig. 11**.

## The one sentence

The review ends in a decision. What comes out is introduced, or not taken forward.

## Why the old one failed and what this does instead

Fig. 6 drew the decision as two bare vertical lines with a gap, which read as nothing, and its
two outcomes were a solid curve and a dashed curve at nearly the same angle, which did not read
as two fates. This plate puts the decision on a short solid vertical through a dot: the call, a
moment crossed, not a wall. The outcomes differ four ways at once so they register in a second:
direction (up versus down), line (solid versus dashed), length (to the edge versus a short way),
and ending (open versus a solid bar). The bar is a plain stop, the engineering end-of-line mark.
It says decided, not defective.

## Strings, ship character for character

**aria-label** (on the `<svg>`):

    Diagram: a dashed line comes in from the left and reaches a dot on a short solid vertical line, labelled the call. Two lines leave the dot in different directions. The upper one is solid and runs all the way to the right edge, labelled introduced. The lower one stays dashed, drops away, and stops at a short solid bar, labelled not taken forward.

**Labels** (four, uppercase in the DOM): `UNDER REVIEW`, `THE CALL`, `INTRODUCED`,
`NOT TAKEN FORWARD`.

## Geometry (artboard units)

| | |
|---|---|
| viewBox | `80 104 1480 564`. Root getBBox in headless Chromium: x 100, y 127.6, w 1440, h 519.2. Pad is 20 each side, rounded outward to whole units on top and bottom. No `width` or `height` attribute. |
| The call | solid vertical, `(700,230)` to `(700,470)`, stroke 2 |
| Under review | dashed, `(100,350)` to `(692,350)`, stroke 1.5, dash `4 9` |
| Introduced | solid cubic `M 708 350 C 900 350, 1050 180, 1540 180`, runs to the right edge of the box |
| Not taken forward | dashed cubic `M 708 350 C 830 350, 900 540, 1060 560`, then a solid bar `(1060,532)` to `(1060,588)` across its end |
| The decision | one dot, `(700,350)` r 10 |
| Labels | font-size 24, letter-spacing 3, monospace stack. At 660px render the plate scales 0.446, so labels land at 10.7px. |

Every stroke and fill is `currentColor` or `none`, as presentation attributes. The site classes
(`fig-solid`, `fig-dash`, `fig-dot`, `fig-label`) are on every element so styles.css section 20
and the reveal still apply when inlined. DOM order is solid, dashed, dot, labels. Keep it.

## Do not change

- Exactly one branch continues and exactly one stops. Two of either turns the plate into a rate.
- The introduced branch turns solid AT the dot, not further along. Solid means decided.
- The stopped branch stays dashed to the bar. Making it solid would make the two outcomes differ
  only by length, which is the failure this plate replaces.
- Keep the bar. Without it a dashed line that ends reads as pending, not decided.
- The vertical is short (240 units), not full height. Full height reads as a wall, and the wall
  belongs to Fig. 10.
- Dot radius 10, not the family's 6, for the same reason as Fig. 10.
- No arrowheads.

## Verify

Rendered 2026-09-14 in headless Chromium at 660px wide on black and on white. Four labels
legible, the two outcomes distinguishable at a glance, no colour literal in the file.
