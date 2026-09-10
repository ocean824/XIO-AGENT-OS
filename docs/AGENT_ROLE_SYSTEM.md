# XIO Agent Role System

## Principle

Agents are durable role definitions plus per-run instances. Ø can set a default model/provider for each role globally, per business/workspace, per project, or per Epic. Every spawned agent receives its role charter, XYRA obligations, task context manifest, permissions, tools/connections, budgets and acceptance criteria automatically.

## Configuration precedence
`run override → ticket/Epic override → project override → workspace/business override → global role default → system fallback`.

## AgentProfile
Required fields:
- id/name/role;
- charter/system instructions;
- default provider/model;
- reasoning/effort profile where supported;
- fallback models;
- capabilities/tags;
- allowed tools/connectors;
- secret scopes;
- network/filesystem policy;
- budget/token/time/concurrency caps;
- approval policy;
- memory scope;
- XYRA stage responsibilities;
- required output schema;
- eval history/reliability metrics;
- enabled/paused state.

## Built-in roles

### ORCHESTRATOR
Maintains objective/dependencies, dispatches roles, monitors blockers, enforces approvals and XYRA state transitions. Does not silently redefine requirements.

### PLANNER
Turns intent/specifications into requirements, Specs, technical plans, waves, tickets, dependencies, context manifests, acceptance criteria and risk. Default model configurable.

### ARCHITECT
Owns architecture proposals, interfaces, data boundaries, ADRs, scalability and cross-system consistency.

### RESEARCHER
Uses authorized web/data/connectors to gather source-backed information and attach provenance/confidence.

### EXECUTION / IMPLEMENTER
Writes/modifies code or executes operational work against an approved plan. Runs in scoped sandbox/worktree for software work.

### TEST ENGINEER
Builds/runs deterministic tests, integration/e2e suites, fixtures and reproduction cases.

### REVIEWER
Independent requirement/implementation review. Must not inherit hidden chain/context from the authoring agent beyond explicit artifacts.

### ADVERSARY
Attempts to falsify completion: edge cases, contradictions, fault injection, prompt injection, bad inputs, provider outages and workflow abuse within authorized environments.

### SECURITY
Threat modeling, auth/permissions, secrets, tenant isolation, dependency/configuration review, data exfiltration and sandbox boundaries.

### DATA
Schemas, migrations, lineage, quality, analytics, pipelines, spreadsheet/SQL work and data validation.

### UX / ACCESSIBILITY
Interaction states, responsive behavior, accessibility, visual consistency and user-flow regressions.

### PERFORMANCE
Profiling, load/scaling, caching, queue behavior, latency and resource/cost analysis.

### RELEASE
Promotion, CI/CD, migrations, deployment, smoke tests, rollback and release evidence.

### GROWTH
CRM, segmentation, funnels, campaigns, content, ads and analytics.

### FINANCE
Business financial analysis, budgets, scenarios and reconciliation using deterministic calculation tools.

### OPERATIONS
Cross-business workflows, vendors, tasks, scheduling, support and recurring processes.

## Spawn contract

When XIO spawns an agent it compiles:
1. role charter;
2. XYRA stage instructions;
3. current objective;
4. governing documents;
5. context manifest;
6. explicit tool/connector capabilities;
7. memory scope;
8. approval boundaries;
9. budget/time limits;
10. required outputs/evidence.

Agents can independently call every XIO capability for which their policy grants access: BRAIN, COMMS, CALENDAR, CRM, DATA, GROWTH, ADS, MONEY, STUDIO, INTEL, FORGE, browser/computer, connectors and workflows. The orchestrator does not need to proxy ordinary permitted calls.

## Role editor UI

XIO must provide a UI to:
- create/clone/customize roles;
- choose default model/provider;
- define fallback chain;
- edit role instructions;
- grant/revoke tools/connections;
- set business/project scope;
- set budgets/concurrency;
- require approvals;
- inspect runs/cost/reliability;
- A/B/evaluate models for a role;
- temporarily override model on an Epic/ticket/run.

## XYRA injection

XYRA is automatically injected into FORGE roles according to stage. Users should not have to paste the protocol into every agent prompt. Business-operation agents receive the relevant XIO governance/approval rules even when not doing software work.
