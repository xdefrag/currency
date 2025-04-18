# Themes and Layouts

## Themes

Themes control the overall look and feel (styles, fonts, components).
Apply a theme globally using the `theme` frontmatter key.

```yaml
---
theme: seriph # Use the 'seriph' theme
---
```

Find themes in the [Theme Gallery](https://sli.dev/resources/theme-gallery).

## Layouts

Layouts define the structure of a slide (e.g., title slide, two columns).
Apply a layout to a specific slide using the `layout` frontmatter key.

```yaml
---
layout: two-cols # Use the 'two-cols' layout for this slide
layoutClass: gap-16 # Optional: Add classes to the layout container
---

# Left Column Content

::right::

# Right Column Content
```

Common layouts include `default`, `center`, `cover`, `image-left`, `image-right`, `two-cols`, etc. Themes can provide custom layouts.

## Custom Layouts

This project includes the following custom layouts:

- `cover` - Title slide with a logo, used for the presentation cover.
- `author` - Author information slide with an image and personal details.
- `section` - Section divider slide with a title and bullet points for content.

### Section Layout

The `section` layout is used to create section divider slides. It includes:

- A title in the left column
- Content from the slide in the left column below the title
- Optional illustration in the right column (if provided)

Example usage:

```md
---
layout: section
title: Частные валюты
---

- Ithaca HOUR
- BerkShares
- Эра свободного банкинга
```

To add an illustration to the right column:

```md
---
layout: section
title: Частные валюты
illustration: /path/to/your-image.jpg
---

- List item 1
- List item 2
``` 