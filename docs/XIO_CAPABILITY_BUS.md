# XIO Capability Bus

## Purpose

Every authorized XIO agent must be able to independently use XIO's capabilities and connected services without bespoke hard-wiring per role.

## Architecture

`Agent → Policy Broker → Capability Registry → Tool/Connector Adapter → External/Internal Service → Result/Artifact/Event → Audit + BRAIN`.

## Capability descriptor
Each capability declares:
- stable capability ID;
- description/input/output schema;
- risk class;
- read/write/consequential classification;
- required scopes/secrets;
- tenant/workspace/resource boundaries;
- approval policy hooks;
- idempotency/retry behavior;
- cost/spend metadata;
- provider health;
- audit/evidence behavior.

## Core capability namespaces
- `brain.*`
- `files.*`
- `comms.*`
- `calendar.*`
- `tasks.*`
- `projects.*`
- `crm.*`
- `data.*`
- `finance.*`
- `growth.*`
- `ads.*`
- `social.*`
- `funnels.*`
- `studio.*`
- `intel.*`
- `forge.*`
- `git.*`
- `browser.*`
- `computer.*`
- `workflow.*`
- `connector.*`
- `deployment.*`

## Independence

A GROWTH agent may query BRAIN, create a dataset, inspect CRM, generate creative through STUDIO, build a funnel, publish an ad through ADS and schedule a follow-up workflow if all capabilities are granted. A FORGE planner may inspect GitHub, BRAIN and project files. A finance agent may use DATA and finance connectors. The orchestrator coordinates goals; it is not a bottleneck for permitted tool calls.

## Policy

Capability access is denied by default and granted by role/workspace/project policy. A model cannot request broader authority merely by asking for it. Consequential actions can return `APPROVAL_REQUIRED` with a resumable action token/state.

## Memory

Capability results may create Sources/Signals in BRAIN. Promotion to Fact/Memory follows truth governance; successful workflow patterns may become procedural-memory candidates after review.
