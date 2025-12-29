# Agentic Operating Model — Layered Architecture (Executive Summary)

This document defines the **layered structure** of the agentic operating model and the
types of artifacts that belong to each layer.

The purpose of this separation is to ensure that:

- the agentic setup is reusable across projects
- product-specific concerns never leak into the foundation
- governance, tooling, and roles remain stable over time

---

## Layer 1 — Foundation (Reusable, Project-Agnostic)

**Purpose**  
Defines _how work is done_, not _what is built_.

This layer establishes authority, governance, roles, and non-negotiable rules.
It is reused unchanged across all projects.

**Included artifacts**

- Authority and decision rights
- Operating invariants and non-negotiables
- Agent roster and role mandates
- Quality gates and definition of done
- Documentation system rules (MkDocs)
- CI/CD philosophy (provider-agnostic)
- Container-first operability posture
- Tooling posture and constraints

**Explicit exclusions**

- No domain logic
- No UI or application flows
- No business requirements
- No partner- or product-specific data

---

## Layer 2 — Product Templates (Reusable, Project-Specific Instantiation)

**Purpose**  
Defines _how a product must be specified_, not the product itself.

These templates are copied into a project and then instantiated with
project-specific content.

**Included artifacts**

- Spec templates:
  - problem definition
  - functional requirements
  - non-functional requirements
  - UX constraints
  - architecture boundaries
  - test strategy
- ADR template
- Optional product-level constraints (e.g. AI-first posture)

**Explicit exclusions**

- No concrete implementation
- No business decisions
- No environment-specific configuration

---

## Layer 3 — Product Instance (Per Project)

**Purpose**  
Defines _what is built_.

This layer contains all domain, application, and implementation details.
It is unique per project.

**Included artifacts**

- Concrete specs instantiated from templates
- Project-specific ADRs
- Source code
- Tests and fixtures
- Runbooks
- Application documentation (MkDocs)

---

## Classification Rule (Mandatory)

Every artifact must clearly belong to **exactly one layer**.

- Foundation artifacts must never reference product details.
- Product templates must not redefine governance, roles, or tooling posture.
- Product instances must consume Foundation and Templates without modifying them.

If an artifact cannot be clearly classified, it is incorrectly scoped.

---

## Enforcement

- Quality gates require correct layering.
- The Orchestrator enforces layer boundaries during task decomposition.
- The Documentation Agent ensures artifacts are discoverable and correctly classified.
- The Quality Gatekeeper blocks merges that violate layer separation.

---

## Summary

- **Foundation** governs behavior and control.
- **Product Templates** define structure.
- **Product Instance** contains all domain and application logic.

This separation is a core invariant of the agentic operating model.
