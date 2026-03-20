# SDKs

Use this file when the question is about wallet-client integration rather than only server deployment.

## Relevant SDKs and repos

- `zcash-android-wallet-sdk`: Android light-wallet SDK built to work with `lightwalletd`
- `zcash-swift-wallet-sdk`: Swift light-client framework proof-of-concept
- `zcash-light-client-ffi`: shared light-client FFI layer for app consumption
- `zashi-android` and `zashi-ios`: wallet apps that show how ECC structured real wallet products on top of the SDK stack

## Integration questions to answer

1. which platform is the client on
2. which `lightwalletd` instance does it trust
3. how does the app handle sync and spendable-balance timing
4. what SDK stability or beta caveats matter

## Important caveat

The Android SDK README explicitly calls out beta status and threat-model considerations. Do not describe SDK-based wallet development as production-trivial.
