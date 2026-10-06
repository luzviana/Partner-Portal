# ADR-0001 Independent business services

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Owner: Partner-Portal proposal author; accountable business/technical owners to be confirmed.
- EA review: pending, no approval recorded.
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
