# Ops Playbook

## Failure buckets

- install or build issue
- daemon not starting
- sync stalled
- no peers or unstable peers
- config mismatch
- disk or resource pressure

## Safe ladder

1. confirm process state
2. inspect recent logs
3. inspect relevant config
4. inspect chain progress and peer state
5. only then consider restart, rescan, or reindex
