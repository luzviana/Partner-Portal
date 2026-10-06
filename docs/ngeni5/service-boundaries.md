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
