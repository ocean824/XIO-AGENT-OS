# XIO FORGE — Native Software Factory Architecture

## Goal

Give XIO the core capabilities of modern specification-driven planning environments, CodeSpring-style specification generation, coding-agent swarms, autonomous Epic orchestration, and adversarial review **natively**.

External Traycer, CodeSpring, Codex, Claude Code, GitHub agents, or other systems can be used through adapters but are not required for the domain model or orchestration logic.

## Canonical entities

`SoftwareProject, Repository, ProductIntent, Requirement, Epic, Spec, TechnicalPlan, DeliveryWave, Ticket, Subtask, Dependency, ContextManifest, Decision, ADR, AgentProfile, ModelProfile, Execution, Sandbox, Worktree, Artifact, TestRun, Review, Finding, GauntletRun, Evidence, Promotion, Deployment, Incident, RecoveryRun`.

## State machines

### Epic
`DRAFT → PLANNING → REVIEW → APPROVED → EXECUTING → VERIFYING → COMPLETE | BLOCKED | CANCELLED`.

### Ticket
`BACKLOG → READY → CLAIMED → IMPLEMENTING → VALIDATING → REVIEWING → FIX_REQUIRED → EVIDENCE_READY → DONE | BLOCKED`.

### Finding
`OPEN → ACKNOWLEDGED → FIXING → REVERIFY → RESOLVED | ACCEPTED_RISK | ESCALATED`.

### Promotion
`CANDIDATE → CHECKS → REVIEW → APPROVED → PROMOTING → SUCCEEDED | FAILED | ROLLED_BACK`.

## Planning engine

Input: product intent + governing repo context + constraints.
Output: requirements, architecture questions, specs, plans, waves, tickets, dependencies, acceptance criteria, risks, context manifests, Gauntlet requirements.

Planner must surface material unknowns. It may propose defaults but cannot silently lock founder-level decisions.

## Specification compiler

Produces structured/Markdown documents with stable IDs/frontmatter. Supports templates for PRD, architecture, data, APIs, UX, security, tests, runbooks, ADRs, work packages, evidence.

All generated documents register in a context graph with authority/status/dependencies/supersession.

## Scheduler / autonomous Epic engine

Dependency-aware scheduler computes runnable tickets, concurrency limits, agent capability fit, budget, resource locks, and risk. It dispatches isolated executions and observes outcomes.

Discoveries are classified:
- implementation detail: update technical plan automatically and log;
- non-material architecture clarification: propose/update with review policy;
- material product/architecture change: stop affected dependency chain and escalate.

## Agent runtime

Agent profile includes role, provider/model preferences, tools, permissions, budget, network policy, filesystem scope, secrets scope, timeout, retry policy, evaluation history.

Agents communicate through structured artifacts/events, not uncontrolled shared hidden context.

## Sandbox/worktree manager

- create isolated workspace;
- checkout scoped branch/worktree;
- inject only authorized secrets/config;
- enforce network/tool policy;
- capture commands/tool calls/logs;
- collect diffs/tests/artifacts;
- destroy/retain according to policy.

## Context compiler

Ranks governing and task-specific context. Uses repository symbol search, dependency graph, requirements, ADRs, prior findings and semantic retrieval. Emits context manifest with token/size budget and provenance.

## Review council

Independent roles can run in parallel:
- requirements reviewer;
- architecture reviewer;
- code reviewer;
- test reviewer;
- security reviewer;
- data reviewer;
- UX/accessibility reviewer;
- performance reviewer;
- adversary/chaos reviewer.

Council outputs structured findings with severity, evidence, affected requirements, confidence, reproduction, remediation and revalidation criteria.

## Adversarial engine

Can perform bounded fault injection in sandbox/staging: dependency outage, malformed provider response, network timeout, permission denial, stale schema, race/retry, prompt injection, malicious document, bad migration, partial deployment. Never attack unauthorized external systems.

## Gauntlet engine

Builds a gate matrix from requirements/risk. Runs deterministic checks before AI judgment where possible. AI reviewers cannot override hard security/test/policy failures without explicit authorized risk acceptance.

## Evidence ledger

Every completed ticket/Epic records requirement→plan→execution→diff→test→review→finding→fix→evidence lineage. Evidence is queryable from UI and API.

## Git / release

Supports GitHub first; adapters for other SCM later. Default branches: feature/worktree → develop → staging → main. FORGE can create PRs, monitor CI, request reviews, assemble release notes, deploy through adapters, monitor and rollback according to policy.

## User experience

FORGE has:
- natural-language project chat;
- Epic canvas/tree;
- Specs and Tickets;
- dependency graph;
- agent swarm live view;
- executions/logs;
- worktree/diff view;
- review council;
- Gauntlet dashboard;
- evidence explorer;
- environment/deployment view;
- approvals/escalations;
- project memory/decisions.
