---
title: FAQ
description: Preempt confusion.
order: 15
---

## Is this a state manager?

No. It coordinates _intents_. It can work alongside Redux, Zustand, or simple React state. It manages the _timeline_ of changes, not just the current value.

## Can I replace Redux/Zustand with this?

Yes, you _can_ use it to hold state, but it is optimized for complex async flows, undo/redo, and auditing. For simple "is modal open" state, `useState` is fine.

## Is this backend safe?

Yes. The Core Runtime runs in Node.js and is often used for coordinating backend workflows or deterministic testing.

## Is this open source?

The **Core Runtime** is open source. The **Advanced Inspection** features overlaying it are proprietary and require a license. This keeps the runtime transparent but the commercial value protected.
