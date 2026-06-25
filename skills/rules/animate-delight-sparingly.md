---
id: animate-delight-sparingly
category: animation-principles
priority: HIGH
---

# animate-delight-sparingly

Reserve delight animations for rare, meaningful interactions.
Never animate things users do 100+ times a day — it becomes friction, not delight.
Hover effects on frequently used nav items, close buttons, or tab switches
should be instant or near-instant.

**Fail:**
```tsx
// Navigation item used dozens of times per session
<motion.a
  whileHover={{ scale: 1.05, rotate: 2 }}
  transition={{ type: 'spring' }}
>
  Dashboard
</motion.a>
```

**Pass:**
```tsx
// Delight reserved for a rare, celebratory action
<motion.div
  animate={hasCompleted ? { scale: [1, 1.2, 1] } : {}}
  transition={{ duration: 0.4 }}
>
  🎉
</motion.div>
```
