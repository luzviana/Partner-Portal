# CTO decision brief — author revision 1

**Decision requested now: review the revised design, not authorize implementation.** EA v2 identified five remaining blockers. This revision adds concrete designs and pre-use evidence gates; coordinator will route the exact commit for EA v3. Human EA/affected-owner/Security and explicit Cleber approval remain pending. No procurement, configuration, deployment or merge is authorized.

## 1. Product shape

The portal integrates five independent services, each with its own usable interface and possibly a different solution. It does not become the identity or permission authority. Retain HubSpot as CRM and consume existing SSO's direct-login model. Each application owns grants. Shared commercial data use governed owner APIs, not shared table access.

## 2. Protect customer solutions, not just partner tenants

One partner can serve multiple unrelated customers; different partners may collaborate on one customer with different permissions. Explicit customer/solution/environment/workspace bindings and local grants protect these cases. Recommend scoped public catalog/navigation with isolated detailed solution state. Topology, support, restore and lifecycle policies require owner approval before use; SaaS organization labels alone do not prove isolation.

## 3. Compare real alternatives before buying or building

Marketplace: Medusa and CloudBlue against thin custom. Quotes: HubSpot against QuoteWerks, with ERPNext conditional on a wider ERP need and custom as an evidence-backed alternative. Planning/discovery: specialist tools versus explicitly limited custom/import paths. Multi-Site likely benefits from owned profile/override logic; test supported vendor extensions before deciding. Compare managed versus self-hosted AI with the same evaluation and cost basis.

No candidate passes by feature list alone. Rights, SSO, isolation/recovery, API/export fidelity, lifecycle and operator ownership are hard gates. Prices/account entitlements are unknown. Unknowns block selection or require an explicit narrowed capability scope. Three-year cost includes people, manual handoffs, stewardship, support, assurance and exit.

## 4. Make quote trust enforceable

Technical proof binds the exact configuration digest and rule version. Price evidence and approval bind the quote revision. Native CPQ edits cannot remove required switching/licensing and still issue a validated quote. Test technical versus price-only edits and expiry during approval. CRM timeout after remote success becomes an uncertain reconciliation state, never a blind duplicate create. Quote approval is not deal-won or an order.

## 5. Deliver in gated slices

P0 establishes authority, vendor evidence, owners and a funded scope. P1 proves Marketplace-to-quote-to-HubSpot. P2 adds independent thin tools. P3 extends separately approved specialist/lifecycle/reporting scope. Every service meets security, contract, support and recovery requirements before first real use; later hardening is not permission to expose data early. Synthetic development and real-user/data approval are different checklists.

Human battle cards/resources, non-Wi-Fi planning, broader technical rules and full lifecycle/report breadth are proposed bounded exclusions from the thin pilot. Product/Cleber must accept that scope or fund expansion. Unsupported technical families cannot be issued as validated configurations.

## 6. Inputs needed from Cleber and accountable owners

Identify accountable people for Product/Commercial, CRM, SSO, Security/privacy, Platform and each service. Confirm pilot users/data/country/currency/catalog, permitted scope exclusions, field/quote masters, commercial expected cases, retention/region/revocation bounds and CRM degraded-mode policy. Supply incumbent contracts, vendor entitlements/constraints, platform/support capacity and budget inputs. [OD-01–OD-10](decisions/open-decisions.md) specify evidence and blocked work; no missing answer is treated as consent.

The old 133-person-day seed and 144–200-person-week envelope were not a reconciled estimate. Expanded acceptance must be re-sized into small tasks with procurement lead times and operating costs before a calendar is promised. Review the [proposal](proposal.md), [finding dispositions](reviews/author-revision-1.md) and [backlog](backlog.md). Historical revision-2 Word/PowerPoint files are explicitly superseded for current decisions; regenerate presentation artifacts after canonical review reconciliation, before requesting implementation approval.
