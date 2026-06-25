---
id: easing-avoid-ease-in
category: timing-functions
priority: HIGH
---

# easing-avoid-ease-in

`ease-in` starts slowly and ends fast. It feels unnatural for UI because
the slowness at the start reads as unresponsive. Avoid it entirely.

**Fail:**
```css
.dropdown {
  transition: opacity 200ms ease-in;
}
```

**Pass:**
```css
.dropdown {
  transition: opacity 200ms cubic-bezier(0.22, 1, 0.36, 1); /* ease-out */
}
```
