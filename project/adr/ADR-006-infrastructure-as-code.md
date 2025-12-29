# ADR-006: Infrastructure as Code Baseline

**Status:** Accepted  
**Date:** 2025-12-29

## Context

Regulated enterprise SaaS requires repeatable, auditable infrastructure changes and minimal configuration drift. Manual provisioning does not scale.

## Decision

All **non-local environments** must be provisioned and managed using **Infrastructure as Code (IaC)**.

## Constraints

1. All infrastructure changes for non-local environments occur via version-controlled IaC.
2. Environment separation is explicit (separate state/workspaces/projects).
3. Secrets are managed via a dedicated secrets mechanism; plaintext secrets in the repo are forbidden.
4. IaC covers at least networking, compute/runtime resources, storage for stateful dependencies, and deployment wiring.

## Reversibility clause

IaC tooling choice may change via ADR; the IaC discipline itself is non-negotiable.

## Consequences

- Reproducible environments.
- Auditable infrastructure history.
- Reduced drift and operational surprises.
