# ADR-0003 HubSpot CRM and synchronization

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Owner: Partner-Portal proposal author; accountable business/technical owners to be confirmed.
- EA review: pending, no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

HubSpot is the established CRM.

## Proposed direction

Retain CRM and propose company/contact/deal master mapping, durable adapter and reconciled summaries.

## Alternatives

Native HubSpot operations versus scoped integration projection; one account versus partner accounts.

## Evidence needed before decision

Inspect actual subscription/app/scopes, choose field writers, approvals and outage policy.

## Consequences and current disposition

CRM incumbent confirmed; ownership/sync design proposed. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.
