# zcash-skills

Public skill pack for agents working on Zcash tasks.

It is built for the things agents actually need to do:

- explain Zcash clearly
- route questions to the right depth
- help with wallets and privacy habits
- troubleshoot nodes
- map goals to RPC methods
- orient users across the ecosystem
- research and write clean answers

![Zcash Skills Banner](./assets/banner.svg)

## Why this repo exists

Most skill repos look clean at the top level but get fuzzy once an agent actually opens a skill. This repo is opinionated in the other direction:

- each skill is action-oriented
- each skill has example prompts
- each skill has routing guidance
- detailed material lives in `references/`
- UI metadata exists in `agents/openai.yaml`

The structure is Codex-native first, but the presentation is meant to feel like a polished public skills catalog.

## What agents can do with it

| Skill | Agent job |
| --- | --- |
| `zcash-overview` | Triage a request and route it to the best next skill |
| `zcash-glossary` | Define Zcash terms fast and cleanly |
| `zcash-beginners` | Teach privacy basics without jargon overload |
| `zcash-wallet-guide` | Help users choose wallets, receive, send, and avoid bad habits |
| `zcash-protocol-explainer` | Explain shielded pools, upgrades, and protocol mechanics |
| `zcash-node-ops` | Diagnose node install, sync, config, and runtime issues |
| `zcash-rpc-reference` | Turn goals into likely RPC methods and caveats |
| `zcash-ecosystem-map` | Explain orgs, projects, grants, and ecosystem structure |
| `basic-research` | Gather and compare sources before answering |
| `basic-writing` | Turn raw facts into clean, readable output |

![Skills Map](./assets/skills-map.svg)

## Layout

```text
zcash-skills/
├── README.md
├── assets/
├── examples/
└── skills/
    ├── basic-research/
    ├── basic-writing/
    ├── zcash-beginners/
    ├── zcash-ecosystem-map/
    ├── zcash-glossary/
    ├── zcash-node-ops/
    ├── zcash-overview/
    ├── zcash-protocol-explainer/
    ├── zcash-rpc-reference/
    └── zcash-wallet-guide/
```

## Quick start

Copy or install the skill folders into a Codex-discoverable skills directory, then call them explicitly or let the harness trigger them from their frontmatter descriptions.

Examples:

```text
Use $zcash-overview to route this question before answering.
Use $zcash-wallet-guide to help me receive ZEC with better privacy.
Use $zcash-node-ops to debug why my node is stuck syncing.
Use $zcash-rpc-reference to map this monitoring task to the right RPC calls.
```

See [quick-prompts.md](/Users/gauthamsanthosh/Polynomial/zcash/zcash-skills/examples/quick-prompts.md) for more example invocations.

## Design rules

- Keep `SKILL.md` short enough to load fast.
- Move detail to `references/`.
- Write descriptions as trigger logic, not marketing copy.
- Prefer task language over abstract topic language.
- Keep privacy, wallet, and ops guidance explicit about tradeoffs.

## Notes

- This repo does not try to mirror a separate manifest protocol exactly.
- It does try to look and feel like a serious public skills repo.
- The content is structured so another agent can use it immediately without guessing what the skill is for.

![Agent Loop](./assets/agent-loop.svg)
