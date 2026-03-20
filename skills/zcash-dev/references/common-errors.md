# Common Errors

Use this file when the user has a real build problem rather than a greenfield design question.

## Frequent failure patterns

- assuming the wallet supports the receiver or flow the product assumes
- using protocol terminology as if it were the same as product capability
- building a backend that depends on richer state than its RPC source reliably exposes
- designing a privacy-sensitive flow without surfacing user-visible caveats
- treating node health, wallet support, and transaction submission as one system boundary

## Good debug sequence

1. restate the intended product behavior
2. identify the actual failing layer
3. identify what assumption broke
4. narrow the fix to that layer before redesigning everything
