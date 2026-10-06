# Source evidence and strategy traceability

## Authoritative inputs

- Task NGENI-5: enterprise architecture, service boundaries, OSS/paid choices, phased plan, actionable backlog and CTO presentation.
- User confirmation: local Platform_Strategy_Updated.pdf is the source, 24 physical pages.
- SHA-256: `fe6fd6bd2b90f74c245376e4a901cc1f9e02a7ec4430beb698ae488e6ab830d9`.
- User correction on 6 October 2026: independent entry points mean independent services with potentially different solutions; the portal integrates them; services may share product/pricing data; HubSpot is the existing CRM.
- User review gate: coordinate with Enterprise Architecture, deepen solution analysis, retain work in the repository/PR, and wait for EA review plus explicit user approval before consequential implementation. Silence is not approval.

The full PDF is available to the EA reviewer on the same authorized host. The exact local path was sent through the EA terminal handoff. It is not included in this public repository, and mockup customer/product/pricing details are not reproduced as production facts. A reviewer without source access must report that blocker, not claim PDF alignment.

## Traceability

| PDF pages | Requirement | Draft response | Backlog evidence |
| --- | --- | --- | --- |
| 1-2 | Independently usable tools and common experience | Five independent business services; portal composes access/context | R01, R07, R10, R39 |
| 4-5 | Opportunity context and site import | HubSpot references, scoped projection, staged site import | R02-R03, R16-R18, R31 |
| 6-7 | Floor plans and profiles | Independent planning solution, canonical device map, no unsupported RF claims | R27-R28, R40 |
| 8-9 | Discovery and asset dispositions | Independent observations and reviewed KEEP/REUSE/UPGRADE/REPLACE/ADD | R29-R30, R41-R42 |
| 10-11 | AI solution assistance | Independent AI context, governed retrieval and reviewed typed proposals | R34-R37 |
| 12-15 | Marketplace and battle cards | Governed product authority, partner eligibility and content provenance | R12-R14, R34 |
| 16 | Technical compatibility | Deterministic versioned technical rules | R19-R21 |
| 17 | Multisite expansion | Independent sites/profiles/overrides and versioned package | R31-R33 |
| 18-19 | Quote and proposal | One commercial authority, immutable approved snapshot | R13, R18-R24 |
| 20-21 | Customer lifecycle | HubSpot CRM plus minimal source-linked projections | R03, R16-R18, R43 |
| 22-24 | Reports and resources | Isolated reporting, export fidelity and governed knowledge | R34, R44-R45 |

Mockup values are not measured load, vendor quotes, validated RF accuracy or actual revenue. Scheduling, staffing, SLOs and candidate preferences remain hypotheses.

## EA reference baseline inspected

Repository: https://github.com/luzviana/ngenious-enterprise-architecture

Inspected local HEAD: `d07714f19ee726b1aae4352047036a88dad0441a`. The reviewer must verify whether a newer accepted baseline applies.

Relevant paths: `docs/standards/tenancy-and-customer-isolation.md`, `docs/standards/api-and-event-contracts.md`, `docs/standards/security-audit-secrets-and-approvals.md`, `catalogs/capabilities/sso.md`, `docs/governance/centralization-decision-criteria.md`, `docs/governance/cross-repository-change-procedure.md`, `docs/governance/pull-request-review-process.md`.

ADR-0004 is scoped to the Ole Media pilot. Its customer-dedicated ingress example is evidence to assess, not inherited approval for Partner-Portal.
