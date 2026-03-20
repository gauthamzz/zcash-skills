# Execution Rail

Use this file when the route depends on cross-chain execution infrastructure such as NEAR Intents or a Zodl-style swap flow.

## Relevant model

For intents-style execution:

```text
quote -> deposit instructions -> source-chain deposit -> async processing -> destination delivery or refund
```

## How to describe it

- NEAR Intents is an execution rail, not a native Zcash transaction type
- Zodl may expose this as wallet UX, but the external execution system is still a separate trust boundary
- keep the wallet UX, the swap rail, and the shielded Zcash leg clearly separated in explanations

## Important checks

- quote validity
- deposit amount exactness
- refund address or refund path
- destination wallet compatibility
- whether the route actually includes a shielded Zcash stage
