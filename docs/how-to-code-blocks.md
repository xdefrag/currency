# Code Blocks

Slidev uses [Shiki](https://shiki.style/) for syntax highlighting.

## Basic Highlighting

Use standard Markdown fenced code blocks with a language identifier.

```markdown
```ts
console.log('Hello, Slidev!');
```

## Line Highlighting

Append `{...}` after the language identifier to highlight specific lines.

- ` {1,3}`: Highlight lines 1 and 3.
- ` {1-3}`: Highlight lines 1 to 3.
- ` {1,3-5}`: Highlight line 1 and lines 3 to 5.
- ` {all}`: Initially highlight all lines.
- ` {all|1-2|3|all}`: Animation sequence for highlighting on clicks.

```markdown
```ts {1,3-5|all}
function greet(name: string) {
  // This is line 2
  console.log(`Hello, ${name}!`); // Line 3
  // Line 4
}
// Line 6
```
```

## Twoslash Integration

Add `twoslash` within the `{}` to enable TypeScript type information on hover.

```markdown
```ts {twoslash}
import { ref } from 'vue'
const count = ref(0);
count.value = 'hello'; // Type error will be shown
```
```

## External Code Snippets

Embed code from external files using the `<<<` syntax.

```markdown
<<< @/path/to/your/code.ts
```

- `@/`: Refers to the project root.
- Append `#regionName` to import a specific named region (using `#region` / `#endregion` comments in the source file).
- Append `{lines}` to show line numbers.

## Shiki Magic Move

Wrap multiple code blocks with ` ````md magic-move` to animate changes between them.

````markdown
````md magic-move
```js
// Step 1
let a = 1;
```

```js
// Step 2
let a = 1;
let b = 2;
```
````
```` 