# ADR-0008 EA review and user implementation approval

**Latest user scope:** [HubSpot-first priority plan](../priority-plan.md) supersedes old five-service/phase assumptions. AI Sales Support is cross-page with no menu item; Site Designer includes multisite; Site Designer/Discovery are deferred and not initialized. Existing review and control obligations remain.
- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: User Cleber + EA + affected owners/Security as applicable; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
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

## Author revision 1 response

EA v2 changes-required report is acknowledged; this author revision requests v3, not approval. Coordinator alone routes the exact new commit. No messages, implementation, merges, procurement or configuration authorized. Silence remains no approval.

Incorporated design: [reviews/author-revision-1.md](../reviews/author-revision-1.md). Decision gate: All OD-01 through OD-10 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
