# oli

A one-page site for the Elisava Vibe Coding lesson, live at https://olibcn.github.io/oli/

## Style

White and gray pixel art. Everything is drawn on a pixel grid, with hard edges and no blur or gradients.

### Colors

| Token     | Value     | Used for                     |
|-----------|-----------|------------------------------|
| `--paper` | `#ffffff` | page and card background     |
| `--grid`  | `#efefef` | background grid lines        |
| `--shade` | `#d4d4d4` | hard pixel shadows           |
| `--spark` | `#bdbdbd` | sparkle decorations          |
| `--gray`  | `#707070` | second heading               |
| `--ink`   | `#2b2b2b` | card frame and first heading |

### Type

- Font: [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) from Google Fonts, falling back to `monospace`.
- Sizes are multiples of 8 so the pixel font stays crisp: 24px on phones (16px under 360px wide), 40px from 640px, 48px from 960px.
- Font smoothing is off, so the letters keep square edges.
- Headings have a hard shadow one font pixel down and right (`0.125em`).

### Layout and shapes

- The background is a 16px grid of light gray lines, like graph paper.
- One white card is centered on the page.
- The card frame is a 4px (`--px`) border with notched corners, plus a stepped gray drop shadow. Both are drawn with stacked `box-shadow`s, not `border`.
- Two pixel sparkles sit in opposite corners of the card (inline SVG with `shape-rendering="crispEdges"`).

### Content

1. `<h1>` "hola món", in `--ink`
2. `<h1>` "jo soc oli", in `--gray`, followed by a blinking block cursor

The cursor blinks with a stepped animation and stays still when the visitor's system asks for reduced motion.

## Publishing

GitHub Pages serves `index.html` from the root of the `main` branch. Push to `main` and the site updates within about a minute.
