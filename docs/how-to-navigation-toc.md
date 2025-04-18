# Navigation and Table of Contents

## Navigation Bar

Hover at the bottom-left corner to reveal the navigation controls.

- Previous/Next Slide
- Slide Overview
- Presenter Mode
- Dark Mode Toggle
- Download (PDF/PNG/PPTX)
- Camera View
- Drawing Tools
- Open in Editor
- GitHub Link (if configured)

## Keyboard Shortcuts

- `Right Arrow` / `Space`: Next slide or animation.
- `Left Arrow` / `Shift`+`Space`: Previous slide or animation.
- `Up Arrow`: Previous slide.
- `Down Arrow`: Next slide.
- `G`: Go to slide number.
- `D`: Toggle dark mode.
- `P`: Toggle presenter mode.
- `O`: Toggle slide overview.
- `C`: Toggle camera view.
- `S`: Toggle drawing mode.

(See [docs](https://sli.dev/guide/ui#navigation-bar) for full list)

## Table of Contents (Toc)

Use the `<Toc>` component to automatically generate a table of contents based on slide titles and levels.

```html
<Toc minDepth="1" maxDepth="3" /> 
```

- `minDepth` / `maxDepth`: Control the heading levels included.
- Use `title` and `level` frontmatter on slides to customize their appearance in the ToC.

```yaml
---
title: Custom Title for ToC
level: 2 # Indent this slide in the ToC
---
``` 