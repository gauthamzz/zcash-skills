# Ops Playbook

## Failure buckets

- install or build issue
- daemon not starting
- sync stalled
- no peers or unstable peers
- config mismatch
- disk or resource pressure
- `lightwalletd` dependency or frontend issue on top of a node

## Safe ladder

1. confirm process state
2. inspect recent logs
3. inspect relevant config
4. inspect chain progress and peer state
5. only then consider restart, rescan, or reindex

## Node-stack notes

- `lightwalletd` depends on a healthy underlying node and can require `zcashd` settings such as `txindex=1`, `lightwalletd=1`, and `experimentalfeatures=1` in relevant setups
- `lightwalletd` caches blocks locally and can spend significant time rebuilding or rechecking that cache after corruption or first startup
- `zcash-stack` is relevant when the user is deploying multiple Zcash services together, not just a standalone node
