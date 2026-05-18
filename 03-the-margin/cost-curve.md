# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) |High |High-confidence and complex investigations routed to frontier models |
| Inference (cascading/triage) | LOW |Initial filtering and low-risk checks handled by smaller cheaper models |
| Infrastructure | MEDIUM |Includes orchestration, APIs, monitoring, audit logs, and retrieval systems |
| Data/storage | MEDIUM |Secure storage of operational logs, datasets, embeddings, and evaluation history |
| Human-in-the-loop | HIGH |Analyst validation and escalation reviews remain critical for governance |
| **Total AI COGS** | Medium| Costs remain manageable through routing and selective frontier-model usage|

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:*Lightweight model for initial nominal checks, entity extraction, duplicate detection, and low-risk screening.*
**Frontier model:*Advanced reasoning model used for ambiguous matches, adverse media analysis, multilingual investigations, and high-risk escalation scenarios.*
**Routing rule:*Requests with low complexity and high confidence remain on the triage layer, while uncertain, multilingual, politically sensitive, or high-risk cases are escalated automatically to the frontier model.*
**Expected cascade ratio:*Approximately 70–80% handled by lower-cost models and 20–30% escalated to frontier models.*

## Pricing Model

**Current pricing:*Traditional enterprise licensing and operational support model.*
**Proposed AI pricing:*Base enterprise subscription with AI usage tiers depending on screening volume, advanced investigations, and premium analytical capabilities.*
**Model:** seat-based / usage-based / outcome-based / hybrid Hybrid model combining enterprise seats with usage-based AI processing for high-volume or advanced investigations.

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x |Moderate pressure on margins | Increase routing efficiency and shift more low-risk cases to cheaper providers/models|
| Heaviest segment doubles | Infrastructure and frontier-model usage increases significantly|Introduce stricter escalation thresholds and optimize caching/retrieval logic |
| Model provider raises prices 50% |Medium operational impact |Activate multi-provider fallback strategy and renegotiate enterprise volume commitments |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
Predictable licensing revenue with mostly fixed infrastructure and support costs.

**After (AI-enabled):** Higher-value operational platform with usage-linked AI revenue, increased analytical capabilities, and stronger customer dependency, but with variable inference costs tied to adoption and workload complexity.

**Net margin shift:*Margins become more variable in the short term due to AI inference costs, but long-term value and pricing power increase through operational integration, automation gains, and premium intelligence capabilities.
*
