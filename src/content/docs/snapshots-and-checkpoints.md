---
title: Snapshots & Checkpoints
description: Explain immutability and safety.
order: 10
---

## Snapshot Semantics

A **Snapshot** in TCR is a deep clone (or structural sharing copy) of the Reality at a specific Cursor. It is **immutable**.

```typescript
const snap = timeline.snapshot()
```

## Momentary Checkpoints

Use snapshots to save "safe points" before a risky operation (like a large batch update or network sync).

## Restoring from Snapshots

You can "reset" reality to a snapshot. Note that this is different from time-traveling (undo). Resetting to a snapshot effectively "forgets" the history that happened after it (unless you are on a fork).

## Exploration Safety

Because snapshots are immutable, you can pass them to calculation functions without fear of them being mutated by the view layer.
