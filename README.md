# Specarium

**Specarium** is a spec-driven operating model and incubator for building software systems
with clarity, governance, and repeatable execution.

It provides a reusable, domain-agnostic foundation where **product intent is captured as specifications**
and systematically transformed into plans, tasks, and implementation — while humans retain
ownership of meaning and decisions.

---

## Why Specarium?

Most software projects fail not because of bad code, but because of:

- unclear intent
- implicit decisions
- missing governance
- fragile handoffs between planning and execution

Specarium addresses this by making **specifications the primary source of truth** and by enforcing
clear boundaries between:

- governance
- product intent
- and execution

---

## Core Principles

- **Spec-first**  
  No meaningful change without an explicit specification.

- **Human-owned meaning**  
  AI assists execution, but never defines intent or business meaning.

- **Governance by design**  
  Authority, constraints, and quality gates are explicit and versioned.

- **Repeatability**  
  New projects start from the same disciplined baseline.

- **Domain agnostic**  
  Suitable for SaaS products, internal tools, regulated systems, and experiments.

---

## Repository Structure

```text
project/        # Governance, quality rules, agent role contracts (reusable)
.specify/       # Spec Kit memory and templates
.codex/         # Codex / Spec Kit execution configuration
docs/           # Framework documentation
specs/          # (created per project) product capabilities and features
