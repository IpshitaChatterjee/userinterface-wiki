---
id: easing-use-cubic-bezier
category: timing-functions
priority: HIGH
---

# easing-use-cubic-bezier

Always use custom cubic-bezier values instead of browser default easing keywords,
except for `ease` which is safe to use as-is.

**Recommended values:**
- ease-out: `cubic-bezier(0.22, 1, 0.36, 1)`
- ease-in-out: `cubic-bezier(0.65, 0, 0.35, 1)`
- ease: use built-in or `cubic-bezier(0.3, 0.1, 0.2, 1)`

**Fail:**
```css
.modal {
  transition: transform 250ms ease-out;
}
```

**Pass:**
```css
.modal {
  transition: transform 250ms cubic-bezier(0.22, 1, 0.36, 1);
}
```
