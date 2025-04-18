# Styling Slides

## UnoCSS Utility Classes

Slidev integrates [UnoCSS](https://unocss.dev/), allowing you to use utility classes directly in Markdown or frontmatter.

- **Frontmatter:** Apply classes to the entire slide using the `class` key.

  ```yaml
  ---
  class: text-center bg-blue-100
  ---
  ```

- **Inline HTML:** Apply classes directly to HTML elements.

  ```html
  <div class="p-4 rounded bg-green-50">
    Styled content.
  </div>
  ```

- **Markdown Attributes:** Apply classes using `{ ... }` syntax (requires `mdc: true` in frontmatter).

  ```markdown
  # A Heading { .text-red-500 .font-bold }
  
  A paragraph with a { .bg-yellow-200 } highlighted section.
  ```

## Slide-Scope Styles

Embed `<style>` tags within a slide's Markdown to apply CSS rules scoped to that specific slide.

```markdown
# Slide with Custom Styles

<style>
h1 {
  color: purple;
}
.custom-class {
  font-style: italic;
}
</style>

This <span class="custom-class">text</span> is italic.
```

## Global Styles

Create a `./style.css` or `./styles/index.ts` file in your project root to add global CSS rules affecting all slides. 