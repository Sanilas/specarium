# ADR-003: Primary Persistence and Evolutionary Data Change Discipline

**Status:** Accepted  
**Date:** 2025-12-29

## Context

Persistence choices and data evolution discipline are among the hardest-to-reverse decisions in enterprise SaaS. We need strong transactional foundations and safe continuous evolution.

## Decision

Use **PostgreSQL** as the system of record, with **migration-based evolutionary data change discipline**.

## Constraints

- PostgreSQL is the system of record for transactional state and projections/read models.
- Schema changes are executed through versioned migrations.
- Data evolution must support continuous delivery; “big bang” migrations require an explicit ADR.

## Reversibility clause

A change of primary database requires a future ADR and an explicit migration strategy and should be treated as exceptional.

## Consequences

- Strong consistency and enterprise acceptance.
- Stable base for event-sourced projections and regulatory evidence needs.
