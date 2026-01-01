---
title: Mental Model
description: Install the correct mental model before any code.
order: 2
---

> "If this model makes sense, continue. If not, TCR is not the right tool."

## State vs. Time

Traditional state management asks: **"What is the value right now?"**
TCR asks: **"How did we get here, and where else could we go?"**

## Intent vs. Event

- An **Event** is something that happened (passive). e.g., "User clicked button".
- An **Intent** is a meaningful desire to change the system (active). e.g., `START_CHECKOUT_FLOW`.
- TCR records **Intents**. Intents capture the _why_, not just the _what_.

## Timeline vs. Log

A **Log** is a static list of past events. You read it.
A **Timeline** is a navigable territory. You move through it. You can jump back, fork off a new path, or replay it.

## Resolution vs. Mutation

In Redux or Zustand, you **mutate** state directly (or via reducers).
In TCR, you **resolve** intents. An intent might be:

- **Recorded:** Accepted and applied.
- **Superseded:** Replaced by a newer, more relevant intent (e.g., rapid typing).
- **Discarded:** Rejected because it conflicts with logic.

## Exploration vs. Transaction

Backend transactions commit or rollback. They are binary.
Frontend interaction is an **exploration**. Users change their minds. They undo. They retry. TCR embraces this non-linear nature.
