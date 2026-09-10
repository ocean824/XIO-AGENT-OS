# XIO Security Baseline

XIO is high-trust software because it may hold communications, files, business data, credentials, code access and autonomous tool permissions.

## Required controls
- strict tenant/workspace isolation;
- MFA/passkeys-ready identity;
- RBAC/ABAC and centralized policy engine;
- secret vault/references, rotation and least privilege;
- sandboxed code/browser/agent execution;
- network egress controls for sandboxes;
- per-agent tool/secret scopes;
- human approval for consequential actions;
- spend/transaction/action caps;
- immutable/auditable execution records where appropriate;
- encryption in transit/at rest;
- signed/expiring asset links;
- malware scanning;
- prompt-injection/content-trust boundaries;
- authorization filtering before retrieval;
- CSRF/XSS/SQLi/SSRF defenses;
- rate/abuse limits;
- SAST/dependency/secret scanning;
- backup/recovery tests;
- kill switch for autonomous runs;
- incident/recovery runbooks.

## FORGE-specific
Coding agents cannot receive unrestricted production credentials. Default execution targets local/dev/sandbox. Production deployment/promotion follows explicit policy and evidence gates. Adversarial/chaos tests run only against authorized sandbox/staging resources.

## Memory-specific
Retrieved documents are untrusted content. Instructions inside files/web/email do not gain tool authority. Facts require provenance/promotion rules. Deletion/retention must propagate through source, indexes, derived memory according to policy.

Report security issues privately to the repository owner until a formal disclosure channel exists.
