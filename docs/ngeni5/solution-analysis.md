# Solution analysis and EA research brief

**Preliminary comparison, not a product selection.** EA is requested to deepen this analysis with current primary sources, contract/edition evidence, disqualifiers and a reasoned shortlist. No paid trial, purchase, vendor outreach, account modification or application implementation is authorized by this research request.

## Required comparison method

Apply hard gates before weighted scoring: authorized standalone access, customer-solution isolation, supported data export, canonical product/BOM handoff, acceptable licensing/API rights and no duplicate quote authority. A failed gate cannot be offset by a low price.

For candidates that pass, proposed weights are functional fit 25%, integration/contract fit 20%, security/isolation 20%, operational fit 15%, three-year cost 10%, portability 10%. EA should challenge the weights. Mark unknowns unknown; do not invent numeric scores or prices. Compare purchased SaaS, maintained open-source products, and custom development separately; a canvas or LLM library is not a turnkey solution.

## Candidate questions by domain

| Domain | Candidate paths | What is known | Evidence still required | Provisional direction |
| --- | --- | --- | --- | --- |
| Marketplace | Thin custom service; supplier-hosted catalogs; dedicated B2B commerce/catalog product to be researched | Existing draft has no validated turnkey candidate | Partner price segmentation, channel offers, technical comparison, product mapping, export/API rights, catalog stewardship | Keep thin custom as baseline, require EA to name and test credible paid/OSS alternatives |
| Floor Plan | Konva-based custom placement; Hamina; alternative specialist planners to be researched | Konva supplies canvas primitives, not RF calculation; Hamina supplies specialist planning workflows | Supported file types, RF assumptions/validation, BOM export, SSO, embedding/API contract, resale rights, device coverage, multisite behavior | Compare specialist integration with custom placement-only; never equate the two scopes |
| Discovery | NetBox with imports; runZero; other authorized inventory/discovery platforms | NetBox is a source of truth, not a scanner alone | Agent/collector model, segmented networks, supported devices, active/passive impact, credential custody, export, tenancy and license | Separate inventory stewardship from discovery and from proposal disposition |
| AI Builder | Owned orchestration with Bedrock; vLLM and pgvector; other compliant managed providers | Serving and retrieval are building blocks, not complete solution governance | Model quality, data retention/region, per-tenant isolation, tool authorization, cost limits, provider exit, model-weight terms | Run common offline evaluation before recommendation |
| Multi-Site | Custom profiles/overrides service; planning-vendor extension; CPQ-based configuration | Custom domain fit is assumed, no complete vendor fit proved | Profile inheritance, site exceptions, revision diff, deterministic expansion, bidirectional package mapping and exports | Require same 60-site fixture for every candidate |
| Quote and pricing | HubSpot CPQ; independent custom service; ERPNext; specialist HubSpot-compatible CPQ to research | HubSpot is incumbent CRM; quoting capabilities exist but actual entitlement/fit is unknown | Technical dependency rules, NRC/MRC, partner access, quote revision/approval, API automation, pricebook authority, cost and tax separation | Evaluate HubSpot first for integration value, not automatic selection |
| Identity | Existing ngenious SSO capability; underlying IdP alternatives only through SSO owner | EA identifies SSO as shared identity capability | Owner, supported flows/claims, external IdP federation, MFA, lifecycle, workload credentials, logout and recovery | Partner-Portal consumes approved contract; no parallel IdP decision |
| Hosting/integration | Existing approved cloud; managed containers/queue/PostgreSQL; vendor-managed SaaS | No cloud, capacity or residence selected | Solution isolation, network boundary, data egress, restore, deployment workflow, support staffing, cost at three volumes | Prefer operational simplicity after boundaries and vendor fit |

## Comparable proof cases

- Two partners with different offer/price entitlements; direct lookup/export cannot bypass those grants.
- One assessment starts outside the portal and without a deal, then links to an authorized HubSpot deal.
- Sixty sites, reusable profile, one override and a profile revision; re-export preserves all quantities/provenance.
- Unsupported vendor product maps to a visible resolution queue, never an invented SKU or zero price.
- Technical checks reject an incompatible license and a 500 W demand on a 370 W PoE budget.
- One-time and monthly recurring amounts remain distinct across calculation, approval, proposal and CRM summary.
- Retry after an uncertain remote commit creates no duplicate quote/CRM record; reordered notifications reconcile.
- Disable the portal or AI service independently; supported native/manual work continues with explicit dependency limits.
- Revoke a user or offer; cached exports, retrieval and service access follow the documented revocation policy.
- Export/restore a complete solution with mapped IDs and versions, then demonstrate the vendor exit path.

## Cost model and recommendation deliverable

For each shortlisted option, record edition, license restrictions, external partner seats, API/export add-ons, implementation effort, migration, stewardship, infrastructure/model usage, support, HA/DR and exit cost. Use low/expected/high volume assumptions and sensitivity to named users, sites, devices, quotes and tokens. Distinguish verified list price, negotiated quote, unknown and engineering estimate. Avoid a single blended score that hides a failed isolation or licensing gate.

EA should return: preferred option, viable alternative, rejection reasons, evidence date/URL, unanswered procurement questions, scope of proof, operating owner, cost drivers and draft ADR consequences for each domain. Vendor evidence does not approve implementation.

## Existing primary-source starting points

- HubSpot API: https://developers.hubspot.com/docs/reference/api/overview
- HubSpot CPQ: https://knowledge.hubspot.com/cpq/getting-started-with-hubspot-cpq
- HubSpot products/catalog: https://knowledge.hubspot.com/products/create-and-manage-products and https://legal.hubspot.com/hubspot-product-and-services-catalog
- ERPNext: https://docs.frappe.io/erpnext/quotation and https://docs.frappe.io/erpnext/pricing-rule
- Hamina: https://docs.hamina.com/hamina
- Konva: https://konvajs.org/
- NetBox: https://netboxlabs.com/docs/netbox/
- runZero: https://www.runzero.com/platform/
- Bedrock: https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html
- vLLM and pgvector: https://docs.vllm.ai/en/latest/ and https://github.com/pgvector/pgvector

These are research starting points already used in draft 2, not proof of commercial API or tenant fit. EA must add deeper current evidence.
