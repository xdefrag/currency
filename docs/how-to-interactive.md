# Interactive Elements

## Draggable Elements (`v-drag`)

Make elements draggable within the slide.

- **Directive:** Add `v-drag` to an HTML element. Optionally provide a unique ID string `v-drag="'my-element-id'"` to persist the position in frontmatter.

  ```html
  <img src="logo.png" v-drag="'logo'" class="w-20 h-20">
  ```

- **Component:** Wrap content with `<v-drag>`.

  ```html
  <v-drag class="p-4 border rounded">
    Drag this container!
  </v-drag>
  ```

- **Positioning:** Double-click draggable elements in dev mode to visually adjust their position. Positions are saved in the slide's frontmatter (e.g., `dragPos: { logo: ... }`).
- **Draggable Arrow:** Use `<v-drag-arrow>` to create draggable arrows.

## Monaco Editor

Embed the Monaco Editor (used in VS Code) for interactive code editing or display.

- **Read-only Editor:** Add `{monaco}` to a code block fence.

  ```markdown
  ```ts {monaco}
  // Read-only Monaco editor
  const message = "Hello";
  ```
  ```

- **Runnable Editor:** Add `{monaco-run}` to allow executing the code within the slide.

  ```markdown
  ```ts {monaco-run}
  // Runnable Monaco editor
  console.log('Executed in Slidev!');
  ```
  ```

- **Diff Editor:** Add `{monaco-diff}` to show a diff view.

  ```diff {monaco-diff}
   // Monaco diff editor
  - const a = 1;
  + const a = 2;
  ```

- **Configuration:** Customize Monaco options globally in `package.json` or `vite.config.ts` under `slidev.monaco` or per-block, e.g., `{ monaco: { readOnly: true } }`. 