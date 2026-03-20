---
name: zcash-wallet-support
description: Practical Zcash wallet support for receiving, sending, backups, address compatibility, and privacy-safe user guidance. Use when Codex needs to help a normal user or support workflow choose a wallet path, explain what to verify before sending or receiving, handle seed and backup questions, or avoid common wallet privacy mistakes without drifting into full node operations.
---

# Zcash Wallet Support

Use this skill for real wallet support work, not generic crypto education.

## What this skill is for

- wallet choice and compatibility questions
- receive and send workflows
- backup and recovery guidance
- address and receiver confusion
- privacy caveats normal users actually need

## Use this when

- a user is trying to receive or send ZEC safely
- the user is confused about addresses, receivers, wallet support, or backups
- the task is support-oriented rather than developer-oriented

## Example requests

- "Which wallet should I use for everyday Zcash?"
- "How do I receive ZEC without exposing more than I need to?"
- "What should I check before I send?"
- "What exactly do I need to back up?"
- "How does Zodl fit into normal Zcash wallet usage?"

## Default support flow

1. Identify the exact wallet job.
2. Give the shortest safe sequence.
3. Call out the main compatibility or privacy caveat.
4. Tell the user what to verify before acting.

## Workflow

1. Identify the wallet job.
2. Give the shortest safe path.
3. State the main risk or caveat.
4. Explain what the user must verify before acting.
5. Route node-backed issues to `../zcash-node-ops/` and product-implementation issues to `../zcash-dev/`.

## What good answers include

- what the user is trying to accomplish
- what can go wrong
- what to verify before send or receive
- what needs to be backed up or preserved
- whether the issue is really wallet UX, node state, or app implementation

## Guardrails

- Do not promise wallet feature support you have not verified.
- Do not present privacy as automatic.
- Do not bury custody or backup risk in soft language.
- Keep user-facing help concrete and check-list driven.

## References

- Read `references/wallet-patterns.md` for the standard support flow.
- Read `references/privacy-gotchas.md` when the user is about to assume wallet usage automatically preserves privacy.
- Read `references/recovery.md` when the user asks about seed phrases, migration, or backup material.
- Read `references/zodl.md` when the user asks specifically about Zodl, or when Zodl-specific wallet behavior is relevant.
