# Integrations

Use this file when the user is building around existing Zcash-facing product patterns rather than a generic wallet or RPC feature.

## Relevant current examples

- Zodl is the flagship Zcash mobile wallet brand and is relevant when the user asks about wallet-product patterns, user-facing ZEC flows, or product expectations around shielded UX.
- NEAR Intents is relevant when the user asks about cross-chain swaps or payment flows that move between shielded ZEC and assets on other ecosystems.

## How to frame NEAR Intents in Zcash work

- treat it as a cross-chain execution and settlement layer, not as "native Zcash functionality"
- separate the Zcash-side send or funding action from the downstream solver-driven execution path
- keep privacy claims narrow and explicit because cross-chain flows can expose more than a pure shielded ZEC transfer

## Good answer shape

1. identify the user-facing flow
2. separate Zcash-native behavior from cross-chain orchestration
3. state what the external system is responsible for
4. state the privacy and trust caveats
