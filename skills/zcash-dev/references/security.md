# Security

Use this file when the feature touches keys, signing, transaction submission, or privacy-sensitive UX.

## Security checklist

- keep signing boundaries explicit
- do not blur watch-only and spend authority paths
- explain backup and recovery implications
- validate receive and send targets before submission
- surface privacy caveats instead of implying guarantees

## High-risk mistakes

- assuming all addresses or receivers are equally supported
- hiding custody assumptions in product copy
- treating protocol privacy as user privacy without workflow caveats
