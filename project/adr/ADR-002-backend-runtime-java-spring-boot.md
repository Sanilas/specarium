# ADR-002: Backend Runtime and Framework Baseline

**Status:** Accepted  
**Date:** 2025-12-29

## Context

Backend runtime and framework strongly influence security posture, maintainability, ecosystem maturity, and long-term change cost.

## Decision

Use **Java with Spring Boot** as the backend runtime and framework baseline.

## Constraints

- Java/Spring Boot is the primary backend runtime within the application boundary.
- Introducing additional backend runtimes requires a new ADR with explicit irreversibility, operational, and compliance impact analysis.

## Reversibility clause

Revisit only with clear evidence of unacceptable delivery friction or non-negotiable enterprise constraints that Spring Boot cannot satisfy.

## Consequences

- Enterprise-grade ecosystem and conventions.
- Reduced technology fragmentation risk.
