# XIO Canonical Data Model

## Identity / organization
`User, Organization, Business, Workspace, Membership, Role, Permission, Policy, Approval, SecretGrant, Budget`.

## Knowledge / memory
`Source, SourceVersion, Chunk, Signal, Claim, Fact, Memory, MemoryLink, Contradiction, Citation, EmbeddingRef, KnowledgeNode, KnowledgeEdge`.

## Agents / workflows
`AgentProfile, ModelProfile, Tool, ToolGrant, Skill, SkillVersion, Workflow, WorkflowVersion, Trigger, WorkflowRun, AgentExecution, AgentMessage, Artifact, Evaluation`.

## FORGE
`SoftwareProject, Repository, Requirement, Epic, Spec, TechnicalPlan, DeliveryWave, Ticket, Subtask, Dependency, ContextManifest, Decision, ADR, Sandbox, Worktree, CodeExecution, TestRun, Review, Finding, GauntletRun, Evidence, Promotion, Deployment, Incident, RecoveryRun`.

## Operations
`Project, Goal, Milestone, Task, TaskDependency, Comment, Notification, ApprovalRequest`.

## Communications
`Contact, Company, IdentityHandle, Conversation, Message, Attachment, Meeting, MeetingParticipant, FollowUp`.

## CRM / growth
`Relationship, Lead, Deal, Pipeline, Segment, Campaign, Sequence, SequenceStep, OutreachMessage, Funnel, FunnelStep, Form, Submission, Offer, Experiment, ConversionEvent`.

## Content / social / ads
`ContentItem, ContentVersion, Asset, Brand, SocialAccount, SocialPost, PublishJob, AudienceMetric, AdAccount, AdCampaign, AdGroup, AdCreative, AttributionEvent`.

## Data
`Dataset, DataSource, Spreadsheet, Sheet, DataPipeline, Transform, PipelineRun, Query, Chart, DataLineage`.

## Finance
`FinancialAccount, Transaction, RevenueRecord, ExpenseRecord, Invoice, Subscription, BudgetPlan, Forecast, Scenario, ReconciliationRun`.

## Studio
`Document, Presentation, Slide, Template, GeneratedAsset, Export`.

## Intel
`Watchlist, WatchTarget, IntelSource, IntelItem, ChangeEvent, Brief, Recommendation`.

## Platform
`Connector, Connection, SyncRun, WebhookEndpoint, ApiCredentialRef, AuditEvent, FeatureFlag, Entitlement, SubscriptionPlan, UsageRecord`.

## Rules
- tenant/workspace scope on all private records;
- append/supersede provenance for truth and governance artifacts;
- immutable/versioned execution evidence where practical;
- monetary values decimal-safe + currency;
- authorization applied before retrieval;
- secrets stored as references to vault values, not plaintext domain records;
- model outputs cannot directly mutate protected facts/policies without workflow authorization.
