# App Development

Use this file when the user is building a Zcash-facing product rather than asking for protocol theory alone.

## Canonical components

- `zcashd`: the original C++ full node; still widely referenced, but operationally constrained by release support windows and deprecation pressure
- Zebra: the Rust full node from Zcash Foundation; relevant for new deployments, OpenAPI-described RPC workflows, and regtest/testnet work
- `lightwalletd`: the bandwidth-efficient backend used by mobile-friendly shielded light wallets such as Zashi and Ywallet
- wallet SDKs: `zcash-android-wallet-sdk`, `zcash-swift-wallet-sdk`, and `zcash-light-client-ffi`
- `zcash-stack`: a Helm chart that deploys `zcashd`, Zebra, `lightwalletd`, Caddy, and `dnsseeder` as one infrastructure package

## Common build targets

- wallet app
- payment flow
- portfolio or monitoring dashboard
- backend service that inspects chain state
- transaction construction and submission service
- lightwalletd-backed mobile or web wallet support layer

## Standard architecture questions

1. does the feature need a full node, `lightwalletd`, or just RPC-backed read access
2. where does signing happen
3. what address, receiver, or pool assumptions exist
4. what privacy assumptions does the UI imply
5. what happens when wallet or node support lags the protocol story
6. what needs to be tested before production

## Useful answer shape

1. state the product shape
2. identify the node, RPC, or `lightwalletd` dependency
3. identify the wallet and signing boundary
4. identify the compatibility, privacy, and failure risks
