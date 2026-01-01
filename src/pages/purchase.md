---
layout: ../layouts/PageLayout.astro
title: Purchase License | TCR
---

<main class="py-24 pt-48 px-6 min-h-screen">
  <div class="max-w-3xl mx-auto prose prose-invert prose-headings:font-sans prose-code:font-mono prose-a:text-primary">

# Purchase a TCR License

## Commercial Licensing

TCR is a **licensed** developer tool for use in commercial projects.
Find out how the license purchasing process works below.

---

## How Purchasing Works

1. Select the plan that fits your needs from the pricing page.
2. Once payment is complete, you will receive a **license key**.
3. Add the license key to your project to start using TCR commercially.

---

## License Activation

License activation can be done using one of the following methods.

### Via CLI

```bash
tcr activate <LICENSE_KEY>
```

### Via Environment Variable

```bash
export TCR_LICENSE_KEY=<LICENSE_KEY>
```

or

```env
TCR_LICENSE_KEY=your-license-key
```

The runtime automatically detects the license.

---

## License Scope

- The license is **project-based**.
- For the same project, it can be used across:

  - local development
  - CI / test environments
  - production
    environments simultaneously.

- Distributing source code is **permitted** under the license, but the license key must be kept secret.

---

## Payment & Delivery

- Payments are processed via a secure payment infrastructure.
- After payment:

  - The license key is delivered via email.
  - No manual activation process is required.

> We are currently in early access.
> For some plans, the license key may be delivered manually.

---

## Refund Policy

- A refund can be requested within **14 days** of purchase.
- The license key will be revoked and the fee refunded.
- Refunds are not issued in cases of abuse or license violation.

---

## Need Help or Enterprise Licensing?

For enterprise use, custom license terms, or invoicing:

**[contact@tcr.tools](mailto:contact@tcr.tools)**

---

## Summary

- Deterministic debugging and temporal tooling are critical infrastructure for commercial projects.
- A TCR license allows you to use this infrastructure safely and sustainably.
- The purchasing and activation process is simple and transparent.

  </div>
</main>
