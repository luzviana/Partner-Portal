# ADR-0001 Independent business services

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: Product + each service owner; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

User requires five independently usable services, each possibly supplied by a different solution.

## Proposed direction

Five named business boundaries with native access, source ownership and supported contracts.

## Alternatives

Single modular application is superseded; separate SaaS/self-hosted/custom solutions remain candidates.

## Evidence needed before decision

Define each operating owner and whether source repository and deployment separation are needed.

## Consequences and current disposition

User requirement confirmed; implementation form not approved. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.

## Author revision 1 response

Five independent business services remain a confirmed requirement; internal modules are not automatically independent runtimes. No selected vendor or topology follows from this requirement.

Incorporated design: [service-boundaries.md](../service-boundaries.md). Decision gate: OD-01/06/08 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
