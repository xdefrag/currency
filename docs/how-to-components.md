# Using Vue Components

Slidev allows embedding Vue components directly within Markdown for interactive elements.

## Built-in Components

Slidev provides several built-in components:

- `<Tweet id="...">`: Embeds a tweet.
- `<Youtube id="...">`: Embeds a YouTube video.
- `<Toc ...>`: Generates a Table of Contents (see `how-to-navigation-toc.md`).
- `<Link ...>`: Creates links.
- `<Code ...>`: Renders code blocks.
- `<Mermaid ...>`: Renders Mermaid diagrams (see `how-to-diagrams.md`).
- ... and more. See [Built-in Components Docs](https://sli.dev/builtin/components.html).

```html
<Tweet id="1390115482657726468" scale="0.65" />
```

## Custom Components

Create your own Vue components (`.vue` files) inside the `./components/` directory in your project root. They will be automatically available for use in your Markdown.

**Example:** `./components/Counter.vue`

```vue
<script setup>
import { ref } from 'vue'

const props = defineProps({
  initial: {
    type: Number,
    default: 0,
  },
})

const count = ref(props.initial)
</script>

<template>
  <button @click="count++" class="px-2 py-1 rounded border border-gray-400">
    Count: {{ count }}
  </button>
</template>
```

**Usage in Markdown:**

```html
<Counter :initial="10" />
``` 