# Shape Dividers

An SVG section-divider generator. Pick a shape, an edge, a colour and a size; copy pure CSS.

**Live:** https://nandiraju.github.io/dividers/

## How it works

The divider is a `::before` pseudo-element carrying the SVG as a `background-image` data URI.
Your markup never changes — you add one class:

```html
<div class="svg_divider">
  <h2>Your section</h2>
</div>
```

- **Four edges.** Top, right, bottom and left are each a separately-oriented SVG with a swapped
  viewBox, not a CSS rotation.
- **Long axis** (100–400%) and **short axis** (0–400px) drive `background-size`; **position**
  (0–100%) drives `background-position`, and only bites once the shape overflows its container.
- **Animate** locks the long axis to 100%, applies `scaleX(n)`, pins `transform-origin` to the
  anchored edge and ping-pongs the shape across it. It is mutually exclusive with **flip** —
  both drive `transform`.
- **Responsive** emits a mobile base plus `768px` and `1025px` tiers, each independently
  configurable, plus a `2100px` rule that grows the short axis with the viewport.

50 shapes, from [zenplates](https://zenplates.co/patterns/dividers) and
[svgbackgrounds](https://svgbackgrounds.com/elements/svg-shape-dividers).

## Caveat

The generated base rule sets `position: relative` on `.svg_divider`, because the pseudo-element is
absolutely positioned against it. If you apply the class to an element that is already
`position: absolute`, the divider's rule will override it. Wrap it instead.

## Files

| File | |
|---|---|
| `index.html` | the generator — self-contained, no dependencies |
| `divicraft.html` | earlier DiviCraft playground (uses `style.css`, `shapes.js`) |
| `divider_demo.html` | static pattern reference |
