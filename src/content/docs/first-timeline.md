---
title: Create Your First Timeline
description: Your first success with TCR.
order: 5
---

Let's create a simple counter to understand the basics.

## 1. Create the Timeline

```typescript
import { createTimeline } from '@tcr-tools/core'

// Define your state shape
interface State {
  count: number
}

// Initialize
const timeline = createTimeline<State>('counter', {
  initial: { count: 0 },
})
```

## 2. Record Intents

Instead of checking `state.value`, we record an **action** (intent).

```typescript
// Record an increment intent
timeline.action({ type: 'increment', payload: 1 })

console.log(timeline.state.count) // 1
```

## 3. Undo / Redo

This is where TCR shines. History is free.

```typescript
timeline.action({ type: 'increment', payload: 1 }) // count: 2

timeline.undo()
console.log(timeline.state.count) // 1

timeline.redo()
console.log(timeline.state.count) // 2
```

## 4. Reading State

`timeline.state` is a **projection**. It calculates the result of all valid intents up to the current cursor.
