# NaughtyDuk — Website Clone

A frontend clone/rebuild of the [NaughtyDuk](https://naughtyduk.com) agency website. Built it as a personal project to practice advanced CSS layouts, custom cursor logic, and CSS animations.

## What's in it

- Full single-page layout with hero, about, projects grid, capabilities, clients and footer sections
- Custom cursor with a lagging ring effect (lerp animation in vanilla JS)
- Scrolling marquee ticker
- CSS grid-based project cards (12-column layout)
- Glitch animation on the hero background text
- Animated background grid that scrolls on loop
- Frosted glass nav that appears on scroll
- Grain/noise texture overlay using inline SVG filter
- Fully responsive (mostly — mobile nav still needs a hamburger menu, TODO)

## Tech

Just plain HTML, CSS and a bit of vanilla JS. No frameworks, no build tools. One file.

- Google Fonts (Bebas Neue, Space Mono, DM Sans)
- CSS custom properties for theming
- CSS Grid for the projects section layout
- `requestAnimationFrame` for the cursor ring animation
- `mix-blend-mode: difference` for the cursor effect

## What I learned

The cursor lag effect was the trickiest part — I kept getting a jittery ring until I understood lerp (linear interpolation). The formula is basically:

```
current += (target - current) * smoothingFactor
```

Setting the smoothing factor to `0.12` felt the best. Too high and it's instant, too low and it drags too much.

Also spent way too long on the glitch keyframe animation for the background DUK text. `clip-path` + `skewX` together gives that broken-signal look.

The project grid was originally going to be flexbox but grid with named column spans ended up being way cleaner for the asymmetric layout.

## Live Demo

> *(github.com/Asadullahx4/Agency-website-clone)*

## How to run

Just open `index.html` in a browser. That's it.

---

Built by me as a study/practice project. Original design belongs to NaughtyDuk Ltd.
