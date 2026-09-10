# XIO Cross-Repository Context Contract

## Required upstream

### ØMEGA
Repository: `ocean824/XYRASYSTEMS---OMEGA-AI`
Branch: `master` until repository governance changes it.

XIO planning must inspect ØMEGA before defining or changing:
- agent hierarchy/roles;
- model routing;
- memory/context systems;
- tool schemas;
- skills;
- swarm/handoff patterns;
- browser/desktop agents;
- coding/software agents;
- orchestration/control plane;
- security/governance for agents;
- XYRA/CodeSpring integration patterns.

High-value existing upstream artifacts include the ØMEGA README, `CODESPRING-MASTER-INSTRUCTIONS.md`, `CODESPRING-INTEGRATION-MANIFEST.md`, `docs/agent-structure.md`, `docs/agent-design-patterns.md`, `docs/agent-integration-patterns.md`, `docs/architecture-overview.md`, `docs/canonical-control-plane-addendum.md`, `docs/2026-agent-intelligence-stack.md`, PRIME prompts, skills, architectures and security corpus.

## Resolution policy

If XIO and ØMEGA describe the same generic runtime capability differently:
1. determine whether XIO requirement is product-specific or generic;
2. generic capability belongs upstream in ØMEGA;
3. XIO product behavior remains downstream;
4. create an ADR when reconciliation changes an approved contract;
5. preserve explicit XIO product requirements rather than silently discarding them;
6. update both repos when a shared interface changes.

## Future registry

XIO BRAIN should eventually maintain a machine-readable repository registry containing repo URL, role, owner, default branch, interfaces, version, dependency relationships and context-index locations for all Ø umbrella products.
