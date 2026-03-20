---
name: deploying-zcash-stack
description: Deploy the full Zcash ecosystem stack on Kubernetes using zcash-stack. Use when Codex needs to plan or implement a multi-service Zcash deployment including zcashd, Zebra, lightwalletd, Caddy, and dnsseeder, or when the user asks for a plug-and-play Zcash infrastructure deployment rather than a single-node setup.
---

# Deploying Zcash Stack

Use this skill when the user wants a real multi-service Zcash infrastructure deployment rather than a standalone node.

## What this skill is for

- `zcash-stack` Helm deployments
- Kubernetes-based Zcash infrastructure
- multi-service topologies that include nodes, wallet backends, and edge services
- planning how `zcashd`, Zebra, `lightwalletd`, Caddy, and `dnsseeder` fit together

## Example requests

- "Deploy the Zcash ecosystem on Kubernetes."
- "How does zcash-stack fit together?"
- "What services does zcash-stack include?"
- "Should I use zcash-stack or just run a node?"

## Workflow

1. Confirm that the user actually wants a multi-service deployment.
2. Identify which stack components are required.
3. Explain the service graph before giving deployment steps.
4. Keep stack deployment distinct from single-node troubleshooting.

## What to load

- Read `references/components.md` for the service inventory and role of each component.
- Read `references/when-to-use.md` for choosing between `zcash-stack`, standalone node ops, and `lightwalletd`-specific work.

## Guardrails

- Do not recommend Kubernetes complexity for a user who only needs one node.
- Do not treat `zcash-stack` as interchangeable with a single-node install.
- Make explicit which services are public-facing and which should stay internal.
