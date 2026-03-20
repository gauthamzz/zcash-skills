---
name: zcash-dev
description: End-to-end Zcash development playbook for agents building apps, services, wallet integrations, transaction flows, RPC-backed features, or developer tooling. Use when Codex needs to design or implement Zcash-facing product work, choose a technical approach, explain protocol constraints that affect implementation, or connect wallet UX, addresses, transactions, RPC, testing, and security into one development workflow.
---

# Zcash Dev

Use this skill for the work an agent actually does when building on Zcash: product architecture, wallet flows, address handling, transaction submission, RPC-backed services, testing, and implementation tradeoffs.

## What this skill is for

- app and service architecture
- wallet integration planning
- receive and send flow design
- chain-state and RPC-backed features
- developer tooling and testing strategy
- protocol constraints that matter to implementation

## Default decisions

1. Prefer the smallest architecture that can safely support the feature.
2. Keep wallet UX, signing, and node responsibilities clearly separated.
3. Treat RPC shape, receiver support, and wallet capability as version- and product-sensitive.
4. Push protocol deep dives into implementation-relevant terms, not academic exposition.

## Example requests

- "Build a Zcash wallet dashboard that shows balances and sends transactions."
- "Design the backend architecture for a Zcash payment service."
- "Map this product feature to Zcash addresses, receivers, RPC, and testing."
- "Explain the Zcash protocol details that matter for implementing this app."
- "Design a Zcash cross-chain swap or payment flow that uses NEAR Intents."

## Task classification

- wallet or product UX
- backend service or monitoring
- RPC-backed integration
- address and receiver handling
- transaction flow design
- testing and deployment readiness

## Workflow

1. Identify the build target: wallet app, backend service, monitoring tool, developer SDK, or integration layer.
2. Separate product UX concerns from protocol and node concerns.
3. Choose the smallest architecture that can safely support the feature.
4. Call out where wallet support, node support, RPC availability, and protocol semantics can diverge.
5. Route pure operational debugging to `../zcash-node-ops/` and user-facing wallet troubleshooting to `../zcash-wallet-support/`.

## Deliverable expectations

When implementing or planning, be explicit about:

- where chain state comes from
- where signing happens
- what address or receiver assumptions exist
- what happens on unsupported paths or stale state
- what should be tested before shipping

## What to load

- Read `references/app-dev.md` for app and service architecture patterns.
- Read `references/protocol-map.md` when protocol semantics affect product design.
- Read `references/testing.md` when the user needs a validation or QA strategy.
- Read `references/security.md` when the feature handles keys, signing, or high-value transaction flows.
- Read `references/common-errors.md` when the user is debugging mismatches between product expectations and Zcash behavior.
- Read `references/integrations.md` when the user asks about Zodl-style swap or cross-chain payment flows, including NEAR Intents.

## Guardrails

- Do not answer product implementation questions with abstract protocol trivia.
- Do not assume wallet support matches protocol capability.
- Do not recommend full-node complexity when a lighter architecture is enough.
- Keep version-sensitive RPC or feature assumptions explicit.
