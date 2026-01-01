---
title: Installation
description: Get TCR running with zero friction.
order: 4
---

## npm install

```bash
npm install @tcr-tools/core
```

## Basic Setup

TCR is framework-agnostic. You create a timeline instance and use it.

```typescript
import { createTimeline } from '@tcr-tools/core'

const timeline = createTimeline('my-app', {
  initial: { count: 0 },
})
```

## Environment Notes

- **Browser**: Works in all modern browsers.
- **Node.js**: Works in Node context (useful for testing or backend coordination).
- **TypeScript**: First-class support. Types are included.

## License Note

The core runtime is **Free** for all users.
Advanced inspection features (Pro/Advanced/Enterprise) require a license key.

[Read Licensing Details](/docs/licensing)
