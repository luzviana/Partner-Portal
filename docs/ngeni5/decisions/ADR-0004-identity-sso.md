# ADR-0004 Existing SSO capability integration

- Status: **Proposed**, except the explicit review gate which applies immediately.
- Date: 2026-10-06
- Owner: Partner-Portal proposal author; accountable business/technical owners to be confirmed.
- EA review: pending, no approval recorded.
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
