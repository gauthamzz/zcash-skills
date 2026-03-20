---
name: zcash-rpc-reference
description: Map Zcash tasks to the right RPC methods and method families. Use when Codex needs to translate an operator or wallet goal into likely `zcash-cli` or JSON-RPC usage, identify the relevant method family, or explain common RPC caveats around chain state, wallet state, addresses, transactions, and node administration.
---

# Zcash RPC Reference

Turn intent into the likely method path.

## What this skill does

- map tasks to RPC families
- explain method choice at a practical level
- surface likely prerequisites and gotchas
- stop the agent from spraying random commands

## Example requests

- "Which RPC should I use to inspect chain progress?"
- "How do I map address balance checks to Zcash RPC?"
- "What should I call to inspect peers or mempool state?"

## Working style

1. Restate the job in operational terms.
2. Identify the likely method or small method set.
3. State prerequisites.
4. State one or two caveats.

## Guardrails

- Do not fake exact field-level output when version details matter.
- Route protocol explanations to `../zcash-protocol-explainer/`.
- Route runtime diagnosis to `../zcash-node-ops/`.

## References

- Read `references/task-map.md` for common task-to-method patterns.
