# XIO ADS — Autonomous Advertising & Growth Engine

## Goal

XIO should be capable of planning, creating, launching, monitoring and optimizing paid acquisition across supported advertising networks under Ø-defined budgets/policies. Native platform integrations are preferred; MadeThis is a supported accelerator/fallback adapter where its API offers useful capabilities.

## Native-first provider strategy

Provider adapters should target official APIs where practical:
- Meta Marketing/Ads;
- Google Ads;
- TikTok Ads;
- LinkedIn Ads;
- X/Pinterest/other networks as prioritized;
- analytics/attribution providers;
- ecommerce/payment/CRM conversion sources.

No provider-specific campaign object leaks into the canonical XIO campaign model.

## MadeThis adapter

MadeThis currently exposes an HTTP API and OpenAPI schema designed for coding agents. Its documented ads endpoints include campaign listing, budget updates, insights, pausing, Meta interest resolution and publishing a Meta campaign. It also exposes an MCP server for eligible developer accounts. XIO should therefore implement `MadeThisAdsAdapter` as an optional provider/accelerator, not a hard dependency.

## Canonical objects
`AdAccount, Campaign, AdGroup, AdCreative, Audience, TargetingSpec, BudgetPolicy, BidStrategy, ConversionGoal, TrackingPixel, AttributionEvent, Experiment, SpendEvent, PerformanceSnapshot, OptimizationDecision, Approval, ProviderMapping`.

## Agent roles

### MEDIA_BUYER
Builds channel/budget strategy and campaign structures.

### CREATIVE_STRATEGIST
Creates hypotheses, hooks, concepts, offers and briefs from brand/customer/product context.

### CREATIVE_PRODUCER
Uses XIO STUDIO/image/video/audio providers to generate variants.

### COPYWRITER
Produces platform-aware primary text, headlines, descriptions, scripts and landing-page copy.

### AUDIENCE_RESEARCHER
Builds/validates audiences, keywords, interests and exclusions using provider tools and XIO BRAIN/INTEL.

### LAUNCH_OPERATOR
Validates tracking, destination, budget, approvals and publishes through provider adapter.

### OPTIMIZER
Monitors performance, proposes/executes permitted budget/bid/creative/audience changes, pauses losers under policy and creates experiments.

### ADS_ADVERSARY
Checks tracking, spend caps, duplicated campaigns, bad destinations, policy/brand mismatch, attribution anomalies, runaway automation and misleading performance conclusions.

## Workflow

`BUSINESS/PRODUCT CONTEXT → GOAL → OFFER → AUDIENCE → CHANNEL PLAN → CREATIVE MATRIX → LANDING/FUNNEL → TRACKING QA → BUDGET POLICY → APPROVAL → PUBLISH → OBSERVE → ATTRIBUTION → OPTIMIZE → REPORT → MEMORY`.

## Autonomy levels

- `ADVISORY`: XIO recommends only.
- `DRAFT`: creates campaigns/creative but does not publish.
- `GUARDED`: may publish/optimize inside explicit campaign and spend limits; increases beyond policy require approval.
- `AUTONOMOUS_BOUNDED`: manages campaigns within Ø-defined daily/monthly/channel/business limits, protected metrics and stop-loss rules.

Pause/stop actions may be configured as lower-friction safety actions than spend increases.

## Budget/spend controls
- per campaign/day/month/business caps;
- provider/account caps;
- maximum automatic increase percentage and frequency;
- confirmation threshold;
- stop-loss conditions;
- anomaly detection;
- idempotent publish/update operations;
- ledger of external spend decisions;
- emergency global pause/kill switch.

## Optimization

Never optimize a single vanity metric blindly. Objective configuration can include CAC/CPA, ROAS, MER, conversion rate, qualified lead rate, LTV/CAC, revenue, contribution margin, retention or custom business KPIs. Use statistically cautious experiments and record uncertainty.

## Creative factory

XIO generates matrices across hook × angle × format × audience × offer × CTA. It stores creative lineage so performance can feed BRAIN as evidence rather than vague memory.

## Attribution

Ingest provider-reported performance plus first-party events where configured. Maintain source/attribution model and distinguish observed revenue from modeled attribution.

## Security / permissions

Ad agents receive business-scoped ad credentials, not global secrets. Every spend-changing action is audited. Policies determine whether the action executes, parks for approval or is blocked.
