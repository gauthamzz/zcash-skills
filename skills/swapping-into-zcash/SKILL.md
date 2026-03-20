---
name: swapping-into-zcash
description: Help users or builders design, explain, or troubleshoot flows that swap into Zcash or shielded ZEC. Use when Codex needs to answer how to swap from another chain into ZEC, build a swap widget or cross-chain payment flow that lands in Zcash, reason about NEAR Intents or Zodl-style swap UX, or explain the operational and privacy caveats of bridging or swapping into Zcash.
---

# Swapping Into Zcash

Use this skill for swap and bridge style flows that end in Zcash or shielded ZEC.

## What this skill is for

- user-facing "how do I swap into Zcash" support
- builder-facing swap widget or payment-flow design
- NEAR Intents and Zodl-style cross-chain routing
- quote, deposit, execution, status, and refund lifecycle explanation
- privacy and trust caveats specific to swap-based entry into Zcash

## Quick start

| Use case | Start here |
|----------|------------|
| User support | `references/user-flow.md` |
| Builder / product flow | `references/integration-flow.md` |
| NEAR Intents / Zodl pattern | `references/near-intents.md` |
| Safety and privacy caveats | `references/caveats.md` |

## Integration flow

```text
Quote -> Deposit instructions -> Deposit transaction -> Execution / solver processing -> Status tracking -> ZEC delivery or refund
```

## Example requests

- "How do I swap ETH into Zcash?"
- "Design a swap widget that lands users in ZEC."
- "Explain how Zodl swap flows relate to NEAR Intents."
- "What privacy risks exist when swapping into shielded ZEC?"

## Workflow

1. Identify whether the task is user support, product design, or backend integration.
2. Distinguish Zcash-native behavior from external swap or solver infrastructure.
3. Explain the quote, deposit, status, and refund lifecycle clearly.
4. State what trust, compatibility, and privacy assumptions the flow introduces.
5. Route wallet-only questions to `../zcash-wallet-support/` and broader product work to `../zcash-dev/`.

## Critical knowledge

1. A swap into Zcash is not the same thing as a native shielded transfer.
2. Cross-chain execution introduces external counterparties, solver logic, or bridge-like trust assumptions.
3. Refund paths, destination compatibility, and time-limited quotes matter as much as the happy path.
4. If the user expects shielded privacy at the end of the flow, explain where that begins and what was exposed before that point.

## References

- Read `references/user-flow.md` for end-user guidance.
- Read `references/integration-flow.md` for builder-facing architecture and lifecycle.
- Read `references/near-intents.md` when NEAR Intents or Zodl-style swap execution is relevant.
- Read `references/caveats.md` for safety, refund, compatibility, and privacy warnings.
