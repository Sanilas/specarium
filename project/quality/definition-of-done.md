# Definition of Done (DoD)

## Purpose

This Definition of Done defines the **minimum acceptable quality bar** for any work item, capability, or release candidate.

No work may progress past its phase gate unless the DoD is satisfied.

---

## Global DoD (Applies to All Work)

A work item is considered done only if:

- Implementation matches frozen specifications
- No unresolved ambiguity remains
- Tests exist and pass for defined acceptance criteria
- No critical or high-severity defects remain
- Documentation is updated where applicable
- Traceability from spec → plan → tasks → tests is intact

---

## Capability-Level DoD

For a capability to be considered done:

- All acceptance criteria are implemented
- Quality Gatekeeper reports pass on defined quality gates
- Known risks are explicitly documented
- No unapproved Class C or D changes exist

---

## Release Readiness DoD

Before release consideration:

- All quality gates pass
- No open critical or high-risk items
- Release notes drafted
- Explicit human GO decision recorded

---

## Non-Negotiables

- DoD cannot be weakened without human approval
- DoD violations block progression
