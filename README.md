\# Specarium



\*\*Specarium\*\* is a spec-driven operating model and incubator for building software systems

with clarity, governance, and repeatable execution.



It provides a reusable, domain-agnostic foundation where product intent is captured as

specifications and systematically transformed into plans, tasks, and implementation —

with humans retaining ownership of meaning and decisions.



---



\## Why Specarium?



Most software projects fail not because of bad code, but because of:

\- unclear intent

\- missing governance

\- ad-hoc decisions

\- and fragile handoffs between planning and execution



Specarium addresses this by making \*\*specifications the primary source of truth\*\* and

by enforcing clear boundaries between:

\- governance

\- product intent

\- and execution



---



\## Core Principles



\- \*\*Spec-first\*\*: No meaningful change without a specification.

\- \*\*Human-owned meaning\*\*: AI assists execution, never defines intent.

\- \*\*Governance by design\*\*: Authority, quality gates, and constraints are explicit.

\- \*\*Repeatability\*\*: New projects start from the same disciplined baseline.

\- \*\*Domain agnostic\*\*: Works for SaaS, internal tools, regulated systems, and experiments alike.



---



\## Repository Structure



```text

project/        # Governance, quality rules, agent role contracts (reusable)

.specify/       # SpecKit memory and templates

.codex/         # Codex / SpecKit execution configuration

docs/           # Framework documentation

specs/          # (created per project) product capabilities and features



