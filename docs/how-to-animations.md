# Animations

## Click Animations (`v-click`)

Apply the `v-click` directive to elements to make them appear sequentially on clicks.

```html
<div v-click>Appears on first click</div>
<div v-click>Appears on second click</div>

<!-- Specify click order -->
<div v-click="3">Appears on third click</div>

<!-- Group elements to appear together -->
<ul v-click="[1, 4]">
  <li>Appears on first click</li>
  <li>Appears on first click</li>
  <li>Appears on fourth click</li>
</ul>

<!-- Hide initially, appear later -->
<div v-click.hide>Hidden initially, appears on click</div>
```

## After Click (`v-after`)

Use `v-after` to make an element appear *after* the corresponding `v-click` animation on the *same* element or its children finishes.

```html
<div v-click>
  Show first...
  <span v-after>...then show this</span>
</div>
```

## Marking Text (`v-mark`)

Highlight inline text elements on click using `v-mark`, powered by [Rough Notation](https://roughnotation.com/).

```html
<!-- Simple usage -->
<span v-mark>Highlight me</span>

<!-- Specify click order and style -->
<span v-mark.circle.orange="3">Circle on 3rd click</span>
<span v-mark.underline.red="4">Underline on 4th click</span>
```

Common styles: `underline`, `circle`, `box`, `strike-through`, `highlight`, `crossed-off`.
Colors: Standard CSS colors (e.g., `red`, `blue`, `#ff00ff`).

## Motion Animations (`v-motion`)

Create more complex animations using the `v-motion` directive, powered by [@vueuse/motion](https://motion.vueuse.org/).

```html
<div 
  v-motion
  :initial="{ x: -100, opacity: 0 }" 
  :enter="{ x: 0, opacity: 1, transition: { delay: 500 } }"
  :leave="{ x: 100, opacity: 0 }"
  :click-3="{ scale: 1.2 }" /* Animate on 3rd click */
>
  Animate me!
</div>
```

- `:initial`: State before entering.
- `:enter`: State when entering the viewport (or on first load).
- `:leave`: State when leaving the viewport.
- `:visible`: State while visible.
- `:hovered`: State on hover.
- `:click-[n]`: State after n-th click.
- Properties like `x`, `y`, `opacity`, `scale`, `rotate` can be animated.
- Customize `transition` options (duration, delay, type: spring/tween, etc.).

## Slide Transitions

Control the animation between slides using the `transition` frontmatter key.

```yaml
---
transition: slide-left # Slide in from the right
---
```

Common transitions: `fade`, `slide-left`, `slide-right`, `slide-up`, `slide-down`, `fade-out`, `zoom`, `none`.
See [Slide Transitions Docs](https://sli.dev/guide/animations#slide-transitions). 