# XIO Context Index

## Governing order
1. direct Ø instruction;
2. `BUILD_CONTRACT.md`;
3. approved PRD/architecture/FORGE/data/security/API specs;
4. accepted ADRs;
5. scoped ticket/acceptance criteria;
6. `PROJECT_MEMORY.md`;
7. supporting CodeSpring/XYRA corpus;
8. existing implementation where not contradicted.

## Large corpus design

XIO may contain hundreds/thousands of Markdown specifications. Store them as an indexed dependency graph, not one prompt.

Recommended metadata:
```yaml
id: XIO-CS-0001
status: PROPOSED
authority: supporting
domain: forge
depends_on: [XIO-REQ-FRG-001]
supersedes: []
applies_to: [packages/forge]
```

Statuses: `LOCKED, APPROVED, OPEN, PROPOSED, SUPERSEDED`.

## Context manifest

Every FORGE ticket/work package declares governing docs, task-specific docs, ADRs, code/symbol context, requirements, acceptance criteria, prior findings, test/evidence requirements and context budget.

XIO's native context compiler should eventually generate this automatically using dependency graphs + semantic/symbol retrieval + authority rules.
