---
title: Runtime Lifecycle
description: Explain ownership and cleanup.
order: 12
---

Understanding when to create and destroy timelines is key to avoiding memory leaks.

## Creating Timelines

Create a timeline when a logical unit of work begins.

- **Global SPA:** One root timeline initialized at app start.
- **Form Wizard:** Create a timeline when the modal opens.
- **Tabbed Interface:** One timeline per tab.

```typescript
const timeline = createTimeline('session-1')
```

## Disposing Timelines

When a timeline is no longer needed (e.g., closing a tab), **dispose** of it.

```typescript
timeline.dispose()
```

Disposing ensures:

- Subscriptions are unsubscribed.
- Memory in the Hot Tier is freed.
- Connection to DevTools is severed.

## Subscriptions

You can subscribe to changes in Reality.

```typescript
const unsubscribe = timeline.subscribe((newReality) => {
  render(newReality)
})

// Later
unsubscribe()
```

## Failure Modes

- **Storage Quota Exceeded:** If IndexedDB is full (Warm Tier), TCR will emit a warning but keep the Hot Tier functioning.
- **Serialization Error:** If you attempt to put non-serializable data into an intent (like a function or DOM node), TCR will throw explicitly.
