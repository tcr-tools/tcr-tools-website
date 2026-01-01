---
title: Licensing
description: Canonical licensing explanation.
order: 14
---

This document defines how **Temporal Coordination Runtime (TCR)** is licensed.

## Licensing Philosophy

TCR is a **runtime**, not a SaaS. Licensing reflects **how deeply time is inspected and controlled**.

- Observing time is free.
- Understanding causality requires a license.
- Producing proof requires stronger guarantees.

## License Tiers

### Free — Observe

**Purpose:** Understand what is happening.

- Core runtime
- Timeline recording
- Undo / redo
- Studio (read-only)
- Local-only operation

### Pro — Understand

**Purpose:** Understand **why** it happened.

- Causality graph
- Supersede / invalidate inspection
- Fork & what-if exploration
- Timeline comparison
- Offline replay

### Advanced — Prove

**Purpose:** Produce deterministic evidence.

- Deterministic replay guarantees
- Proof exports (checksums)
- Advanced DSL queries
- Forensic-grade inspection

### Enterprise — Control

**Purpose:** Infrastructure.

- Offline / air-gapped licensing
- Organization-wide licenses
- LTS

## Common Questions

**Can I use Free in production?**
Yes.

**Does Studio mutate runtime state?**
No.

[View Full Pricing](/pricing)
