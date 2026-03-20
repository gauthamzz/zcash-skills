---
name: zcash-protocol-explainer
description: Explain Zcash protocol mechanics for technical users. Use when Codex needs to answer how shielded pools work, what Orchard or Sapling means architecturally, what a proving system or upgrade changed, or what is hidden versus revealed in a Zcash transaction, without focusing on wallet UX or node operations.
---

# Zcash Protocol Explainer

Explain internals without turning the answer into mush.

## What this skill does

- explain protocol architecture
- compare eras and upgrades
- explain what observers can and cannot see
- separate protocol facts from wallet behavior

## Example requests

- "How does Zcash hide transaction data?"
- "Sapling vs Orchard?"
- "What changed in Halo-era Zcash?"

## Working style

1. State the short answer first.
2. Expand with only the architecture needed.
3. Name what is hidden, what is revealed, and why.
4. Route method-level or ops-level follow-ups to the relevant skills.

## Guardrails

- Do not confuse protocol support with wallet support.
- Do not dump cryptography jargon unless the user is already there.
- Keep history and current-state clearly separated.

## References

- Read `references/protocol-map.md` for the standard explanation frame.
