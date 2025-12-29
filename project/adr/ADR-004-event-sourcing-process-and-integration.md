# ADR-004: Event Sourcing Default, Auditability, Process Ownership, and Integration Discipline

**Status:** Accepted  
**Date:** 2025-12-29

## Context

We must prevent opaque workflows and ensure high-integrity traceability suitable for regulated enterprise SaaS. Partial event-driven systems with ad-hoc mixing of API calls and events lead to unpredictable coupling and poor operability.

## Decision

Adopt **event sourcing as the default persistence model for core domain aggregates**, with strict process ownership and integration rules.

## Constraints

### 1) Event sourcing as default

- Core domain aggregates persist as append-only event streams.
- Current state is derived via projections (read models).
- Events are versioned contracts with documented intent and lifecycle.

### 2) Auditability and evidence

- The event stream forms part of the authoritative historical record.
- Security- and compliance-relevant actions must be attributable (actor, tenant context, timestamp, intent, correlation/request id).

### 3) Process ownership and visibility

For any cross-boundary business process:

- A single process owner is accountable end-to-end.
- The process has an explicit representation (state machine, saga, or workflow).
- A canonical flow description exists (trigger, steps, external calls, events, retry/compensation intent).

### 4) Anti-hybrid rule

For each cross-boundary process, exactly one coordination pattern must be chosen:

- Orchestration (default), or
- Choreography (requires explicit justification)

Organic mixing of calls and events without an ADR is forbidden.

### 5) Reliability rule

Event publication and consumption across boundaries must be reliable and consistent with the persistence model. Mechanisms must prevent split-brain behavior and “ghost events.”

## Reversibility clause

Event sourcing is the default, but exceptions are allowed per capability via ADR when domain value is low or operational cost outweighs benefit.

## Consequences

- Higher upfront discipline.
- Improved traceability, auditability, and process clarity.
- Avoidance of distributed-monolith failure modes.
