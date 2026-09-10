# XIO Build Contract

## Authority
Direct current instruction from Ø > this Build Contract > approved PRD/architecture/security/data/API specs > accepted ADRs > scoped ticket/acceptance criteria > project memory > supporting corpus > existing implementation.

## Non-Negotiables

1. XIO is a real operating system for founder/business workflows, not a dashboard mockup.
2. XIO FORGE natively implements specification compilation, Epic planning, ticket orchestration, agent swarms, isolated worktrees/sandboxes, autonomous approved execution, adversarial review, XYRA Gauntlets, evidence, and release promotion. Traycer/CodeSpring/Codex/other systems may integrate, but none is required for core FORGE behavior.
3. XIO is model-agnostic. No core domain logic depends on one model vendor.
4. External tools/providers sit behind adapters and expose honest status.
5. Durable memory is governed by provenance/confidence/review; agents cannot promote guesses into facts silently.
6. Consequential external actions require authorization according to policy. Autonomous planning is not blanket authorization to send, spend, publish, delete, deploy, merge, sign, transact, or disclose.
7. Software promotion is evidence-gated through XYRA.
8. Material requirement/product changes escalate to Ø rather than being silently simplified.
9. Monetization/business functionality is not deleted merely because launch/compliance work may be required. Preserve architecture with configuration/feature/jurisdiction/provider gates unless functionality is confirmed illegal/impossible.
10. Security, tenant isolation, secrets, auditability, backup/recovery, and prompt-injection boundaries are architectural requirements.
11. The FounderOS reference may be reused only according to its license and should be treated as a starting/reference implementation; XIO's architecture is independently governed here.
12. Build for the complete end-state. Release waves may progressively activate features without disposable rewrites.

## XYRA Completion Loop
`REQUIREMENT → PLAN → IMPLEMENT → VALIDATE → REVIEW → ATTACK → FIX → RE-VALIDATE → EVIDENCE → PROMOTE`.

A task is not complete merely because code exists or tests happen to pass. Acceptance criteria must map to evidence.

## Defect Escalation
- requirement defect → escalate/update requirement intentionally;
- architecture defect → ADR/contract change + re-Gauntlet affected areas;
- test defect → correct only when governing behavior proves test wrong;
- environment defect → fix environment + rerun;
- provider defect → implement retry/fallback/degrade/error/block behavior;
- security/data/privacy defect → block affected promotion until resolved/risk-accepted by authorized owner;
- UX/accessibility defect → fix or explicitly disposition against requirements.
