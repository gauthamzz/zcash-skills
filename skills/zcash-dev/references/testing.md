# Testing

Use this file when the user asks how to validate a Zcash-facing feature.

## Test buckets

- address parsing and validation
- receive and send flow validation
- RPC failure handling
- chain-state staleness and retry behavior
- wallet compatibility and fallback behavior
- `lightwalletd`-backed sync or cache behavior where relevant

## Good testing pattern

1. unit test parsing and task mapping
2. integration test RPC-backed flows
3. simulate unhappy paths around state drift, timeouts, and invalid inputs
4. test user-visible privacy warnings and compatibility checks
5. if using `lightwalletd`, test behavior during cache warmup or backend inconsistency
