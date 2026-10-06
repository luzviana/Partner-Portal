# ADR-0004 Existing SSO capability integration

**Latest user scope:** [HubSpot-first priority plan](../priority-plan.md) supersedes old five-service/phase assumptions. AI Sales Support is cross-page with no menu item; Site Designer includes multisite; Site Designer/Discovery are deferred and not initialized. Existing review and control obligations remain.
- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Accountable roles: SSO owner + application owners + Security; named acceptance pending.
- EA v2: changes required against a60a88d; author revision awaits exact-commit v3; no approval recorded.
- User implementation approval: pending, no approval recorded.

## Context

EA catalogs SSO as the shared identity capability. SSO baseline `ad5337ceb5077afb3040a59ee939e959b81dcae3` includes ADR-001 (Keycloak selected subject to proof of concept and technical approvals), ADR-002 (decentralized application authorization), and ADR-003 (direct application authentication). This existing provider decision does not assert production readiness or authorize Partner-Portal configuration.

Each application initiates its approved OIDC flow and enforces local membership, roles and resource permissions. Existing identity sessions provide SSO. Portal discovery/navigation does not create access rights or make the portal a mandatory authentication intermediary. Identity self-service must not acquire a product launcher/catalog through this proposal.

## Proposed direction

Consume approved SSO contracts, retain service-local authorization and scoped workload identities.

## Alternatives

Existing SSO direct integration or vendor federation; capability change through SSO owner if needed.

## Evidence needed before decision

Obtain owner acceptance and supported claims/flows, lifecycle and native vendor SSO evidence.

## Consequences and current disposition

Proposed; affected owner acceptance pending. The proposal must account for operating cost, security/isolation, compatibility and rollback before adoption. Relevant findings belong in [review status](../reviews/status.md), and revisions must be reviewed against their exact commit. No accepted implementation decision is inferred from a draft document or a merged documentation PR.

## Author revision 1 response

Preserve direct application login and local grants. EA v2 resolved PP-EA-02 in design only. Provider acceptance, registration, named owners and runtime evidence remain pending. Remote SSO baseline fbd3b3f7406411155a4a9616df96540570ba4585 has the same three ADR contents according to pinned EA v2.

Incorporated design: [authority-and-lifecycle.md](../authority-and-lifecycle.md). Decision gate: OD-05 in [open decisions](open-decisions.md). Acceptance mapping and evidence are in the [finding register](../reviews/author-revision-1.md).
