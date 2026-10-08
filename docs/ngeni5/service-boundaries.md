# Revised portal and capability boundaries

[P1–P3 detailed architecture](integration-architecture-p1-p3.md) now proposes deployment boundaries: portal/integration backend, durable worker and separately isolated AI runtime. These refine the assessment below; none is approved for implementation.

Author revision 2. User-approved feature priority is distinct from implementation approval. [Priority plan](priority-plan.md) supersedes the earlier mandatory five-service topology. These are proposed ownership boundaries, not a commitment to a runtime per row.

| Surface/capability | Owner and state | Integration and deployment assessment |
| --- | --- | --- |
| Home | Portal view of partner/customer/sales/lead/promotion/opportunity data | HubSpot authoritative. Scoped server projection and cache with freshness. No independent Customers master/app |
| Opportunities | Portal workflow for HubSpot opportunity, BOM, price and proposal revisions | Deal mapping proposed pending account inspection. Single proposal authority; stored price/BOM in HubSpot. Not a second CRM |
| Resources | Human find/open UI for HubSpot files, including battle cards | HubSpot file source plus minimal index/metadata if needed. Rights and per-partner access through adapter |
| Marketplace | Canonical product presentation and temporary selections | Thin UI/provider module first. Product/price master confirmed before persistence; Opportunities owns proposal workflow. No direct sales engine |
| AI Sales Support | Agent conversations, scoped context, grounded responses and proposed actions | Always available on active portal pages, no menu item. Governed agent backend/tools; separate runtime only for isolation/operations benefit |
| HubSpot adapter | Mappings, scoped reads, command/reconciliation ledger | Provider-owned facade. No browser/model CRM credentials. Runtime form chosen with operating owner, no unnecessary gateway |
| Product/pricing authority | One writer per field and versioned prices | Existing master/HubSpot first assessment. APIs or governed publication; no cross-product SQL |
| Proposal/BOM module | Exact versions, approvals, 30-day validity and artifacts | Native HubSpot capability if proven; supported fallback must preserve full versioned BOM/price in HubSpot. Do not introduce competing totals |
| Site Designer | Future geometry/sites/profiles/overrides and simulations | Floor plan and multisite combine into one capability. Priority 4 deferred, no separate multisite service initialization |
| Discovery | Future authorized collection of all observable network items and assessment evidence | Priority 4 deferred. Imports may supplement discovery but cannot replace active network discovery outcome |

Initial deployment assessment: portal UI and server-side integration/application capabilities, using existing SSO. Isolate risky processing, secrets and customer scope as required. Whether catalog, proposal, agent or adapter warrant separate runtimes remains an EA/operating-owner decision. A source repository, menu screen and microservice are different boundaries.

Default detailed customer state remains solution/environment scoped; rights to common product/pricing data do not extend to CRM visibility, resources or AI context. Apply [authority/lifecycle](authority-and-lifecycle.md), [contracts](contracts.md) and [first-use gates](release-and-operations.md) to any implementation form. Native access for future purchased tools remains evaluated where useful; the AI service no longer requires a standalone application.

Package exchange remains a contract question: provider-owned proposal/BOM module, source/target adapter or separate service. For current Marketplace-to-HubSpot use, evaluate the module/adapter first. A separate durable exchange is justified only by actual consumers, retained evidence, independent recovery, funded owner and incremental TCO. R05 records that decision before R15. Future Site Designer export must fit the agreed contract when explicitly reactivated.
