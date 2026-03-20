---
name: zcash-overview
description: Route Zcash questions to the right depth and the right follow-on skill. Use when Codex needs to classify a Zcash request, decide whether the user needs beginner education, wallet help, protocol explanation, node operations, RPC guidance, or ecosystem context, or give a fast top-level orientation before going deeper.
---

# Zcash Overview

Route first. Answer second.

Use this skill when the agent needs to identify what kind of Zcash work is actually being asked for and avoid jumping into the wrong depth.

## What this skill does

- classify the request
- estimate user level
- give a short framing answer
- hand off to the right specialist skill

## Routing map

- beginner question -> `../zcash-beginners/`
- term or jargon question -> `../zcash-glossary/`
- wallet or address question -> `../zcash-wallet-guide/`
- protocol or privacy mechanics question -> `../zcash-protocol-explainer/`
- node install or troubleshooting question -> `../zcash-node-ops/`
- RPC or command mapping question -> `../zcash-rpc-reference/`
- orgs, grants, or project-landscape question -> `../zcash-ecosystem-map/`

## Example requests

- "What is Zcash and why does privacy matter?"
- "Which Zcash skill should handle this node sync problem?"
- "I need the short version first, then the technical version."

## Working style

1. Identify the job.
2. State the likely best skill.
3. Give one concise framing paragraph if helpful.
4. Route explicitly.

## Guardrails

- Do not invent detail that belongs in a more specific skill.
- Do not treat wallet UX, protocol internals, and ecosystem politics as the same domain.
- Keep the first answer short unless the user clearly wants depth.

## References

- Read `references/routing-guide.md` when the request spans multiple Zcash domains.
