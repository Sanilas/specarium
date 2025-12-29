# ADR-005: Delivery Platform Baseline (Compose for Local, Containers for Non-Local)

**Status:** Accepted  
**Date:** 2025-12-29

## Context

We need enterprise-responsible, repeatable deployments while keeping early-stage operations simple. Docker Compose provides a low-friction local harness; containers ensure portability.

## Decision

- Use **Docker Compose** as the default local and developer orchestration harness.
- Use **containers on a managed container runtime** for all non-local environments.
- Kubernetes is not assumed initially, but the system must remain migration-ready.

## Constraints (Kubernetes-ready runtime contracts)

1. Configuration is externalized (environment variables or injected config).
2. Secrets are managed externally and never baked into images or committed to the repo.
3. Services expose health and readiness semantics.
4. Stateful dependencies are explicit and isolated.
5. No host-specific assumptions beyond orchestration abstractions.
6. Environment differences are expressed via configuration, not divergent manifests.

## Reversibility clause

Migration to Kubernetes requires an ADR and is expected to be a bounded infrastructure change, not a re-architecture, if constraints are respected.

## Consequences

- Fast local iteration.
- Enterprise-compatible deployments without early Kubernetes overhead.
- Clear upgrade path to Kubernetes.
