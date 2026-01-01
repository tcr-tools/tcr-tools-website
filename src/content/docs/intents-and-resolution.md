---
title: Intents & Resolution
description: Explain how meaning is recorded in TCR.
order: 6
---

## What an Intent Represents

An **Intent** is an immutable record of "what was attempted". Unlike a Redux action which is typically a command to change state, a TCR Intent is a historical fact.

```typescript
{
  id: 'intent_123',
  type: 'SAVE_DOCUMENT',
  payload: { title: 'Draft' },
  timestamp: 1704067200000
}
```

## Resolution Types

When an Intent enters the timeline, the **Coordinator** decides its fate.

1.  **Record**: The intent is accepted. Reality is updated.
2.  **Supersede**: A newer intent replaces an older one (e.g., a "Save" intent superseding a previous "Save" that hasn't finished).
3.  **Discard**: The intent is rejected (e.g., validation failure).
4.  **Defer**: The intent waits for a condition (e.g., waiting for network).

## Why Resolution Exists

In a complex async world, not every action should result in a state change _immediately_ or _additively_. Resolution allows us to model:

- Debouncing (supersede)
- Optimistic updates (record -> then potentially invalidate)
- Race condition handling (ordering guarantees)

## Determinism Guarantees

TCR guarantees that given the same sequence of Intents, the resulting Reality will always be identical. This is crucial for **Prove** tier features like audit logs and replay.
