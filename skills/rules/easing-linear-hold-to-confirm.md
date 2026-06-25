---
id: easing-linear-hold-to-confirm
category: timing-functions
priority: MEDIUM
---

# easing-linear-hold-to-confirm

Linear easing is valid for "hold to confirm/delete" interactions where
the progress bar is explicitly visualizing the passage of time.
The constant speed signals duration intentionally — the user needs to feel time passing.

**Pass:**
```css
.hold-progress {
  transition: width 2000ms linear;
}
```

**Fail:**
```css
.hold-progress {
  transition: width 2000ms ease-out; /* misrepresents time passage */
}
```
