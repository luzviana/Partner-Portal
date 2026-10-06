# ADR-0005 Customer solution isolation and deployment

**Latest user scope:** [HubSpot-first priority plan](../priority-plan.md) supersedes old five-service/phase assumptions. AI Sales Support is cross-page with no menu item; Site Designer includes multisite; Site Designer/Discovery are deferred and not initialized. Existing review and control obligations remain.
- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: Product + Security + EA + solution data owners; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
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

## Author revision 1 response

Recommend corporate navigation/public catalog plus isolated solution/environment state. Explicit partner/customer/solution/workspace authorities, placement and three-axis restore/support tests apply. Select topology before R09 or sensitive SaaS import; RLS/schema/vendor organization IDs alone prove neither restore nor failure isolation. No exception is granted.

Incorporated design: [authority-and-lifecycle.md](../authority-and-lifecycle.md). Decision gate: OD-01/07 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
