# Advanced Features

This covers a few more advanced Slidev capabilities.

## Importing Slides

Import slides from another Markdown file using the `src` frontmatter key on a slide separator.

```markdown
# My Main Presentation

Content...

---
src: ./shared/common-intro.md
---

More content...

---
# Import specific slides by index (1-based)
src: ./another-deck.md:1,3-5 
---
```

- Use ranges (`3-5`) and individual indices (`1`).
- Frontmatter from the imported slides can be merged or overridden.

## Drawing

Enable drawing tools via the navigation bar (Pen icon) or `Shift+S`.

- **Persistence:** Drawings are temporary by default. Set `drawings: { persist: true }` in global frontmatter to save drawings with the presentation data.
- **Configuration:** Customize pen colors, sizes, etc. See [Drawing Docs](https://sli.dev/features/drawing).

## Recording

Slidev has built-in recording features accessible from the navigation bar (Camera icon).

- **Presenter Mode:** Start recording in Presenter Mode (`?presenter=true` URL).
- **Camera View:** Show your webcam feed overlayed on the slides.
- **Export:** Recordings can often be saved or exported (details may vary based on setup).

## Exporting

Export your presentation to various formats using the navigation bar or CLI commands:

- **PDF:** `slidev export` (default)
- **PNGs:** `slidev export --format png` (one image per slide/click)
- **PPTX:** `slidev export --format pptx` (experimental, requires `playwright-chromium`)
- **Single-Page Application (SPA):** `slidev build` (creates a hostable web app in `./dist/`)

See [Exporting Docs](https://sli.dev/guide/exporting) for more options (dark mode, clicks, etc.). 