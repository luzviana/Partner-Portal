# ADR-0006 Quote authority and solution handoff

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: Commercial + technical validator + package provider; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

Heterogeneous design tools need one trustworthy commercial result.

## Proposed direction

Immutable source packages and one quote authority; no dual authoritative price calculator.

## Alternatives

HubSpot CPQ, independent custom quote service, ERPNext or specialist CPQ after comparable fit tests.

## Evidence needed before decision

Verify technical rules, NRC/MRC, approval/revision API, license, partner access and integration recovery.

## Consequences and current disposition

Proposed; compared alternatives incorporated, hard-gate evidence and selection pending. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.

## Author revision 1 response

Evaluate HubSpot against QuoteWerks, conditional ERPNext and custom using common hard gates. Bind configuration digest/rule version and commercial evidence to quote revision; prohibit native CPQ edit/issue bypass. Choose exchange module/adapter/service with durable owner and TCO before R15, not automatically a separate runtime. R19-R24 execute proof only after approval.

Incorporated design: [quote-and-crm-controls.md](../quote-and-crm-controls.md). Decision gate: OD-03/09 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
