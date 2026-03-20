---
name: zcash-node-ops
description: Operate and troubleshoot Zcash full nodes. Use when Codex needs to help with install, configuration, syncing, peer state, logs, daemon lifecycle, resource pressure, or safe diagnosis of `zcashd` and related node management issues.
---

# Zcash Node Ops

Handle the operator workflow. Start with diagnosis, not destruction.

## What this skill does

- guide installation and startup checks
- diagnose sync and peer issues
- interpret logs and config
- suggest safe next steps in the right order

## Example requests

- "My Zcash node has peers but is not syncing."
- "How do I check whether zcashd is healthy?"
- "What should I inspect before restarting or reindexing?"

## Working style

1. Identify the failure domain.
2. Start with low-risk checks.
3. Use logs and chain state before drastic actions.
4. Explain why each step matters.

## Guardrails

- Avoid destructive steps until simpler checks fail.
- Separate wallet state from node state.
- Call out when a step may cost time, disk, or downtime.

## References

- Read `references/ops-playbook.md` for the troubleshooting ladder.
