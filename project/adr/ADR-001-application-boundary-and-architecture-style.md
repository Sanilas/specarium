# ADR-001: Application Boundary and Initial Architecture Style

**Status:** Accepted  
**Date:** 2025-12-29

## Context

We need a system shape that fits regulated enterprise SaaS expectations and solo-founder delivery reality. Premature distribution increases operational overhead and coupling risk.

## Decision

Adopt a **modular monolith** within a single explicit application boundary.

## Constraints

- One deployable “product boundary” initially.
- Internal modules are treated as architectural: responsibilities and dependencies must be explicit and governable.
- Extraction into separate services is allowed only via a future ADR that justifies the distribution and its operational and compliance implications.

## Reversibility clause

Revisit when operational needs force distribution (scale, isolation, independent release cadence) and the cost is justified.

## Consequences

- Keeps complexity and operational burden low early.
- Preserves an intentional path to later decomposition.
