# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | LOW | H / M / L |Shift non-critical workloads to secondary providers while preserving the primary provider for high-risk and strategic use cases. Review consumption and temporarily reduce non-essential AI processing. | 
| **Abstraction** | MEDIUM | H / M / L | MEDIUM |Reinforce the abstraction layer to ensure prompts, routing, and evaluation pipelines remain provider-agnostic and can be switched with minimal operational disruption.
| **Routing** | MEDIUM | H / M / L |MEDIUM | Dynamically reroute lower-priority requests to alternative providers and activate fallback logic based on cost, latency, and operational criticality.
| **Eval** | HIGH | H / M / L |HIGH | Immediately rerun golden datasets and regression benchmarks against alternative providers to validate quality, hallucination rate, and operational acceptability before wider rollout.

## Portability Score
<!-- Ready / Partial / Locked --> PARTIAL 
PARTIAL
## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? --> since the model we are building will have different provider we will be able to reroute less critical use cases to the second best provider in order to minmize financial impact. for high critica high strategical we will keep the provider and look for alternatives. this strategy will give us a small safety net and some time in case this occurs to build and test with other provider . 
since the model we are building will have different provider we will be able to reroute less critical use cases to the second best provider in order to minmize financial impact. for high critica high strategical we will keep the provider and look for alternatives. this strategy will give us a small safety net and some time in case this occurs to build and test with other provider .

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
What remains defensible is the operational layer built around the model: proprietary internal datasets, analyst feedback loops, governance workflows, golden evaluation datasets, and institutional review logic. While a provider may replicate generic AI capabilities, it would be significantly harder to reproduce the operational trust, adjudication history, and domain-specific escalation processes accumulated over time
