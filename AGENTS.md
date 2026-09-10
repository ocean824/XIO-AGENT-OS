# XIO Agent Operating Contract

XIO is developed under XYRA and itself contains a native XYRA-compatible agent/swarm runtime.

## Development pipeline
`Ø → canonical specifications → XIO/Traycer planning environment → context compiler → coding-agent swarm → adversarial review → XYRA Gauntlet → GitHub promotion → release`.

Codex may be the primary coding worker, but the protocol is model-agnostic.

## Project mode policy
For a complete XIO build, use Epic planning. Decompose the complete end-state before autonomous implementation. Smart-YOLO-style execution is permitted only for an explicitly approved Epic/spec/wave/ticket scope.

## Context policy
Read `docs/CONTEXT_INDEX.md`. Large CodeSpring/XYRA corpora are selectively retrieved through context manifests. Never bulk-load hundreds of Markdown files into every agent turn.

## Work isolation
Implementation agents use scoped branches/worktrees/sandboxes. Parallel agents must not mutate the same working tree without explicit coordination.

## Independent review
Material implementation must be reviewed by at least one role/context that did not author the change. High-risk areas require specialized security/data/permissions review.

## Evidence
Completion packet: requirements satisfied, changed modules, migrations/config, tests, commands/results, security/privacy checks, UI artifacts where relevant, known limitations, unresolved findings, commit/PR references.

## Native FORGE requirement
When building XIO FORGE, do not implement it as wrappers around Traycer/CodeSpring. Implement native domain objects/services for Epics, Specs, plans, tickets, context manifests, executions, agent roles, sandboxes/worktrees, review findings, Gauntlet runs, evidence, and promotions. External systems are adapters.
