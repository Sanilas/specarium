# Agent Model & Role Registry

## Operating Model — Agentic Execution

### Status

**Foundational Operating Model Artifact**

This document defines **which agent roles exist**, **why they exist**, and **how they relate to authority and execution**.

All agents listed here are governed by:

- `project/foundation/01-authority.md`
- enforced by `project/agents/orchestrator.md`

This document is **tool-agnostic** and does not define execution behavior.

---

## 1. Purpose of the Agent Model

The agent model exists to:

- separate execution concerns by responsibility
- enable autonomous work without ambiguity
- prevent implicit authority
- make escalation and accountability explicit

Agents are **not Scrum roles** and **not team metaphors**.

They are **bounded execution responsibilities**.

---

## 2. Agent Classification

Agents are grouped into **three constitutional categories**:

### 2.1 Governance Agents

Agents that enforce rules, quality, and authority.  
They perform **no delivery work**.

### 2.2 Delivery Agents

Agents that execute approved plans and produce system artifacts.

### 2.3 Support Agents

Agents that support delivery without owning system behavior or authority.

---

## 3. Governance Agents

### 3.1 Orchestrator

**File:** `project/agents/orchestrator.md`  
**Category:** Governance  
**Role:** Constitutional Court

**Responsibilities**

- Enforces authority boundaries
- Classifies actions (A/B/C/D)
- Applies default approval rules
- Blocks and escalates at no-agent zones
- Enforces phase gates

**Explicit Non-Responsibilities**

- No implementation
- No design decisions
- No risk acceptance
- No release authority

---

### 3.2 Quality Gatekeeper

**File:** `project/agents/quality-gatekeeper.md`  
**Category:** Governance (Execution-Enabling)

**Responsibilities**

- Define QA strategies (ISTQB / ISO 25010)
- Enforce quality gates
- Validate test coverage
- Report defects and risks

**Explicit Non-Responsibilities**

- No gate downgrades
- No risk acceptance
- No release approval

---

## 4. Delivery Agents

### 4.1 Backend Engineer

**File:** `project/agents/backend-engineer.md`  
**Category:** Delivery

**Responsibilities**

- Backend services & domain logic
- Internal APIs
- Backend tests and refactoring

**Authority Boundaries**

- No business reinterpretation
- No external API finalization
- No ADR approval

---

### 4.2 Frontend Engineer

**File:** `project/agents/frontend-engineer.md`  
**Category:** Delivery

**Responsibilities**

- UI implementation
- Frontend integration
- Accessibility & usability compliance

**Authority Boundaries**

- No UX invention
- No semantic changes
- No workflow redesign

---

### 4.3 Data Engineer

**File:** `project/agents/data-engineer.md`  
**Category:** Delivery

**Responsibilities**

- Data modeling & persistence
- Isolation & compliance mechanisms
- Migrations & reporting structures

**Authority Boundaries**

- No data meaning decisions
- No external schema exposure
- No compliance risk acceptance

---

### 4.4 DevOps

**File:** `project/agents/devops.md`  
**Category:** Delivery

**Responsibilities**

- Infrastructure & environments
- CI/CD pipelines
- Observability & rollback

**Authority Boundaries**

- No release authority
- No security posture changes without approval
- No gate bypassing

---

## 5. Support Agents

### 5.1 Test Engineer

**File:** `project/agents/test-engineer.md`  
**Category:** Support

**Responsibilities**

- Test design & execution
- Defect reporting
- Test documentation

**Authority Boundaries**

- No acceptance criteria changes
- No defect acceptance

---

### 5.2 UX Designer

**File:** `project/agents/ux-designer.md`  
**Category:** Support (Design Authority)

**Responsibilities**

- UX flows & interaction design
- Usability & accessibility validation

**Authority Boundaries**

- No business rule changes
- No scope expansion

---

### 5.3 Documentation

**File:** `project/agents/documentation.md`  
**Category:** Support

**Responsibilities**

- Technical & user documentation
- Runbooks & guides
- API documentation drafts

**Authority Boundaries**

- No external publication without approval
- No semantic changes

---

## 6. Execution Independence

This document **does not imply** that all agents are:

- autonomous
- executable
- backed by Codex

Whether an agent becomes executable is a **separate decision**.

Some agents may:

- remain conceptual
- remain human-only
- or be partially automated

---

## 7. Authority Inheritance

All agents:

- inherit constraints from `01-authority.md`
- defer to the orchestrator on conflicts
- must block on no-agent zones
- must escalate ambiguity affecting meaning, risk, or commitment

No agent may override another agent’s authority.

---

## 8. Amendment Policy

Changes to this document:

- alter execution responsibility
- affect escalation paths
- may impact governance guarantees

They must therefore be treated as **operating model changes**.

---

## 9. Final Statement

> Agents are not teammates.  
> They are **bounded executors under law**.

This registry exists to ensure:

**maximum autonomy without loss of control.**

---
