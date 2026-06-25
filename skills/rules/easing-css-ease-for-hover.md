---
id: easing-css-ease-for-hover
category: timing-functions
priority: MEDIUM
---

# easing-css-ease-for-hover

Use CSS `ease` (not ease-out) for hover effects that transition color,
background-color, or opacity. Also appropriate for subtle animations like
button-to-checkmark transforms and toast/notification components.

`ease` is asymmetrical — starts faster than ease-in-out, ends slower —
which makes hover transitions feel snappy without being abrupt.

**Fail:**
```css
.button:hover {
  transition: background-color 150ms ease-out;
}
```

**Pass:**
```css
.button:hover {
  transition: background-color 150ms ease;
}
```
