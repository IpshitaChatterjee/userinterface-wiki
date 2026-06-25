---
id: animate-user-feedback
category: animation-principles
priority: HIGH
---

# animate-user-feedback

Animate responses to direct user actions to provide feedback and continuity.
State changes that have visual consequences (loading, success, error, expand)
benefit from animation. Skip animation when speed matters more than smoothness.

**Fail:**
```tsx
<button onClick={handleSubmit}>
  {isLoading ? <Spinner /> : 'Submit'} // Jarring state swap
</button>
```

**Pass:**
```tsx
<motion.button
  onClick={handleSubmit}
  animate={{ opacity: isLoading ? 0.6 : 1 }}
  transition={{ duration: 0.15 }}
>
  {isLoading ? <Spinner /> : 'Submit'}
</motion.button>
```
