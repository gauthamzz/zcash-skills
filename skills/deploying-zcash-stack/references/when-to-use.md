# When To Use

Use this file when the user is not sure whether they need `zcash-stack` at all.

## Use `zcash-stack` when

- the user wants Kubernetes-native deployment
- the user needs more than one Zcash service
- the team wants a plug-and-play ecosystem deployment rather than stitching services together manually

## Do not use `zcash-stack` when

- the user only needs a single node
- the job is really wallet support
- the job is only local app development against one backend

## Routing

- single-node health issue -> `zcash-node-ops`
- light-wallet backend or SDK issue -> `building-with-lightwalletd`
- product architecture issue -> `zcash-dev`
