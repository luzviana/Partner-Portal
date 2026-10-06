# Proposed service boundaries

**Proposed only.** Independence is established by the user. Deployment topology and shared capability scope require EA review.

| Service | Owned state and policy | Consumed contracts | Independent acceptance |
| --- | --- | --- | --- |
| Marketplace | Selection, comparison and offer presentation | Product/offer lookup, eligible price evaluation, package submission | Native access and export without portal |
| Floor Plan | Files, scale, geometry, placements, simulations | Product mapping and package export | Native editor with source version and data exit |
| Discovery | Observations, scan/import jobs and assessment evidence | Approved collector ingest, canonical mapping, package export | Authorized assessment without portal |
| AI Builder | Solution-local conversations, retrieval and tool traces | Entitled catalog/content, typed proposal tools | Native assistance; no commercial approval authority |
| Multi-Site | Sites, profiles, overrides and expansion revisions | Product map and package handoff | Native workspace and reproducible expansion |
| Portal/BFF | Session composition, navigation and workflow status | Existing SSO; scoped service APIs | Portal failure does not remove native service access |
| Product/Pricing | Governed product/offer IDs, eligibility and price policy | Master adapter and publication contracts | One writer per mastered field; no cross-product SQL |
| Solution Exchange | Immutable submitted packages and handoff status | Package schema and service identities | Review whether an independent runtime is needed versus a provider-owned library/adapter |
| Quote/Proposal | Exact quote versions, approvals and rendered artifacts | Package, technical validation, authoritative pricing and CRM summary | One quote authority; independent of source tool availability |
| HubSpot adapter | Account-scoped mappings, sync state and command ledger | HubSpot CRM plus governed internal facade | Reconciliation without a competing CRM master |

## Deployment scope is an open decision

Business-service independence does not automatically select one multi-customer SaaS data plane. Compare a scoped corporate Partner-Portal capability, independently deployed customer-solution services, and a hybrid with shared non-sensitive catalog plus isolated solution state. Preserve solution-specific files, inventory, topology, AI context, credentials, telemetry and backups unless a reviewed ADR permits a narrower exception.

The user's permission to share product/pricing data does not authorize sharing detailed customer inventory or CRM visibility across solutions. State isolation, procurement, operational ownership and pricing confidentiality need separate evidence. Prove each vendor's tenancy model rather than treating an application tenant ID as sufficient.

## Ownership and failure rules

Services may share repository conventions and managed infrastructure only within an approved boundary. No consumer writes or reads another product's database. Native vendor APIs remain implementation surfaces behind governed contracts for external/customer integrations. Native UI access is limited to approved users and vendor roles.

Each boundary needs a named provider owner, consumer list, service identity, contract version, independent release/rollback, restore/export path and failure behavior. No additional repository, common gateway or enterprise-wide broker is selected by this draft.

## Authority and first-use constraints

The [authority/placement/lifecycle model](authority-and-lifecycle.md) is part of every boundary. A service workspace belongs to one solution/environment, not merely a partner tenant. Local grants determine access; portal links are only projections. Discovery owns observations, never implicitly iTop's detailed inventory. Lifecycle/reporting may hold only approved minimized projections. [Release checklists](release-and-operations.md) apply before each service's first exposure; every vendor must pass [selection gates](solution-analysis.md).

## OD-09 package exchange alternatives before R15

| Form | Provider/consumers and benefits | Burden / selection evidence |
| --- | --- | --- |
| Provider-owned package module | Quote provider owns durable submitted packages; five independent tools consume its versioned submission/read contract. Lowest added runtime count. | Quote outage affects intake; retention/export and independent contract evolution required. Proposed first option to evaluate, not selected. |
| Contract plus source/target adapters or reusable library | Schema owned by named package provider; source services retain artifacts, target records accepted copy/digest. Avoid central store. | Library alone cannot own durable receipt, replay or audit. Allocate these to providers; prove historical quote survives source unavailability/deletion policy. |
| Separate exchange service | Named exchange provider owns intake/receipts, durable packages and fanout; tools and quote consume it independently. | Extra identity/store/backup/on-call and cost. Justify reuse/failure value and funded ownership over module approach. |

Technical lead records consumer inventory, package custodian, retention, failure/recovery, support and incremental three-year TCO in R05/R08. OD-09 is a hard predecessor to R15. No new runtime/repository is implied by “exchange”; R50 only revisits measured decomposition later. Five independent business services persist under every option.
