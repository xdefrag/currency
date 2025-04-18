# Slide Structure

## Slide Separators

Use `---` surrounded by newlines to separate individual slides.

```markdown
# Slide 1
Content for the first slide.

---

# Slide 2
Content for the second slide.
```

## Frontmatter

Use YAML frontmatter at the beginning of the file or a slide (`---`) to configure slide-specific options or presentation metadata.

```yaml
---
# Applied to the whole presentation if at the top
title: My Presentation
theme: default
---

# Slide 1 Content

---
# Applied only to this slide
layout: center
transition: fade-out
---

# Slide 2 Content
```

Common frontmatter options include `title`, `theme`, `layout`, `class`, `background`, `transition`, `level` (for ToC).

## Speaker Notes

The last HTML comment block (`<!-- -->`) in a slide is treated as speaker notes, visible in Presenter Mode.

```markdown
# Slide Content

<!--
This is a speaker note.
It can contain **Markdown** and HTML elements.
-->
``` 