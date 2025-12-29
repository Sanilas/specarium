# Quality Gates

## Purpose

Quality gates define **hard checkpoints** that prevent unsafe progression through the delivery lifecycle.

Gates are enforced by:

- Quality Gatekeeper
- Orchestrator

---

## Gate 1 — Planning Gate

**Entry Criteria**

- Frozen specification exists

**Exit Criteria**

- Implementation plan exists
- Tasks defined
- QA strategy defined
- No unresolved semantic ambiguity

---

## Gate 2 — Implementation Gate

**Entry Criteria**

- Approved plan
- No blocked ADRs

**Exit Criteria**

- Implementation complete
- Tests implemented and passing
- No unapproved Class C/D changes

---

## Gate 3 — Verification Gate

**Entry Criteria**

- Implementation complete

**Exit Criteria**

- Quality Gatekeeper reports pass
- No critical or high defects
- Known risks explicitly listed

---

## Gate 4 — Release Readiness Gate

**Entry Criteria**

- All prior gates passed

**Exit Criteria**

- Release notes drafted
- Explicit human GO/NO-GO recorded

---

## Enforcement Rules

- Gates cannot be skipped
- Gates cannot be downgraded without human approval
- Failed gates block progression
