# App Development

Use this file when the user is building a Zcash-facing product rather than asking for protocol theory alone.

## Common build targets

- wallet app
- payment flow
- portfolio or monitoring dashboard
- backend service that inspects chain state
- transaction construction and submission service

## Standard architecture questions

1. where does chain state come from
2. where does signing happen
3. what address or receiver compatibility matters
4. what privacy assumptions does the UI imply
5. what needs to be tested before production

## Useful answer shape

1. state the product shape
2. identify the node or RPC dependency
3. identify the wallet and signing boundary
4. identify the failure and compatibility risks
