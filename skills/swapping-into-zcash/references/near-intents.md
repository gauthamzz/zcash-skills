# NEAR Intents

Use this file when the user explicitly mentions NEAR Intents, 1Click API, CrossPay, or Zodl-like swap execution.

## Relevant pattern

The NEAR Intents 1Click model is:

```text
request quote -> receive deposit instructions -> send deposit -> optionally submit tx hash -> poll status -> receive destination asset or refund
```

## Important concepts to preserve

- preview quotes and committed deposit instructions are different states
- deposit instructions are typically time-bound
- status polling matters because execution is asynchronous
- terminal outcomes include success, refund, incomplete deposit, and failure

## Zcash framing

- treat NEAR Intents as cross-chain execution infrastructure, not native Zcash functionality
- if Zodl uses a swap path powered by NEAR Intents, separate the wallet UX from the execution rail
- if the user wants shielded ZEC at the end, explain where shielding starts and what happened before that point
