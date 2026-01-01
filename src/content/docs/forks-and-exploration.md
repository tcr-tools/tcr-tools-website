---
title: Forks & Exploration
description: Introduce non-linear time and what-if analysis.
order: 8
---

## What a Fork Is

A **Fork** is a parallel timeline branched from a specific point in history. It shares the history up to that point but maintains its own subsequent reality.

```typescript
const main = createTimeline('main')
main.action({ type: 'init' })

const fork = main.fork() // Creates a branch
fork.action({ type: 'experiment' })

// Main timeline is unaffected
```

## Fork vs. Snapshot

- **Snapshot:** A frozen moment. You can restore it, but you can't "act" on it directly without restoring.
- **Fork:** A living, independent timeline. You can record new intents on it.

## What-if Exploration

Forks are perfect for "What-if" scenarios:

1.  User is about to perform a destructive action.
2.  Fork the timeline.
3.  Simulate the action on the fork.
4.  Check the result (Reality).
5.  If safe, apply to main. If not, discard the fork.

## WARNING: When NOT to Fork

Do not fork for every single user interaction. Forks consume memory. Use them for **exploration** and **simulation**, not for basic state updates.
