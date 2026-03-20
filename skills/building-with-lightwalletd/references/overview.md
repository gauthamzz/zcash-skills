# Overview

`lightwalletd` is a bandwidth-efficient backend service for Zcash light wallets such as Zashi and Ywallet.

## Core backend facts

- it is designed to support mobile-friendly shielded wallets
- it typically sits on top of `zcashd`
- the backing `zcashd` instance must be configured with `txindex=1`, `lightwalletd=1`, and `experimentalfeatures=1`
- after changing those settings, `zcashd --reindex` is required once for them to take effect

## Runtime behavior

- `lightwalletd` caches blocks from Sapling activation forward
- first startup can spend roughly an hour warming that cache
- startup is much faster after the cache exists
- corruption is detected and automatically triggers block re-download from the affected height

## Good answer shape

1. identify the backend topology
2. identify the `zcashd` dependency
3. identify cache and startup expectations
4. identify what the client SDK needs to connect
