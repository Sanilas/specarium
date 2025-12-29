# ADR-000: Architectural Decision Discipline and Shared Understanding

**Status:** Accepted  
**Date:** 2025-12-29

## Context

Architecture is the set of decisions that are important and hard to change, plus the shared understanding of the system by expert developers. We want a minimal baseline that constrains execution while keeping the system evolvable.

## Decision

Use ADRs as the binding mechanism. Baseline ADRs must remain minimal and focused on irreversible constraints. All other decisions are per-capability ADRs and must not contradict baseline constraints.

## Constraints

1. **Baseline ADR test:** A baseline ADR must be justified as “important + hard to change” in this context.
2. **Reversibility clause:** Every ADR must include how change remains possible and what triggers a revisit.
3. **Shared understanding artifact:** Maintain a lightweight, living view of:
   - the application boundary,
   - major modules/containers,
   - key end-to-end process and integration flows.  
     (Tooling is not mandated; the shared understanding is.)
4. **ADR gating:** Any decision that introduces:
   - new cross-boundary coupling patterns,
   - new infrastructure primitives beyond baseline,
   - additional runtimes or languages  
     requires an ADR.

## Consequences

- Prevents accidental architecture and technology sprawl.
- Provides enforceable constraints for later Codex execution.
