---
name: private-cross-chain-transfer
description: Design, explain, or support wallet-to-wallet transfers that use a Zcash privacy leg across chains such as Solana, Base, and other EVM networks. Use when Codex needs to help a user move value from one wallet to another via a swap into ZEC, shielding or shielded holding, and optional swap-out flow, including NEAR Intents- or Zodl-style execution patterns, destination-wallet compatibility, refund paths, and the real privacy limits of the route.
---

# Private Cross-Chain Transfer

Use this skill for the actual high-value user job: move funds from one wallet on one chain to another wallet on another chain with a Zcash privacy segment in the middle.

## What this skill is for

- Solana wallet -> ZEC -> another wallet flow design
- Base or EVM wallet -> ZEC -> another wallet flow design
- support answers for "how do I move privately between wallets"
- agent-driven planning for quote, deposit, shielding, holding, and exit legs
- explanation of where privacy starts, stops, and leaks

## Quick start

| Use case | Start here |
|----------|------------|
| User asks how to move funds privately | `references/user-playbook.md` |
| Builder wants to automate or productize the flow | `references/agent-flow.md` |
| Swap and execution layer is NEAR Intents or Zodl-like | `references/execution-rail.md` |
| Privacy/trust caveats | `references/privacy-model.md` |

## Canonical flow

```text
Source wallet -> quote and deposit route -> swap into ZEC -> shielded hold or shielded send -> optional swap out -> destination wallet
```

## Example requests

- "I have SOL in one wallet and want to move to another wallet more privately."
- "Take funds from my Base wallet and land them in another wallet using Zcash as the privacy leg."
- "Design an agent workflow that routes from Solana to ZEC and then onward."
- "What parts of this cross-chain path are private versus public?"

## Workflow

1. Identify the source chain, source asset, destination chain, and destination wallet.
2. Determine whether the user wants to stop in ZEC or continue out to another chain.
3. Separate the route into legs: source-chain swap/deposit, Zcash entry, shielded leg, optional exit leg.
4. State what each leg exposes publicly and what each external service learns.
5. Explain quote expiry, deposit rules, refunds, and destination support before the user acts.
6. Route wallet-only issues to `../zcash-wallet-support/`, swap-engine specifics to `../swapping-into-zcash/`, and broader product work to `../zcash-dev/`.

## Critical knowledge

1. This is not "private end to end" by default.
2. The source-chain leg is generally public on the source chain.
3. The Zcash leg can provide stronger privacy if the flow actually enters and uses shielded ZEC.
4. The exit leg may reveal timing or linkage depending on how the user leaves Zcash.
5. External swap or intents infrastructure can see or infer more than a pure shielded transfer.

## References

- Read `references/user-playbook.md` for support-style answers.
- Read `references/agent-flow.md` for automation or agent-planned routes.
- Read `references/execution-rail.md` for NEAR Intents and Zodl-style execution framing.
- Read `references/privacy-model.md` for the real privacy boundary map.
