# ADR-0003 HubSpot CRM and synchronization

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: CRM administrator + CRM adapter operator; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
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

## Author revision 1 response

Use durable correlation and Uncertain/NeedsOperator states; delayed visibility never justifies duplicate create. Set retry/uncertainty/operator deadlines and field/grant ownership before R16/R18. Buyer acceptance, deal-won and ordering are separate from quote approval.

Incorporated design: [quote-and-crm-controls.md](../quote-and-crm-controls.md). Decision gate: OD-04/07 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
