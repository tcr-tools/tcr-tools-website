---
title: Terminology
description: Short, precise definitions of key TCR concepts.
order: 3
---

## Timeline

The container for your application's temporal history. It holds the sequence of intents and manages the current position (cursor).

## Intent

A structured record of a user or system action. It contains a `type`, `payload`, `timestamp`, and unique `id`. It is an **Time-Traveller** object, not just data.

## Resolution

The process of deciding what to do with an Intent. It determines the resulting Reality.

## Reality

The projected state at the current cursor position. "State" implies a static value; "Reality" implies a dynamic projection that changes as you move through time.

## Fork

A parallel branch of history. Forking allows you to explore "what-if" scenarios without affecting the main timeline.

## Snapshot

A static copy of Reality at a specific point in time. Used for performance optimization and potential restoration points.

## Cursor

The pointer indicating the current position in the Timeline. Moving the cursor (Time Travel) instantly updates the Reality.

## Supersede

When a new Intent invalidates a previous one (e.g., a new search query making the previous network request irrelevant).

## Invalidate

To mark an Intent (and its effects) as no longer valid, often due to a later decision or external factor.

## Defer

To pause the resolution of an Intent until a specific condition is met (e.g., waiting for a network response).
