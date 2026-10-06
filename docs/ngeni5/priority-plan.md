# Reviewed portal scope and action priorities

Author revision 2, based on Cleber's latest reviewed feature list. This user direction supersedes the earlier five-independent-entry-point/menu model and old P0–P3 roadmap. It authorizes planning changes, not implementation, configuration, procurement, scans or deployment. EA must assess the revised boundaries through coordinator routing; prior reports do not approve this new scope.

## Current portal experience

| Surface | Confirmed scope | Delivery priority |
| --- | --- | --- |
| Home | HubSpot-sourced partner information, sales, leads, promotions and aggregated opportunities. Customers are included here. | 1 |
| Opportunities | HubSpot-backed opportunity details, prices, BOMs, proposal revisions and quote status. Prices/quotes are not a separate menu destination. | 1 integration definition and read journey; 2 proposal generation |
| Marketplace | List products we sell, select quantities and prepare a proposal valid for 30 days. Persist price and BOM with the proposal in HubSpot. No direct sale/checkout/payment. | 2 |
| Resources | Findable HubSpot files, including battle cards. No separate Battle Cards menu. | 1 content/access integration and basic find/open journey |
| AI Sales Support | Mandatory agent available on every portal page, with page/opportunity context. No menu item and no separate standalone AI application requirement. | 3 |
| Site Designer | Former Floor Plan Designer plus multi-site profiles/overrides inside the same capability. No separate Multi-Site Designer. | 4, deferred; do not initialize |
| Discovery | Find items on an authorized network, beyond networking equipment alone. | 4, deferred; do not initialize |

Initial navigation: Home, Opportunities, Marketplace and Resources. AI Sales Support is a persistent support control. Site Designer/Discovery need no routes, scaffolds, credentials, provisioning or placeholders now. Do not create an agent runtime yet; mandatory agent delivery follows review/approval and Priorities 1–2.

## Priority 1 — define and prove the HubSpot integration

First deliverable is the integration specification and field/access matrix, not UI scaffolding. Inventory actual HubSpot account, subscriptions, object/property/association model, supported APIs, app type/scopes, available test environment and content access. No account entitlements or partner mapping are assumed. Agree which HubSpot records represent partner, customer, lead, opportunity, promotion and resource. Proposed opportunity mapping is a Deal, subject to CRM owner confirmation; “lead” need not mean the Leads API object.

Home is a portal view of HubSpot data, with record links, source timestamps and scoped totals. “From HubSpot” is interpreted as HubSpot-sourced content rendered by the portal, not an assumed iframe or licensed embedded HubSpot dashboard. Confirm metric definitions: what counts as sales, leads and opportunities; date window; currency treatment; visibility and de-duplication. Never sum quote revisions as new sales. Promotions require an actual maintained HubSpot source/validity model; do not invent a Promotions object or infer eligibility from visibility.

Use a server-side HubSpot adapter and application-local partner/customer/opportunity grants. SSO identity is not CRM record permission. Browser and agent receive no HubSpot administrative token. List, aggregate, record, file and agent tool paths enforce the same scope. Home outage state distinguishes unavailable from a real zero. Reconciliation uses supported notifications plus bounded re-read; unknown write outcome never permits duplicate create.

Resources need an agreed folder/taxonomy and metadata (title, type, product/category, audience, version, validity, source file ID). Start with findability through authorized names/metadata and filters; full-text indexing is a separate decision. Private files require authorized temporary access; a folder or signed link alone does not define partner permissions. Battle cards are human-readable Resources content and can later ground AI. Revoke cached metadata/download access with the source. No separate document repository as master.

Exit: owner-accepted HubSpot map, Home and Opportunities read contract, Resources access contract, error/recovery cases, provider/SSO acceptance and approved synthetic-versus-real proof plan. The future implementation gate proves the scoped read journey and resource access before Priority 2 launch. Completion of this planning document is not proof that the integration works.

## Priority 2 — simplified Marketplace and 30-day proposal

Provisional recommendation: thin custom catalog/selection experience over the confirmed catalog source, integrated with HubSpot Opportunities and a governed proposal workflow. It avoids introducing order, inventory-fulfilment, seller onboarding or checkout functions absent from this brief. Product/price source is currently unknown; HubSpot is the first source to evaluate if already maintained there. Keep one price authority.

Required journey: choose authorized opportunity/customer, browse products we sell, select quantities, calculate with authoritative prices, review BOM and proposal, apply required commercial/technical approval, persist a version in HubSpot and show it under Opportunities. No website payment, direct purchase, auto-order or automatic deal-won. Proposal creation and customer sending are separate permissions; automatic sending is not authorized by the brief.

Exactly 30 days of proposal validity is confirmed. Proposed anchor is issuance after approval and verified HubSpot persistence, not draft creation. Commercial must confirm calendar/time-zone/end-of-day semantics before implementation. Record issued_at and expires_at, and render the same expiry in portal, document and HubSpot representation. Test day-boundary and expired-revision behavior. An expired proposal cannot be reused as a current offer; renewal creates a new priced/approved revision. Catalog updates do not silently alter an issued proposal. Commercial must establish whether offer prices can be honored for the full period; a shorter supplier price validity blocks issuance until a supported 30-day policy exists, rather than silently shortening the user's requirement.

The durable HubSpot representation must include structured BOM line items (canonical SKU/product, description, quantity, unit, price, currency, recurring term if applicable), totals, version, validity, authority and proposal artifact. Preferred route is supported native HubSpot quoting if the account and workflow fit. If unavailable, evaluate a deal-associated proposal record/artifact and separately versioned structured BOM using supported account capabilities. A URL or aggregate amount alone does not satisfy “proposal sits in HubSpot with price and BOM.” No custom-object entitlement or unlimited attachment/API rights assumed. Confirm that revisions retain previous price/BOM evidence and cannot duplicate revenue.

Native quote edit bypass, grants, expiry, failed partial association, timeout after remote success and delayed visibility remain acceptance cases. A locally generated document cannot claim “saved to HubSpot” until readback verifies every required association/line/version. HubSpot failure leaves a recoverable pending draft, never a fake issued proposal.

## Priority 3 — mandatory AI Sales Support agent

Agent UI is available across Home, Opportunities, Marketplace and Resources. A separately permissioned agent backend can be an internal capability; it has no menu item and need not be a separate product. Carry only authorized current page/customer/opportunity context and visibly identify the active context. Clear or reauthorize context when switching customers/opportunities or revoking a grant.

Initial tools: read authorized CRM context, find permitted Resources/battle cards, explain catalog products/prices from governed evidence, and propose a BOM/proposal draft for human review. Agent responses link to sources and distinguish unknown/unavailable data. All tool execution reauthorizes server-side. No arbitrary HubSpot API proxy, autonomous price approval, direct table write, purchase, deployment, scan or customer-send capability. Future CRM writes require explicit reviewed action previews, user confirmation, narrow service contract and durable ledger. Mandatory support does not make the model a commercial authority.

Compare managed inference plus owned orchestration with self-hosted inference only against actual data/privacy, operational and cost needs. First prove cross-customer context isolation, prompt-injection resistance, source revocation, hallucinated-price refusal, all-page availability and manual workflows during AI outage. Priority 3 acceptance is required for completion of the initial Priority 1–3 release, even if the first read-only HubSpot increment arrives earlier.

## Priority 4 — defer Site Designer and Discovery

Site Designer combines floor/site design with multisite profiles, overrides and BOM expansion. Reassess one domain boundary later; the old requirement for a separate multisite service is withdrawn. Discovery aims to find all reachable/observable items in the authorized network, including endpoints, servers, printers, IoT and network devices. Import-only assessment does not fulfill that outcome. Future scope must state network segments, credentials, protocols, device classes, coverage measurement, unknown/unreachable devices, safe scan limits and operator stop controls. Do not promise universal detection of powered-off, isolated or blocked devices. No initialization or vendor trial now. Both capabilities await explicit reactivation after priorities 1–3 and their own approval gates.

## Immediate planning actions and owners

1. CRM administrator + Product: account/capability inventory and Home/Opportunities/Resources mapping (R02/R03/R51/R53).
2. Application/SSO/Security owners: partner/customer/opportunity grants and private resource access (R06/R11).
3. Commercial + Technical lead: confirm catalog/price source, 30-day policy and HubSpot proposal/BOM representation (R04/R05/R56).
4. Delivery: make Priority 1 integration evidence the prerequisite for Marketplace delivery; re-estimate only active scope (R08/R54).
5. Product + AI owner: scope the mandatory agent tools and cross-page context; implementation follows Priority 2 acceptance (R58/R59/R60).

Missing business inputs remain owner gates, not silent approvals. Old 133-day seed estimates and previous calendar ranges do not estimate this scope. Existing EA safety/control findings remain relevant; menu/service consolidation does not waive isolation, lifecycle, contract, quote-integrity or first-use evidence.
