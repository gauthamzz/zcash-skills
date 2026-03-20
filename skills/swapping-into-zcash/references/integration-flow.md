# Integration Flow

Use this file when the task is to build or explain the swap system architecture.

## Typical lifecycle

```text
fetch quote -> present quote -> obtain deposit instructions -> user deposits source asset -> execution engine or solver processes -> monitor status -> deliver destination asset or refund
```

## Builder questions to answer

1. where does the quote come from
2. how long is it valid
3. what address or deposit instructions are time-bound
4. how is status tracked
5. what are the terminal states
6. how are partial deposits, failures, and refunds surfaced

## Product requirement

Do not hide the distinction between:

- quote preview
- committed quote or live deposit instructions
- pending execution
- success
- refund or failure
