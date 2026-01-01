---
title: Timeline Navigation
description: Teach time travel properly.
order: 7
---

Moving through time is identifying **where** you are in the causal chain.

## Cursor Semantics

The **Cursor** points to the last applied Intent.

- If Cursor is at the end (Head), you are in "Live" mode.
- If Cursor is in the past, you are in "Inspection" mode.

## Undo vs. Jump

- **Undo (`timeline.undo()`)**: Moves the cursor one step back.
- **Jump (`timeline.jumpTo(id)`)**: Moves the cursor to a specific intent ID.

## Forward Traversal

- **Redo (`timeline.redo()`)**: Moves the cursor one step forward.
- **Play**: You can programmatically traverse forward to replay history.

## Boundaries and Limits

- You cannot undo past the beginning (Initial State).
- You cannot redo past the Head.
- In **Bounded Memory** mode (Free Tier), history may be truncated. If the start of the timeline is pruned, you cannot traverse before that point.
