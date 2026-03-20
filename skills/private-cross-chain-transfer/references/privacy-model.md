# Privacy Model

Use this file whenever the user uses words like "private", "anonymous", or "unlinkable."

## Privacy boundary map

- source-chain deposit leg: usually public on the origin chain
- swap or intents execution rail: visible to the operator or solver to some degree
- shielded Zcash leg: strongest privacy segment when the value actually moves or rests in shielded ZEC
- exit leg: creates new visible activity on the destination side

## What not to say

- do not call the whole route private by default
- do not imply a swap into ZEC automatically means the whole path is unlinkable
- do not ignore timing, destination choice, or reuse patterns

## Better phrasing

- "This route contains a Zcash privacy leg."
- "Privacy improves materially in the shielded segment, but the surrounding cross-chain legs remain visible or partially visible."
