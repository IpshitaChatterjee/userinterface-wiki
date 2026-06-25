---
id: animate-enter-exit-spatial
category: animation-principles
priority: HIGH
---

# animate-enter-exit-spatial

Animate enter and exit transitions for elements that establish spatial
relationships in the UI. Without motion, users lose the mental model
of where things came from and where they went.

Good candidates: modals, drawers, dropdowns, popovers, toasts.

**Fail:**
```tsx
{isOpen && <Modal />} // Appears/disappears instantly — no spatial context
```

**Pass:**
```tsx
<AnimatePresence>
  {isOpen && (
    <motion.div
      initial={{ opacity: 0, y: 8 }}
      animate={{ opacity: 1, y: 0 }}
      exit={{ opacity: 0, y: 8 }}
    />
  )}
</AnimatePresence>
```
