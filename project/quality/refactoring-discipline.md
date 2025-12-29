# Refactoring Discipline

## Purpose

This document defines **how refactoring must be performed**.
It prevents semantic drift, accidental feature introduction, and quality erosion.

Refactoring is classified as **Class B change**.

---

## Definition

Refactoring is:

- behavior-preserving
- semantics-preserving
- externally observable behavior must not change

If behavior changes, the work is **not refactoring** and must be reclassified.

---

## Mandatory Rules

1. **No Mixed Changes**

   - Refactoring must not introduce new features
   - Refactoring must not fix bugs
   - Feature or bug changes require a separate change classification

2. **Small, Reversible Steps**

   - Changes must be incremental
   - Each step must leave the system in a working state
   - Prefer multiple small commits over large rewrites

3. **Tests First or Characterization Tests**

   - Existing behavior must be protected by tests
   - If no tests exist, characterization tests must be added before refactoring

4. **Keep the Build Green**
   - Code must compile
   - Tests must pass at every commit boundary

---

## Allowed Refactoring Techniques

Examples include:

- renaming for clarity
- method extraction
- duplication removal
- modularization
- dependency inversion
- internal API cleanup

---

## Large Refactorings

For large or risky refactorings:

- Use branch-by-abstraction or parallel structures
- Introduce seams before moving logic
- Decommission old paths only after parity is proven

---

## Documentation Requirements

Each refactoring must include:

- motivation (code smell, maintainability issue)
- confirmation that behavior is unchanged
- link to tests validating equivalence

This information must be visible in:

- PR description or
- commit message

---

## Enforcement

Refactoring without adherence to this discipline is considered a **process violation** and must be rolled back.
