# Protocol Map

Use this file when protocol facts actually affect implementation choices.

## Stable implementation facts

- Zcash has transparent and shielded value pools, and sends can move between them.
- The classic user-facing transaction classes are transparent, shielding, deshielding, and fully shielded.
- Shielded transfers hide more transaction data, but fees remain visible.
- Coinbase rewards interact with special shielding rules; operational or wallet flows that touch mined funds need different handling.
- Pool totals are tracked at the node level via `getblockchaininfo`, including monitored value-pool state.

## Standard explanation frame

1. what problem the feature solves
2. what the network verifies
3. what is hidden
4. what remains visible
5. which node, wallet, or UX constraint follows from that

## Important contrasts

- transparent vs shielded
- shielding vs deshielding
- protocol behavior vs wallet UX
- node truth vs what a third-party wallet or service currently exposes
