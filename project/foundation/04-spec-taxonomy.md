# Spec Taxonomy (Foundation)

## Spec artifacts (project-agnostic)

- problem.md
  - What problem exists; who is it for; explicit non-goals.
- requirements.md
  - Functional requirements expressed as capabilities and acceptance criteria.
- non-functional.md
  - NFRs: security, privacy, performance, reliability, observability, compliance posture.
- ux.md
  - IA, flows, states, accessibility constraints, content/tone rules.
- architecture.md
  - Architecture boundaries, module responsibilities, interface contracts, runtime model.
- test-strategy.md
  - Test pyramid, required gates, fixtures, environments, CI enforcement.

## ADR artifacts (decision-agnostic)

- ADR is required when:
  - a tradeoff is made that affects future constraints
  - a library/framework choice is made that changes long-term maintenance
  - a security boundary is defined or changed
  - a data model/event model choice is made

## Spec delta triggers (must update spec)

A spec delta is required for:

- new capability or behavior
- change to user-visible behavior or API/contract semantics
- new configuration surface or env var
- architecture boundary change
- security posture change (authn/authz, secret handling, data sensitivity)
- observability change (logs/metrics/traces expectations)
- webhook/event semantics (verification, idempotency, replay behavior)
- CI gate policy change
- doc taxonomy or doc gate policy change

## Allowed “no spec delta” class

- formatting
- typo fixes
- internal refactor with identical behavior and unchanged public contracts
- adding comments
- purely additive documentation (no behavior change)

## Acceptance criteria style (mandatory)

- Write as testable statements:
  - Given / When / Then or equivalent
- Each requirement must map to:
  - one or more tests
  - one or more documentation pages
