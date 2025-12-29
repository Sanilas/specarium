<!--
Sync Impact Report
- Version change: N/A -> 1.0.0
- Modified principles: n/a -> Broker-Centric Continuity & Traceable State; Contract-Driven Integrations & Idempotent Orchestration; Security, Privacy & Tenant Isolation; Observability & Evidence-Backed Operations; Incremental Delivery & Testable Slices
- Added sections: Safety, Compliance, and Data Boundaries; Delivery Workflow & Quality Gates
- Removed sections: None
- Templates requiring updates: .specify/templates/plan-template.md (updated); .specify/templates/spec-template.md (updated); .specify/templates/tasks-template.md (updated)
- Follow-up TODOs: None
-->

# Insurance Broker Cockpit Constitution

## Core Principles

### Broker-Centric Continuity & Traceable State
Non-negotiable: Every broker- and client-facing flow must preserve state across interruptions, be resumable without manual reconstruction, and emit a verifiable audit trail that ties actions to users, time, and source systems. No workflow can depend on out-of-band memory or personal trackers.  
Rationale: The product's value is reducing broker friction and liability in asynchronous sales; traceability is mandatory for compliance and dispute resolution.

### Contract-Driven Integrations & Idempotent Orchestration
Non-negotiable: External sales journeys, underwriting engines, and communications channels are treated as explicit contracts with stable schemas, idempotent operations, and replay-safe orchestration. Breaking changes require staged rollouts, versioned contracts, and backward-compatible fallbacks.  
Rationale: The platform does not own upstream journeys; contract discipline prevents outages when partners evolve independently.

### Security, Privacy & Tenant Isolation
Non-negotiable: Least-privilege access, scoped tokens, and audited role/entitlement changes are required. Personally identifiable information is minimized, encrypted in transit and at rest, and always associated with tenant partitions; cross-tenant data access is forbidden by default. Delegated access (e.g., to reinsurers) must be time-bound and consent-backed.  
Rationale: Broker and client trust, GDPR obligations, and multi-tenant operation demand strict isolation and auditable controls.

### Observability & Evidence-Backed Operations
Non-negotiable: All flows emit structured logs with correlation IDs, success/error codes, and partner references; business events are captured to an evidence ledger suitable for compliance review. SLOs/SLIs for orchestration latency, retry success, and notification delivery are defined and monitored; paging thresholds are documented.  
Rationale: Detecting and repairing broken journeys depends on measurable signals and evidence, not intuition.

### Incremental Delivery & Testable Slices
Non-negotiable: Every user story is independently deployable and testable, with contract tests for external touchpoints and acceptance criteria tied to broker outcomes. Critical paths (resume journey, consent capture, notification dispatch, audit export) require automated checks. Documentation (plan/spec/tasks) must stay in sync with delivered increments.  
Rationale: The product must deliver value quickly without coupling stories; testable slices reduce risk in a heavily integrated domain.

## Safety, Compliance, and Data Boundaries

- Data residency defaults to EU regions; exceptions require explicit risk acceptance and migration plans.  
- Consent, evidence requests, and underwriting artifacts are retained per insurer policy with GDPR-aligned deletion and export paths.  
- Manual underwriting and evidence uploads must be tamper-evident and traceable to the actor and source system.  
- Third-party communications (email/SMS/push) must avoid leaking confidential identifiers outside authenticated channels.

## Delivery Workflow & Quality Gates

- Constitution Check is mandatory before and after design: verify story independence, contract definitions (inputs/outputs, idempotency), data protection controls, observability coverage, and recovery paths for partner failures.  
- Plans and specs must call out external contracts, data classifications, and rollback/resume behavior; tasks must group by user story to preserve independent delivery.  
- PRs require evidence of automated checks for critical paths and updated documentation links; riskier integrations (identity, consent, payments) require peer review focused on isolation and auditability.  
- Feature rollouts must include staged deployment/rollback steps and communication to affected partners/tenants.

## Governance

- This constitution governs delivery, integration, and quality expectations; conflicting practices are subordinate.  
- Amendments require documented rationale, review by product and engineering leads, and an explicit migration or communication plan when partner contracts change.  
- Versioning follows semantic rules: MAJOR for breaking governance or removed principles, MINOR for new/expanded principles, PATCH for clarifications.  
- Compliance: Every plan, spec, and PR must include a Constitution Check summary; violations need written justification and time-bound remediation tracked in tasks.  
- Runtime guidance and templates must be updated in the same change set when principles or gates move.

**Version**: 1.0.0 | **Ratified**: 2025-12-29 | **Last Amended**: 2025-12-29
