# FounderOS → XIO Migration / Reference Map

FounderOS-DEMO is a useful open-source reference, not XIO's product boundary.

## Preserve / evolve

| FounderOS concept | XIO treatment |
|---|---|
| Operator console | Expand into XIO COMMAND with movable widgets, approvals, multi-business/project context, software-build health, and next actions. |
| Unified comms | Expand connectors, entity resolution, approval policies, memory, follow-up and automation. |
| Funnel | Evolve into full funnel/site/offer builder with deploy/export, forms, experiments and attribution. |
| Social/content | Expand to multi-channel publishing, asset generation, analytics, campaigns and repurposing. |
| Finances | Expand into multi-business finance intelligence, scenarios, invoices/subscriptions and reconciliation. |
| Agents with real `run()` | Replace/extend with XIO SWARM runtime, role/model routing, permissions, isolated executions, event triggers and evidence. |
| Tasks | Integrate with projects, Epics, business workflows and FORGE tickets. |
| Skills | Expand into versioned reusable skills/SOPs with permissions, triggers, tests and marketplace/import/export potential. |
| Org hierarchy | Generalize into users, organizations, businesses, workspaces, departments, agents and permission scopes. |
| Brain/G-Brain | Preserve Markdown/hybrid retrieval concept; expand provenance, access scope, connectors and multimodal sources. |
| Optimal Engine | Preserve Source→Signal→Claim→Fact→Memory concept; expand contradictions, effective dates, supersession, confidence and decision context. |
| Workflows | Expand into event-driven XIO FLOW DAG/runtime with schedules, approvals, retries, long-running jobs and human gates. |
| Integrations honest status | Preserve as a hard architectural rule. |
| Analytics | Expand into cross-business/project/agent/campaign/software analytics. |
| Personas | Evolve into workspace templates/business operating profiles rather than superficial reskins. |

## Replace

- Seeded SQLite production assumption → PostgreSQL canonical store; local/demo adapter may remain.
- Single-process demo runtime → scalable web/API/worker/event architecture.
- Fixed agent roster → dynamic model-agnostic swarm registry.
- Basic knowledge graph → governed multi-source memory + vector/graph retrieval.
- Demo deployment assumptions → adapter-based deployment with Neon/Cloudflare/R2 first-class profile.

## Add — XIO-only major systems

- XIO FORGE native software factory;
- native Epic/Spec/Ticket planner;
- specification compiler / CodeSpring analogue;
- context compiler/manifests;
- multi-agent worktree/sandbox execution;
- autonomous approved Epic execution / Smart-YOLO analogue;
- adversarial/chaos review;
- XYRA Gauntlet/evidence/promotion;
- spreadsheet/data engineering workspace;
- investor/customer outreach and segmentation;
- animated HTML deck/presentation builder;
- website/funnel generator;
- GitHub/repository intelligence;
- browser/computer operations;
- industry intelligence/news radar;
- model router/evals;
- API/MCP/plugin SDK;
- enterprise-grade secrets/audit/security controls;
- desktop/mobile surfaces.

## License discipline

If FounderOS code is incorporated, preserve applicable MIT notices/license obligations. XIO specifications, product identity, new architecture, and independently authored modules remain governed by XIO's own repository/license decisions.
