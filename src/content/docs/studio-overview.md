---
title: Studio Overview
description: Explain DevTools without marketing.
order: 13
---

The **TCR Studio** is a standalone debugging tool that connects to your runtime.

## Read-Only Observer Rule

**The Inspector never mutates the Runtime.**
It is strictly an observer. It can visualize, request history, and display forks, but it cannot inject intents into your application. This ensures that debugging never introduces Heisenbugs.

## Timeline View

The primary view is a "swimlane" visualization:

- **X-Axis:** Time (Sequence).
- **Y-Axis:** Lanes (User Input, System Events, Network).

## Inspector Panel

Clicking any Intent opens the Inspector.

- **Payload:** The data carried by the intent.
- **Resolution:** Was it recorded? Superseded?
- **State Before/After:** The reality change caused by this intent.

## Causality View

Visualizes the "Why?" graph. Helpful for debugging "Why did this update happen?" or "Why was this request cancelled?".

[Open Studio](/studio)
