---
title: Memory Model
description: Set expectations for performance and limits.
order: 11
---

TCR uses a tiered memory architecture to ensure it runs efficiently in the browser while scaling to thousands of intents.

## Bounded Memory Principle

We do not store history infinitely by default. The Hot Tier (active memory) is a **Binary Ring Buffer**.

## Storage Tiers

1.  **HOT TIER (Binary Ring Buffer)**

    - Fast, zero-copy access.
    - Stores the most recent N (e.g., 10,000) intents.
    - Struct-of-Arrays layout.

2.  **WARM TIER (IndexedDB / Compressed)**

    - When the Hot Ring Buffer fills, old intents spill here.
    - Asynchronous, compressed access.
    - ensures "History is never lost" without crashing the browser tab.

3.  **COLD TIER (Export)**
    - Full JSON dump of the timeline.
    - Used for forensic analysis and "Prove" tier exports.

## Trade-offs

- **Binary vs Object:** Binary storage is faster and smaller but requires defined schemas. Object storage is flexible but heavier.
- **Lazy Projection:** TCR computes Reality lazily. We don't store a copy of the state for every single intent; we replay the reducer over the history (optimized with snapshots).
