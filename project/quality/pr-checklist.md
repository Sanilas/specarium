# Pull Request Checklist

## Purpose

Ensure consistency, traceability, and quality for all code changes.

This checklist is mandatory for every pull request.

---

## Required Checks

- [ ] Change is classified (Class A–D)
- [ ] Change aligns with frozen specification
- [ ] No semantic drift introduced
- [ ] Tests added or updated where applicable
- [ ] All tests pass
- [ ] Documentation updated if behavior is affected
- [ ] No unauthorized cross-capability coupling

---

## For Class C or D Changes Only

- [ ] Human approval recorded
- [ ] ADR linked (if applicable)
- [ ] Risk assessment documented

---

## Enforcement

- Quality Gatekeeper validates checklist
- Orchestrator blocks merge on missing items
