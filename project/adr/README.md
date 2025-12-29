# Architecture Decision Records (ADRs)

This folder contains **Architecture Decision Records (ADRs)** for this project.

ADRs are the **binding mechanism** for architectural and technical decisions that are:

- important,
- hard to change later,
- and constrain future implementation and execution.

They are intentionally **minimal, explicit, and evolutionary**.

---

## What ADRs mean in this project

In this project, ADRs serve three purposes:

1. **Capture “the important stuff”**  
   Only decisions with high switching cost, compliance impact, or strong architectural gravity belong here.

2. **Create shared understanding**  
   ADRs document the agreed system boundaries, constraints, and decision rationale so that architecture exists as a shared mental model — not tribal knowledge.

3. **Constrain execution (including AI agents)**  
   All implementation work — including Codex execution — must conform to the accepted ADRs.  
   No new technologies, patterns, or infrastructure primitives may be introduced if they violate an ADR.

---

## What does NOT belong in ADRs

ADRs are **not**:

- detailed designs or blueprints,
- API or schema definitions,
- framework configuration,
- implementation details,
- optimizations for hypothetical future scale.

Those belong in:

- per-capability ADRs (if they introduce irreversible decisions), or
- implementation documentation and code.

---

## Baseline vs Per-Capability ADRs

### Baseline ADRs

Baseline ADRs define the **global, system-wide constraints** that apply to all capabilities.

Examples:

- application boundary and architecture style,
- primary runtime and persistence,
- process and integration discipline,
- deployment and infrastructure constraints.

Baseline ADRs are expected to be **few** and **stable**.

### Per-Capability ADRs

Per-capability ADRs are used when a **specific domain or capability** requires:

- an exception to a baseline default,
- a new integration pattern,
- or a locally irreversible decision.

They must:

- reference the relevant baseline ADRs,
- justify why a deviation or specialization is necessary.

---

## Decision lifecycle

Each ADR must contain:

- **Context** – why the decision exists,
- **Decision** – what is chosen,
- **Constraints** – what this decision enforces or forbids,
- **Reversibility clause** – when and how this decision may be revisited,
- **Consequences** – expected effects and tradeoffs.

ADRs are:

- **Proposed** → discussed and reviewed,
- **Accepted** → binding,
- **Superseded** → replaced by a newer ADR,
- **Deprecated** → no longer valid but kept for historical context.

---

## Rule of thumb

> If a decision can be changed in a day without migration, data loss, or operational risk,  
> it probably does **not** belong in an ADR.

---

## Enforcement

- Any change that violates an accepted ADR requires a new ADR.
- Any disagreement about architecture must be resolved by proposing an ADR change.
- AI-assisted execution is only allowed within the boundaries defined by accepted ADRs.

---

## Current baseline

The current **baseline ADR set** defines:

- the application boundary and architecture style,
- backend runtime and persistence,
- event sourcing and integration discipline,
- delivery platform and infrastructure-as-code rules.

These form the **technical constitution** of the system.
