# ADR-0005 Customer solution isolation and deployment

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Owner: Partner-Portal proposal author; accountable business/technical owners to be confirmed.
- EA review: pending, no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

EA defaults to isolated solution state while the portal integrates multiple services.

## Proposed direction

No enterprise-wide customer data plane selected; compare declared deployment/isolation patterns.

## Alternatives

Corporate control plane plus isolated tools; approved multi-tenant product; per-solution deployment.

## Evidence needed before decision

Threat model, residence/retention, backup/keys, queues/indexes, operations and exception rationale.

## Consequences and current disposition

Proposed; no isolation exception granted. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.
