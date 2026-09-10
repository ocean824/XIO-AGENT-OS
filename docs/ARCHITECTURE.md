# XIO System Architecture

## Logical topology

```text
Web / Desktop / Mobile / CLI / API
             |
      XIO Gateway + Auth
             |
        XIO ORCHESTRATOR
             |
+------------+-------------+-------------+-------------+
|            |             |             |             |
COMMAND     BRAIN         SWARM         FORGE          FLOW
|            |             |             |             |
COMMS       MEMORY       MODEL/TOOLS    GIT/SANDBOX   TRIGGERS
CRM         RETRIEVAL     EXECUTIONS     GAUNTLET      JOBS
GROWTH      PROVENANCE    EVALS          EVIDENCE      APPROVALS
DATA        GRAPH         BUDGETS        DEPLOY        RETRIES
MONEY
STUDIO
INTEL
             |
      CONNECTOR / MCP / API LAYER
             |
Postgres + Vector + Object Store + Queue/Event + Cache
             |
Observability + Audit + Secrets + Policy + Billing
```

## Suggested monorepo

```text
apps/
  web/
  desktop/
  mobile/
  api/
  workers/
  sandbox-runner/
packages/
  domain/
  schemas/
  db/
  auth/
  permissions/
  audit/
  events/
  ai-gateway/
  agents/
  skills/
  workflows/
  memory/
  retrieval/
  knowledge-graph/
  forge/
  planner/
  context-compiler/
  sandbox/
  git/
  gauntlet/
  evidence/
  connectors/
  comms/
  calendar/
  crm/
  growth/
  funnels/
  social/
  data/
  finance/
  studio/
  intel/
  billing/
  ui/
  observability/
```

## Deployment profile

First-class profile: Cloudflare edge/security + R2 object storage + Neon PostgreSQL; provider-neutral interfaces retained. Background workers/sandbox compute may run on suitable container/serverless/compute providers. Heavy agent/code workloads must be separable from the web tier.

## Event-driven core

Major actions emit domain events. XIO FLOW subscribes to events for workflows; BRAIN records relevant operational memory; audit captures consequential changes; analytics receives privacy-safe events.

## Policy engine

Central authorization/policy evaluates actor, tenant/workspace, resource, action, agent identity, tool, secret scope, environment, risk, budget and approval state before consequential operations.

## Model/tool execution

LLMs never receive unrestricted ambient credentials. Tool calls are brokered through XIO with explicit scopes and audit. Structured schemas validate outputs crossing deterministic boundaries.

## Browser/computer execution

Runs in isolated sessions where practical. Capture action logs/screenshots/artifacts as policy permits. Require explicit approvals for sensitive actions.

## Data isolation

All private resources carry tenant/workspace scope. Retrieval filters authorization before semantic search results reach models. Cross-business context sharing is explicit, not accidental.
