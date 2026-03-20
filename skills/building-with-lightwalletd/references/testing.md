# Testing

Use this file when the user needs a local development or integration-test workflow for light-wallet features.

## Useful test paths

- local `zcashd` plus local `lightwalletd`
- testnet-backed wallet flow development
- darksidewalletd-based integration testing for wallets and the backend itself

## Good testing answer shape

1. identify whether the user needs unit, integration, or backend validation
2. pick local `zcashd` plus `lightwalletd` for realistic backend iteration
3. mention darksidewalletd when the user needs deeper integration testing behavior
