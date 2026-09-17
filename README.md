# Aroma & Co. — Café Landing Page

A self-directed front-end demo: a single-page landing site for a fictional
specialty coffee shop in Bengaluru. Built by hand to practise layout,
motion, and type — no frameworks, no build step, no UI kit.

**Live demo:** open `index.html` in a browser, or serve it with
`python3 -m http.server`.

## What it is (and isn't)

This is a **portfolio/practice piece, not a client project.** "Aroma & Co."
is invented — the brand, copy, menu, and stats are all written for the demo.
It exists to show design and vanilla-JS implementation skill in a
self-contained artifact, so it's honest to read it that way.

## Stack

Plain HTML, CSS, and JavaScript in one file (`index.html`, ~880 lines).
Google Fonts (Cormorant Garamond + DM Sans) is the only external dependency.
No npm, no bundler, no runtime.

## What's implemented

- **Custom cursor** — a dot plus a lerp-eased follower ring that scales on
  interactive elements, using `requestAnimationFrame` and `mix-blend-mode`.
- **3D card tilt** — pointer-tracked `rotateX/rotateY` transform on the
  signature-blend card, reset on mouse leave.
- **Scroll reveals** — a single `IntersectionObserver` drives staggered
  entrance animations across sections; menu cards get incremental
  `transition-delay`.
- **Infinite marquee** — CSS-keyframe ticker of café taglines.
- **Adaptive nav** — background and backdrop blur shift past 60px of scroll.
- **Design system** — colour palette and spacing as CSS custom properties
  (`--espresso`, `--caramel`, `--latte`, …); animated SVG coffee cup with
  CSS steam; floating particle accents.

## Structure

Hero → Our Story (with stats) → Menu grid → Atmosphere / Visit (hours) →
Footer. Anchor nav with `scroll-behavior: smooth`.

## Known limitations

Honest list, since this is a demo rather than production work:

- One `@media` breakpoint (900px); it is not fully responsive on small
  phones and the layout has not been tested below ~375px.
- `cursor: none` with a JS-driven cursor degrades on touch devices and hurts
  accessibility; there is no `prefers-reduced-motion` fallback.
- Everything lives in one file — fine at this size, not how I'd structure a
  real project.
- Content is placeholder; the "Reserve a Table" CTA is non-functional.

## Author

Diganth Shetty ([@coding-shetty](https://github.com/coding-shetty))
