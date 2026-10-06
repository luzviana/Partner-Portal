# ADR-0008 EA review and user implementation approval

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Owner: Partner-Portal proposal author; accountable business/technical owners to be confirmed.
- EA review: pending, no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

User requires EA coordination and explicit approval before consequential implementation.

## Proposed direction

Continue documentation/research; record exact-commit review and findings; wait for explicit user scope approval.

## Alternatives

No implicit or time-based approval path.

## Evidence needed before decision

EA report, findings disposition/re-review, user approval reference, affected-owner/security approvals where applicable.

## Consequences and current disposition

Gate active by explicit user instruction; architecture decisions remain proposed. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.
