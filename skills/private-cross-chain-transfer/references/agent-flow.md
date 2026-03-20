# Agent Flow

Use this file when the user wants the agent to reason about or automate the route.

## Agent planning steps

1. classify source chain and source wallet capability
2. obtain quote or route options for source asset -> ZEC
3. check whether the route lands in transparent or shielded-capable wallet support
4. if privacy is the goal, ensure the plan includes a real shielded leg
5. if the route exits Zcash, evaluate the destination-chain path and leak points
6. explain refunds, timeouts, and destination compatibility

## Good agent output

- route summary
- per-leg exposure summary
- trust assumptions
- failure and refund states
- what the user must confirm before execution
