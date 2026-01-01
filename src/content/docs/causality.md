---
title: Causality
description: Answer “why did this happen?”
order: 9
---

TCR tracks not just **what** happened, but **why**.

## Causality vs. Sequence

- **Sequence:** Event A happened before Event B.
- **Causality:** Event A _caused_ Event B.

In traditional systems, you arguably see sequence (logs). In TCR, the Coordinator tracks causality.

## Supersede Chains

When an Intent is superseded, it forms a chain.
`Search(A)` -> superseded by `Search(AB)` -> superseded by `Search(ABC)`.

TCR allows you to inspect this chain to understand why the final reality is `Search(ABC)` and why the network request for `Search(A)` was cancelled.

## Invalidation

An intent can be **Invalidated** by a later intent.
Example: `AuthSuccess` might invalidate a pending `RetryLogin` intent. This is tracked explicitly in the graph.

## Reading Causality Graphs

In the **Studio**, causality is visualized as a directed graph. You can click any Resolution to see its ancestors (causes) and descendants (effects).
