---
title: Introduction
description: What TCR is, who it is for, and how to think about it.
order: 1
---

**Temporal Coordination Runtime (TCR)** is a framework-agnostic coordination layer for complex frontend applications. It treats UI behavior as **temporal exploration** rather than state management.

## What TCR Is

TCR is a **runtime** that sits between your user interactions and your application state. It provides a traversable history, causal tracking, and deterministic intent resolution.

## What Problems It Solves

- **Race Conditions:** By ordering intents deterministically.
- **"Why did this happen?":** By providing a causal graph of every change.
- **Complex Undo/Redo:** By treating history as a first-class citizen.
- **Debugging:** By allowing you to replay, fork, and inspect past states.

## What It Explictly Does NOT Solve

- It is **not** a state manager (like Redux or Zustand). It coordinates _intents_, not just values.
- It is **not** a persistent database. It is a client-side runtime.
- It is **not** a UI framework. It works with React, Vue, Svelte, or Vanilla JS.

## Where to Go Next

1.  **[Mental Model](/docs/mental-model)**: Understand the core philosophy (Crucial first step).
2.  **[Installation](/docs/installation)**: Add TCR to your project.
3.  **[First Timeline](/docs/first-timeline)**: Write your first code.
