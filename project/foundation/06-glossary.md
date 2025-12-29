# Phase 0 Glossary

This glossary defines all abbreviations, roles, and core terms used in the
Phase 0 agentic operating model artifacts.

The glossary is authoritative for terminology used in the Foundation layer.
If a term is ambiguous or overloaded in common usage, its meaning here prevails.

---

## Core Layers

**Foundation**  
The reusable, project-agnostic layer defining governance, roles, authority,
quality gates, and operating rules. It never contains product or domain logic.

**Product Templates**  
Reusable templates that define how a product must be specified, without
containing product-specific content.

**Product Instance**  
A concrete project containing domain logic, implementation code, tests,
runbooks, and instantiated specifications.

---

## Roles and Agents

**Agent**  
An AI system operating under a defined role contract with explicit scope,
capabilities, and constraints.

**Orchestrator / Project Manager Agent**  
The agent responsible for decomposing spec deltas into task graphs, sequencing
work, and enforcing readiness for quality gates. Does not implement production code.

**UX Designer Agent**  
Agent responsible for user experience constraints, information architecture,
interaction flows, accessibility rules, and UX-related specifications.

**Senior Backend Engineer Agent**  
Agent responsible for backend implementation according to specs and ADRs.
May propose architectural decisions but cannot unilaterally decide them.

**Senior Frontend Engineer Agent**  
Agent responsible for frontend implementation according to UX specs and contracts.

**DevOps Agent**  
Agent responsible for operability, containerization, CI mechanics, and runbooks.
Does not select hosting platforms unless explicitly instructed.

**Senior Test Engineer Agent**  
Agent responsible for converting acceptance criteria into executable tests and
owning the test strategy and quality gates.

**Documentation Agent**  
Agent responsible for maintaining the documentation system (MkDocs), ensuring
documentation completeness and correctness.

**Quality Gatekeeper / PR Review Agent**  
Read-only agent responsible for validating compliance with specs, tests,
documentation, security posture, and quality gates.

**Human / Product Owner / Architecture Authority**  
The single human authority owning product intent, architecture decisions,
non-functional requirements, and final merge approval.

---

## Governance and Process Terms

**Authority Model**  
Definition of who is allowed to make which decisions and how conflicts are resolved.

**Invariant**  
A non-negotiable rule that applies across all projects using the operating model.

**Quality Gate**  
A mandatory condition that must be satisfied before a change can be merged
(e.g. tests passing, documentation updated).

**Definition of Done (DoD)**  
A checklist defining when work is considered complete and mergeable.

**Spec**  
A written artifact that defines intent, requirements, constraints, or behavior.
Specs are authoritative over implementation.

**Spec Delta**  
A change to an existing spec or the introduction of a new spec that alters
intent, behavior, or constraints.

**ADR (Architecture Decision Record)**  
A document capturing a significant architectural decision, its context,
alternatives, and consequences.

**Runbook**  
Operational documentation describing how to run, debug, or operate the system.

---

## Tooling and Infrastructure Terms

**CI (Continuous Integration)**  
Automated processes that validate changes through builds, tests, and checks.

**CD (Continuous Deployment / Delivery)**  
Automated processes that deploy validated changes to environments.
Optional in the foundation; provider-agnostic.

**Containerization**  
Packaging an application and its runtime dependencies into a container that
runs consistently across environments.

**MCP (Model Context Protocol)**  
A protocol for exposing tools and systems to agents in a controlled way.

**Docker MCP Gateway**  
A centralized mechanism for exposing approved tools to agents with role-scoped access.
Referenced at a conceptual level only in Phase 0.

---

## Capability and Access Terms

**Tool Capability**  
A class of actions an agent may perform (e.g. version control, test execution).

**Read-only**  
Capability to inspect but not modify artifacts.

**Write**  
Capability to modify artifacts directly.

**Propose-only**  
Capability to create drafts or suggestions that require approval to apply.

**Forbidden**  
Explicitly disallowed capability.

---

## Repository and Collaboration Terms

**PR (Pull Request)**  
A proposed set of changes submitted for review and merging.

**Protected Branch**  
A branch with enforced rules such as required reviews and passing checks.

**Merge Authority**  
The role allowed to approve and merge changes into protected branches.

---

## Documentation Terms

**MkDocs**  
A static documentation generator used as the standard documentation system.

**Documentation Gate**  
A quality gate requiring documentation updates when behavior changes.

---

## Classification Terms

**Material Change**  
A change that affects behavior, interfaces, architecture, configuration,
security posture, or observability. Requires a spec delta.

**Trivial Change**  
A change that does not affect behavior (e.g. formatting, comments).
May be exempt from a spec delta.

---

## Final Note

If a term is used in Phase 0 artifacts and not defined here,
it must be added to this glossary before Phase 1 proceeds.
