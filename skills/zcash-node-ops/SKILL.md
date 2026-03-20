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

## Use this when

- the user is running `zcashd` or related node infrastructure
- the problem is sync, peers, daemon health, config, or resource pressure
- the answer needs an operator-style checklist rather than protocol theory

## Example requests

- "My Zcash node has peers but is not syncing."
- "How do I check whether zcashd is healthy?"
- "What should I inspect before restarting or reindexing?"

## Default approach

1. Confirm process health before changing config.
2. Read logs before restarting.
3. Check peers and chain progress before suspecting corruption.
4. Treat reindex or rebuild as late-stage recovery, not step one.

## Working style

1. Identify the failure domain.
2. Start with low-risk checks.
3. Use logs and chain state before drastic actions.
4. Explain why each step matters.

## What to include in answers

- the symptom being tested
- the exact purpose of each check
- what result would confirm or eliminate a failure domain
- whether the next step risks downtime, disk usage, or long resync time

## Guardrails

- Avoid destructive steps until simpler checks fail.
- Separate wallet state from node state.
- Call out when a step may cost time, disk, or downtime.

## References

- Read `references/ops-playbook.md` for the troubleshooting ladder.
- Read `references/requirements.md` for hardware, networking, and deployment-minded guidance.
