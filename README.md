# Flex Start CSS

A minimal, utility-first CSS class library for flexbox layouts. This repository includes:

- `flex-start.css` — core flexbox utility classes
- `demo.html` — interactive demo displaying how the classes behave
- `documentation.html` — full component reference with practical examples
- `README.md` — this file

---

## Quick start

```html
<link rel="stylesheet" href="flex-start.css">

<div class="flex wrap justify-between items-center" style="height: 120px;">
  <div>Box 1</div>
  <div>Box 2</div>
  <div>Box 3</div>
</div>
```

Add class modifiers to your `.flex` container for direction, wrapping, alignment, grow/shrink, and item control.

---

## Class categories and behavior

### 1. Container display

- `.flex` → `display: flex`
- `.flex.inline` → `display: inline-flex`

### 2. Wrap behavior

- `.flex.wrap` → `flex-wrap: wrap`
- `.flex.wrap-reverse` → `flex-wrap: wrap-reverse`

### 3. Flex direction

- `.flex.reverse` → `flex-direction: row-reverse`
- `.flex.column` → `flex-direction: column`
- `.flex.column.reverse` → `flex-direction: column-reverse`

### 4. `align-items` (cross axis)

- `.flex.items-start` → `align-items: flex-start`
- `.flex.items-center` → `align-items: center`
- `.flex.items-end` → `align-items: flex-end`
- `.flex.items-stretch` → `align-items: stretch`

### 5. `justify-content` (main axis)

- `.flex.justify-start` → `justify-content: flex-start`
- `.flex.justify-center` → `justify-content: center`
- `.flex.justify-end` → `justify-content: flex-end`
- `.flex.justify-between` → `justify-content: space-between`
- `.flex.justify-around` → `justify-content: space-around`
- `.flex.justify-evenly` → `justify-content: space-evenly`
- `.flex.justify-stretch` → `justify-content: stretch`

### 6. `align-content` (multi-line cross axis)

- `.flex.content-start` → `align-content: flex-start`
- `.flex.content-center` → `align-content: center`
- `.flex.content-end` → `align-content: flex-end`
- `.flex.content-between` → `align-content: space-between`
- `.flex.content-around` → `align-content: space-around`
- `.flex.content-evenly` → `align-content: space-evenly`
- `.flex.content-stretch` → `align-content: stretch`

### 7. `align-self` (item-level overrides)

- `.self-start` → `align-self: flex-start`
- `.self-center` → `align-self: center`
- `.self-end` → `align-self: flex-end`
- `.self-stretch` → `align-self: stretch`

### 8. `flex-grow` helpers

- `.grow-0` … `.grow-6`

### 9. `flex-shrink` helpers

- `.shrink-0` … `.shrink-6`

---

## Visual examples (markdown style)

### Align-items

```html
<div class="flex items-center" style="height: 120px; border: 1px solid #aaa;">
  <div style="padding: 10px; background:#64b5f6; color:#fff;">A</div>
  <div style="padding: 10px; background:#42a5f5; color:#fff;">B</div>
  <div style="padding: 10px; background:#2196f3; color:#fff;">C</div>
</div>
```

`items-center` centers items vertically (cross axis).

### Justify-content

```html
<div class="flex justify-between" style="height: 100px; border: 1px solid #aaa;">
  <div style="padding: 10px; background:#67c23a; color:white;">Left</div>
  <div style="padding: 10px; background:#f56c6c; color:white;">Center</div>
  <div style="padding: 10px; background:#909399; color:white;">Right</div>
</div>
```

`justify-between` pushes children to edges with space in between.

### Align-content with wrap

```html
<div class="flex wrap content-space-between" style="height: 180px; border: 1px solid #aaa;">
  <!-- six child items -->
</div>
```

`content-between` spreads wrapped lines across the container height.

### Align-self override on item

```html
<div class="flex items-start" style="height: 120px; border: 1px solid #aaa;">
  <div class="self-end" style="padding: 10px; background:#2db7f5; color:white;">Overrides to end</div>
  <div style="padding: 10px; background:#67c23a; color:white;">Normal</div>
</div>
```

### Grow/shrink behavior

```html
<div class="flex" style="width: 450px; border: 1px solid #aaa;">
  <div class="grow-1" style="padding: 10px; background:#409eff; color:#fff;">grow-1</div>
  <div class="grow-2" style="padding: 10px; background:#67c23a; color:#fff;">grow-2</div>
  <div class="grow-3" style="padding: 10px; background:#f56c6c; color:#fff;">grow-3</div>
</div>
```

```html
<div class="flex" style="width: 310px; border: 1px solid #aaa;">
  <div class="shrink-0" style="width: 120px; padding: 10px; background:#f56c6c; color:#fff;">shrink-0</div>
  <div class="shrink-1" style="width: 120px; padding: 10px; background:#67c23a; color:#fff;">shrink-1</div>
  <div class="shrink-3" style="width: 120px; padding: 10px; background:#409eff; color:#fff;">shrink-3</div>
</div>
```

---

## Notes

- `<code>.flex.content-*</code>` works only when `.flex.wrap` is present and there are multiple lines.
- `<code>.self-*</code>` affects only the element itself consistent with the parent alignment context.
- Use `.grow-*` and `.shrink-*` for more expressive size rules in responsive interfaces.

---

## License

MIT License
