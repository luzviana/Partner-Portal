# Source evidence and strategy traceability

## Authoritative inputs

- Task NGENI-5: enterprise architecture, service boundaries, OSS/paid choices, phased plan, actionable backlog and CTO presentation.
- User confirmation: local Platform_Strategy_Updated.pdf is the source, 24 physical pages.
- SHA-256: `fe6fd6bd2b90f74c245376e4a901cc1f9e02a7ec4430beb698ae488e6ab830d9`.
- User correction on 6 October 2026: independent entry points mean independent services with potentially different solutions; the portal integrates them; services may share product/pricing data; HubSpot is the existing CRM.
- User review gate: coordinate with Enterprise Architecture, deepen solution analysis, retain work in the repository/PR, and wait for EA review plus explicit user approval before consequential implementation. Silence is not approval.

The full PDF is available to the EA reviewer on the same authorized host. The exact local path was sent through the EA terminal handoff. It is not included in this public repository, and mockup customer/product/pricing details are not reproduced as production facts. A reviewer without source access must report that blocker, not claim PDF alignment.

## Current coverage and bounded proposed deferrals

No capability is implemented. Planned means backlog/design scope, not delivery evidence. Deferrals below are author proposals awaiting Product/Cleber acceptance; none is an accepted exception. Until accepted or funded, the omitted capability is excluded from pilot claims and cannot be sold as full strategy delivery. Exit is a specific scope/rule/feed/content decision and small funded backlog before enabling the capability; no invented calendar approval date.

| Physical pages | Intent | Planned slice / item IDs | Explicit limit, owner and revisit gate |
| --- | --- | --- | --- |
| 1–3 | Independent connected tools | Five business services, direct access and portal projection; R01/R06/R10/R39 | Shared dependencies explicit; runtime/selection decisions OD-01/06/08 remain pending |
| 4–5 | Opportunity/site intake | Account-scoped HubSpot references and isolated staged site import; R02/R03/R16-R18/R31 | Actual write/grant policy OD-04 before connector use; no automatic record creation |
| 6–7 | Floor-plan design and device placement | Calibrated geometry/BOM export R27/R28; separately gated RF extension R40 | Camera field of view, IoT placement, edge sizing and full RF accuracy are not proven. Solutions/Product must define representative fixtures, domain criteria and funded tasks before advertising/enabling each non-Wi-Fi family |
| 8–9 | Discovery and reviewed dispositions | Observation imports R29/R30; separately authorized active collection R41/R42 | Import does not equal scanning; universal device/protocol coverage deferred pending measured inventory and Product/Security scope |
| 10–11 | AI contextual solution assistance | Entitled retrieval and reviewed proposals R34-R37 | 50-case evaluation is a scoped fixture, not general correctness; data/model permissions and first-use controls gate launch |
| 12–15 | Marketplace, comparison and human battle cards | Offers/eligibility/selection R12-R14; governed source content R34 | Human comparison/battle-card UI is deferred from thin pilot, not delivered by AI indexing. Product/Catalog must specify comparison fields, versioned human views, rights and acceptance tasks before expanded Marketplace claim; revisit at R08/R39 |
| 16 | Technical rule families | Versioned digest and port/power/license seed R19-R24 | GPU capacity, SD-WAN bandwidth/resilience, IoT protocol/power and additional compatibility families are excluded until technical owner supplies rule sources/expected cases and funds validation. Unsupported products/configurations cannot receive “technically valid” quotes; OD-03/R08 restrict pilot catalog accordingly |
| 17 | Multisite profiles/overrides | Versioned 60-site fixture R31-R33 | Broader scale and vendor-specific semantics require new evidence; Product decides at R39 |
| 18–19 | Common quote and branded proposal | One authority, immutable approved version, native-edit/expiry guards R19-R24 | No automatic deal-won/order/payment workflow; R49 separate business case |
| 20–21 | Customer lifecycle breadth | HubSpot plus one explicitly selected source-owned lifecycle feed R43 | Full asset/license/contract/support/renewal breadth deferred pending OD-10 source/owner/field map and small tasks. No detailed CMDB replication; Product/data owners decide before R43/R44 release claims |
| 22–23 | Business/operational report breadth | One named report with genuine PDF/Excel/CSV/PPT proof R44/R45 | Portfolio, partner performance, pipeline, utilization and other report families require Product-approved metric/source/filter definitions and privacy review; revisit R08/R45 before declaring report suite complete |
| 24 | Partner human resources | R34 governs source knowledge only | Human resource library/navigation/download experience is deferred, not equated with retrieval. Product/content owner must select resource types, publishing/rights/expiry and accessible human experience, then fund tasks before resources launch; revisit R08/R39 |

R01/R08 record included/excluded scope; R19 rejects uncovered rule families; R39/R43/R45 verify that claims match actual accepted scope. If Cleber does not accept a narrowed pilot, scope must be expanded and re-estimated before implementation approval. Mockup quantities are not measured scale, prices, current vendor rights or revenue.

## Exact EA revision inputs

Author revision 1 read with `git show`, not mutable working files: `review-v2.md`, detailed `review-v1.md`, and `build-versus-buy-v1.md` under `reviews/partner-portal/2026-10-06/` at EA commit `5b9fc35daad180e05ee564eb80bbf16eff6124bb`. Reviewed Partner-Portal baseline: `a60a88da5d6e48c212309fc9ac9cea6d4c6e7452`. Source PDF hash/access remains confirmed by that report; no replacement upload requested. The source is unchanged and not republished.

EA v2 checked remote SSO `fbd3b3f7406411155a4a9616df96540570ba4585` and confirmed ADR-001/002/003 match earlier local `ad5337ceb5077afb3040a59ee939e959b81dcae3`. Design alignment is not production readiness. S1 in historical artifacts means the PDF; S2 means the user brief; current vendor evidence and primary links are in [research evidence](solution-research-evidence.md).

## EA reference baseline inspected

Repository: https://github.com/luzviana/ngenious-enterprise-architecture

Inspected local HEAD: `d07714f19ee726b1aae4352047036a88dad0441a`. The reviewer must verify whether a newer accepted baseline applies.

Relevant paths: `docs/standards/tenancy-and-customer-isolation.md`, `docs/standards/api-and-event-contracts.md`, `docs/standards/security-audit-secrets-and-approvals.md`, `catalogs/capabilities/sso.md`, `docs/governance/centralization-decision-criteria.md`, `docs/governance/cross-repository-change-procedure.md`, `docs/governance/pull-request-review-process.md`.

ADR-0004 is scoped to the Ole Media pilot. Its customer-dedicated ingress example is evidence to assess, not inherited approval for Partner-Portal.
