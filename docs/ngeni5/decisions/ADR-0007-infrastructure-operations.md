# ADR-0007 Infrastructure and operating model

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Owner: Partner-Portal proposal author; accountable business/technical owners to be confirmed.
- EA review: pending, no approval recorded.
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
