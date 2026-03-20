---
name: building-with-lightwalletd
description: Build or integrate Zcash light-wallet backends and SDK-driven wallet flows using lightwalletd. Use when Codex needs to set up lightwalletd, connect Android or Swift wallet SDKs, reason about mobile-friendly shielded wallet architecture, configure the required zcashd settings behind lightwalletd, or debug cache, sync, and light-client integration issues.
---

# Building With lightwalletd

Use this skill when the job is specifically about the light-client stack rather than generic Zcash app architecture.

## What this skill is for

- deploying or configuring `lightwalletd`
- wiring mobile or desktop light-wallet clients to a backend
- working with the Zcash Android SDK, Swift SDK, or light-client FFI stack
- understanding `lightwalletd` cache, startup, and testing behavior
- debugging shielded light-wallet backend issues

## Example requests

- "Set up lightwalletd for local Zcash wallet development."
- "How do I connect an Android Zcash wallet app to a backend?"
- "What does lightwalletd need from zcashd?"
- "How should I test a shielded light-wallet flow locally?"

## Workflow

1. Decide whether the user needs backend deployment, SDK integration, or debugging.
2. Confirm whether the backend is `zcashd`-backed or part of a larger stack.
3. Make the `lightwalletd` boundary explicit: backend cache, gRPC interface, wallet SDK, and node dependency.
4. Call out where cache warmup, corruption recovery, or network switching changes behavior.

## What to load

- Read `references/overview.md` for the backend model and required `zcashd` settings.
- Read `references/sdks.md` for Android, Swift, and FFI wallet-client integration guidance.
- Read `references/testing.md` for local developer and integration-test workflows.

## Guardrails

- Do not present `lightwalletd` as a full-node replacement.
- Do not omit the required `zcashd` configuration when the backend depends on it.
- Make clear that light-wallet privacy and trust assumptions differ from running a local full node.
