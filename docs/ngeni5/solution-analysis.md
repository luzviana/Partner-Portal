# Solution choices for the simplified portal

Author revision 2. Scope changed to a HubSpot-first portal and proposal-only Marketplace. This narrows the earlier [EA research](solution-research-evidence.md), which remains dated evidence rather than a selection. No account inspection, purchase or vendor trial occurred.

## Current recommendation and alternatives

| Option | Fit for the revised need | Tradeoff / evidence needed | Disposition |
| --- | --- | --- | --- |
| Thin custom catalog/selection UI + HubSpot proposal workflow | Directly serves our products, quantities, BOM and opportunity without checkout | Own the small integration, grants, rendering and reconciliation. Confirm catalog source and actual quote entitlement/30-day behavior | Leading design recommendation, not implementation selection |
| Thin UI + supported HubSpot deal-associated proposal/BOM representation | Keeps proposal, price and BOM in HubSpot if native quoting cannot fit | Must prove structured BOM, version history, artifacts and 30-day enforcement in supported account features. A total or link alone is insufficient | Conditional fallback, no custom-object entitlement assumed |
| Medusa product/pricing foundation + HubSpot integration | May help if existing catalog tools are inadequate or catalog administration is substantial | Adds software/operations and mappings. Quote/order examples are building blocks, not automatic fit; omit order/payment flow | Conditional challenger after catalog gap evidence |
| CloudBlue channel commerce | Broader supplier/channel/subscription functions than the current requirement | Rights, cost and another platform lifecycle; no present requirement for its wider commerce scope | Park initial evaluation unless a specific required gap justifies it |
| QuoteWerks | Specialist challenger if HubSpot proposal/approval capability demonstrably fails | Adds quoting authority and integration ownership; must still persist full agreed proposal evidence in HubSpot | Escalation option after native fit failure |
| ERPNext or fully custom CPQ | Broad commercial scope or maximal control | More responsibility and potential master overlap than simple proposal generation | Outside initial shortlist absent a documented necessity |

This preference is an architectural inference from the reduced scope, not a measured cheapest option. Assess total cost for equal scope, including integration, licenses, stewardship, operations and exit. No price or purchased capability is known. The user's 30-day validity and HubSpot price/BOM persistence are mandatory comparison cases, not optional scores.

## Current primary-source checks

HubSpot's current Quotes API documents expiry and required quote associations, distinguishes current versus legacy capabilities and ties current quote creation to qualifying Revenue Hub subscriptions. Approvals are primarily UI/workflow managed. Payment configuration can be enabled by account setup, so the selected flow must explicitly prove no checkout/payment behavior. These documented features do not verify the user's subscription or workflow. [HubSpot Quotes API](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/quotes/guide).

HubSpot publishes product APIs that can be evaluated as the catalog source. Existing catalog completeness, commercial field ownership and partner-specific pricing still require inventory. [HubSpot Products API](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/products/guide).

The Files API provides file/folder operations and temporary access for private files. Portal grants, findability, file expiry and prevention of cross-partner download still need an explicit design. [HubSpot Files API](https://developers.hubspot.com/docs/api-reference/latest/files/guide).

Medusa documents a custom quote-management example using commerce primitives. It illustrates extensibility, not an off-the-shelf guarantee of this HubSpot workflow. [Medusa quote-management example](https://docs.medusajs.com/resources/examples/guides/quote-management).

## Priority 1 proof determines Priority 2 selection

R02/R03 establish account/API/object/access constraints. R51/R53 map Home and Resources. R54 proves the integrated read experience under approved first-use gates. R04/R05/R56 then compare native quote versus supported proposal/BOM representation on the actual approved account model. Selection requires:

- Our authorized product list and expected quantities/prices, with partner/customer grants enforced.
- A versioned proposal with complete structured BOM/price stored in HubSpot and visible under the correct opportunity.
- Exactly 30-day customer validity under an agreed clock policy, with expired revisions blocked and renewed through a new version.
- No direct purchase/payment/order or automatic deal-won; no automatic customer send.
- Technical/commercial revision controls, explicit approval and native-edit bypass proof.
- Timeout/partial-write reconciliation, preserved historical BOM/price, private artifacts, revoked access and export/restore.

Unknown rights, account capability, isolation, persistence or expiry behavior blocks the affected route. Manual staff completion is a possible explicitly agreed workflow, not an excuse to claim automation. Provider-specific work and actual evidence follow existing approval gates.

## Other priorities

AI Sales Support is mandatory Priority 3: compare managed inference with owned authorization/tools against self-hosted inference only where policy/utilization justifies operations. The agent is present on every page, not a standalone navigation app. Accept grounded CRM/catalog/resource assistance, human-reviewed drafts, context isolation and safe failure before completing the initial release.

Site Designer (including multisite) and Discovery are Priority 4, not initialized. Preserve specialist research for later without trials, new repositories or active procurement. Future Discovery must target all observable device classes on authorized networks and report unknown/unreachable gaps; import-only assessment is not fulfillment of that requirement. No cloud, model, vendor or production architecture is selected here.
