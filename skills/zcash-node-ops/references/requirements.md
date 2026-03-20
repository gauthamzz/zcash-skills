# Requirements

Use this file when the user is setting up or sizing a Zcash node rather than debugging an existing one.

## Zebra planning facts

- Zebra’s published recommended requirements are 4 CPU cores, 16 GB RAM, 300 GB available disk, and roughly a 100 Mbps connection.
- Zebra’s minimum published hardware requirement is lower, but 300 GB of disk remains the practical floor for mainnet cache growth.
- Zebra’s default network ports are 8233 on Mainnet and 18233 on Testnet.
- Zebra documents an RPC listener pattern and an OpenAPI spec for its RPC methods.

## `zcashd` planning facts

- `zcashd` releases are generally supported for about 16 weeks.
- each `zcashd` build has an End-of-Support height and will automatically halt when the chain reaches it
- deprecated features follow staged removal, so version and feature assumptions must be explicit

## Planning topics

- CPU and RAM headroom
- SSD and disk growth planning
- private RPC exposure versus public network ports
- logging and monitoring
- restart and recovery expectations
- whether the user should be on Zebra, `zcashd`, or a multi-service stack

## Good setup answer shape

1. identify the deployment goal
2. choose the node implementation
3. state the baseline resource assumptions
4. state the public ports and private interfaces
5. explain what to monitor from day one
