# SOCIII SDK

**Build a Digital Worker. Own it. Earn from what you know.**

[SOCIII](https://sociii.ai) is a platform of **Digital Workers** — AI specialists built on the real rules and standards of a field (a title pro, a flight instructor, a nursing educator), governed by a rules engine, with every action written to an owned, tamper-evident record.

This repository is the **open SDK** for building those workers. The platform is closed; the worker you build is *yours*. The SDK is the receipt that proves it.

---

## What's here

| Path | What it is |
|---|---|
| [`CREATOR-SETUP.md`](./CREATOR-SETUP.md) | **Start here.** An AI-pilotable guide — paste it into ChatGPT or Claude and it walks you, one step at a time, from a blank computer to a published worker. You do **not** need to know how to code. |
| [`template/`](./template) | The worker-spec contract. Copy it, fill in the five files, open a PR. That folder *is* your worker. |
| [`sdk/`](./sdk) | `@sociii/sdk` — the JavaScript client for the SOCIII API (workers, vault, marketplace). |

## The worker is a folder

A SOCIII Digital Worker is defined by a small, human-readable spec — five files in [`template/`](./template):

- **`intent.md`** — what the worker does, who it's for, what success looks like, and what it is *not*.
- **`canvas-tabs.json`** — the panels your users see.
- **`service.js`** — the worker's functions, as *pure event proposals* (it proposes; the rules engine validates; events append — it never mutates directly).
- **`sample-data.js`** — fixtures so a first-time user sees something real, not an empty state.
- **`tests/assertions.md`** — the acceptance checks that must pass before it ships.

That's the contract. If it passes review, it becomes a live worker — published to the public marketplace, or kept private to your own business.

## Why the SDK is open but the platform isn't

Free the worker code; charge for the substrate that makes it valuable. The same model that built Red Hat and Hugging Face is the right model for AI workers. Open SDKs make the **creator** the parent of every worker — not the platform. We chose open.

The defensible part — the append-only owned record, the rules engine, the audit trail anchored on-chain — is the substrate, and it stays in the platform. The worker you author is yours to keep, port, and earn from.

## Install the client

```bash
npm install @sociii/sdk
```

```javascript
import Sociii from "@sociii/sdk";

const client = new Sociii();

// Browse the marketplace (no auth required)
const results = await client.marketplace.search("deal analyst");
console.log(results.workers);
```

See [`sdk/README.md`](./sdk/README.md) for the full client API.

## Become a creator

Creator access is **curated** — we onboard a small number of excellent builders at a time, so the marketplace stays high-signal. Tell us what you'd build: **creators@sociii.ai**, or apply at [sociii.ai/onboard/creator](https://sociii.ai/onboard/creator).

---

*SOCIII, Inc. · [sociii.ai](https://sociii.ai)*
