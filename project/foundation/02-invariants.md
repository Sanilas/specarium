# Operating Model Invariants

## Canonical Truth Sources (ordered)

1. spec/ (authoritative intent)
2. adr/ (authoritative decisions)
3. quality/ (authoritative gates)
4. docs/ (authoritative usage and runbooks)
5. code (implementation)

## Non-negotiables

- Spec-first: material change requires a spec delta.
- Docs-first completion: behavior change requires MkDocs update unless explicitly exempted.
- Test evidence: every material change requires executable verification unless explicitly exempted.
- Role encapsulation: agents modify only allowed scopes.
- Reproducible tools: Docker MCP Gateway is the baseline; marketplace MCP is non-foundational.

## Architectural posture (foundation-level)

- Container-first operability: the deliverable is a container that runs consistently.
- No hosting lock-in in the foundation.
- CI is mandatory; CD is optional until a staging provider is chosen.

## Change classification

- Trivial change: formatting, typos, non-behavioral refactors → may be exempt from spec delta.
- Material change: behavior, interfaces, configuration, architecture, deployment, security posture → requires spec delta + doc update + tests.
