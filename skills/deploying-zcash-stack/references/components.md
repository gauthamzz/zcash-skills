# Components

`zcash-stack` is a Helm chart for deploying a complete Zcash ecosystem on Kubernetes.

## Included services

- `zcashd`
- Zebra
- `lightwalletd`
- Caddy
- `dnsseeder`

## Service roles

- `zcashd` and Zebra provide node-level blockchain access
- `lightwalletd` serves light wallets efficiently
- Caddy handles web-facing edge concerns
- `dnsseeder` supports peer discovery infrastructure

## Good answer shape

1. list the services
2. state why each exists
3. explain which ones the user's product actually needs
