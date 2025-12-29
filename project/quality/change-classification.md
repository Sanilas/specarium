# Change Classification Model

## Purpose

This document defines how changes are classified in order to determine:

- required review depth
- required approvals
- whether agent default approval applies

Classification is **mandatory** for all changes.

---

## Change Classes

### Class A — Informational / Non-Behavioral

**Examples**

- documentation updates
- comments
- formatting
- logs or metrics additions without logic impact

**Approval**

- Agent default-approved

---

### Class B — Structural / Internal / Reversible

**Examples**

- refactoring without behavior change
- internal reorganization
- test additions
- implementation details behind stable interfaces

**Approval**

- Agent default-approved
- Orchestrator oversight

---

### Class C — Semantic / Behavioral

**Examples**

- business logic changes
- workflow changes
- acceptance criteria changes
- data meaning changes

**Approval**

- Human approval required
- Orchestrator must block until approved

---

### Class D — Irreversible / External

**Examples**

- public API changes
- persistence schema meaning changes
- release actions
- compliance-relevant behavior changes

**Approval**

- Explicit human approval required
- ADR required where applicable

---

## Classification Rules

- Every change must be classified
- If multiple classes apply → **most restrictive wins**
- Unclassified changes are treated as **Class D**

---

## Enforcement

- Orchestrator enforces classification
- Quality Gatekeeper validates classification consistency
