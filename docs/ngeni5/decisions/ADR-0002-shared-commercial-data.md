# ADR-0002 Shared product and pricing authority

**Latest user scope:** [HubSpot-first priority plan](../priority-plan.md) supersedes old five-service/phase assumptions. AI Sales Support is cross-page with no menu item; Site Designer includes multisite; Site Designer/Discovery are deferred and not initialized. Existing review and control obligations remain.
- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: Catalog + Commercial + privacy/data policy owner; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

Multiple tools need consistent governed products and price evidence.

## Proposed direction

One logical authority per mastered field; provider APIs/exports only, classified eligibility and versioning.

## Alternatives

Shared corporate catalog; solution-local masters with published mappings; facade over HubSpot/ERP/PIM.

## Evidence needed before decision

Compare centralization criteria, data classes, blast radius, price confidentiality and exit.

## Consequences and current disposition

Proposed; EA scope/exception assessment pending. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.

## Author revision 1 response

Classify public specifications separately from partner/customer prices and costs. Select one field writer and approved sharing scope before R12/R13. Record revocation/cache/export/backup/hold bounds before real-data use; consumers use APIs/exports only.

Incorporated design: [authority-and-lifecycle.md](../authority-and-lifecycle.md). Decision gate: OD-02/07 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
