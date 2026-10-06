# ADR-0007 Infrastructure and operating model

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: Platform + Security + Delivery + service operators; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

Independent services add failure boundaries, vendor dependencies and support effort.

## Proposed direction

Managed infrastructure is a candidate, with scoped stores/credentials and independent lifecycle.

## Alternatives

Approved existing platform, vendor SaaS, self-managed OSS; no Kubernetes or new gateway commitment.

## Evidence needed before decision

Named on-call/support, TCO, capacity/SLO, recovery drills, cloud choice and contract compatibility.

## Consequences and current disposition

Proposed; staffing and timing unapproved. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.

## Author revision 1 response

Use SYN versus REAL first-exposure checklists and CON before each first consumer. Name accountable operators before use; R47/R48 cannot introduce controls too late. Re-estimate expanded backlog and journey reliability using vendor failure, recovery and staffing evidence; no cloud/SLO/calendar selected.

Incorporated design: [release-and-operations.md](../release-and-operations.md). Decision gate: OD-08 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
