# Source evidence and strategy traceability

## Authoritative inputs

- Task NGENI-5: enterprise architecture, service boundaries, OSS/paid choices, phased plan, actionable backlog and CTO presentation.
- User confirmation: local Platform_Strategy_Updated.pdf is the source, 24 physical pages.
- SHA-256: `fe6fd6bd2b90f74c245376e4a901cc1f9e02a7ec4430beb698ae488e6ab830d9`.
- User correction on 6 October 2026: independent entry points mean independent services with potentially different solutions; the portal integrates them; services may share product/pricing data; HubSpot is the existing CRM.
- User review gate: coordinate with Enterprise Architecture, deepen solution analysis, retain work in the repository/PR, and wait for EA review plus explicit user approval before consequential implementation. Silence is not approval.

The full PDF is available to the EA reviewer on the same authorized host. The exact local path was sent through the EA terminal handoff. It is not included in this public repository, and mockup customer/product/pricing details are not reproduced as production facts. A reviewer without source access must report that blocker, not claim PDF alignment.

## Latest scope precedence and traceability

The latest reviewed user list supersedes the earlier interpretation where AI and Multi-Site were separate independent entry points. The original 24-page PDF and hash are unchanged; this is a user-directed scope revision, not a replacement source. No feature is implemented.

| Source intent / physical pages | Current user direction | Priority / backlog |
| --- | --- | --- |
| Connected experience, pp. 1–3 | Home/Opportunities/Marketplace/Resources navigation; agent available on all pages, no AI menu | P1 R01/R10/R51-R55; P3 R58-R60 |
| CRM context, pp. 4–5 and 20–21 | HubSpot-sourced Home aggregates partner/sales/leads/promotions/opportunities and includes customers; field/metric mapping first | P1 R02/R03/R16/R17/R51/R52/R54; old R43 superseded |
| Catalog/compare, pp. 12–15 | Marketplace lists products we sell and generates a proposal, not a direct sale; battle cards move to Resources | P2 R04/R12-R14; P1 R53/R55 |
| Quotes, pp. 18–19 | Prices/quotes in Opportunities; complete proposal price/BOM in HubSpot; 30-day validity confirmed | P2 R05/R18-R26/R56/R57 |
| Resources, p. 24 | Findable structure of files in HubSpot, including human battle cards | P1 R53/R55; AI knowledge R34 follows |
| AI assistance, pp. 10–11 | Rename to AI Sales Support, mandatory governed agent on every active page | P3 R34-R39/R58-R60; initial release cannot omit it |
| Floor/site design, pp. 6–7 and multisite p. 17 | Rename Site Designer and combine multisite concept inside it | P4 R27/R28/R31-R33/R40; do not initialize |
| Discovery, pp. 8–9 | Discovery finds all observable items on authorized network; import-only does not meet full goal | P4 R29/R30/R41/R42; no scans/initialization now |
| Technical rules, p. 16 | Retain exact configuration/approval integrity for included proposal products; broader design families later | P2 R19-R24; no unsupported validity claims |
| Reports, pp. 22–23 | Home metrics first, broader reporting later with separate scope | P1 R51/R52; R44/R45 parked |

The latest direction explicitly defers Site Designer and Discovery, and removes prior proposed deferral of the basic human Resources/battle-card experience. Additional full-text search, broad reporting, non-Wi-Fi simulation and rule families still require scope decisions. Mockup figures remain illustrative, not measured capacity or prices.

## Exact EA revision inputs

Author revision 1 read with `git show`, not mutable working files: `review-v2.md`, detailed `review-v1.md`, and `build-versus-buy-v1.md` under `reviews/partner-portal/2026-10-06/` at EA commit `5b9fc35daad180e05ee564eb80bbf16eff6124bb`. Reviewed Partner-Portal baseline: `a60a88da5d6e48c212309fc9ac9cea6d4c6e7452`. Source PDF hash/access remains confirmed by that report; no replacement upload requested. The source is unchanged and not republished.

EA v2 checked remote SSO `fbd3b3f7406411155a4a9616df96540570ba4585` and confirmed ADR-001/002/003 match earlier local `ad5337ceb5077afb3040a59ee939e959b81dcae3`. Design alignment is not production readiness. S1 in historical artifacts means the PDF; S2 means the user brief; current vendor evidence and primary links are in [research evidence](solution-research-evidence.md).

## EA reference baseline inspected

Repository: https://github.com/luzviana/ngenious-enterprise-architecture

Inspected local HEAD: `d07714f19ee726b1aae4352047036a88dad0441a`. The reviewer must verify whether a newer accepted baseline applies.

Relevant paths: `docs/standards/tenancy-and-customer-isolation.md`, `docs/standards/api-and-event-contracts.md`, `docs/standards/security-audit-secrets-and-approvals.md`, `catalogs/capabilities/sso.md`, `docs/governance/centralization-decision-criteria.md`, `docs/governance/cross-repository-change-procedure.md`, `docs/governance/pull-request-review-process.md`.

ADR-0004 is scoped to the Ole Media pilot. Its customer-dedicated ingress example is evidence to assess, not inherited approval for Partner-Portal.
