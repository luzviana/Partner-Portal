# CTO decision brief — HubSpot-first revision

The [P1–P3 integration comparison](integration-architecture-p1-p3.md) is the current technical companion: reuse HubSpot, own a typed integration layer, retain one product/price authority and isolate agent execution. Prove native quotes against private access and no-payment requirements before selecting them. Revision-4 slides do not include this deeper analysis.

The latest reviewed feature list changes the product shape and delivery order. The [revision-4 deck](cto-presentation-rev4.md) presents this current narrative; exported revision-2 and revision-3 decks predate it and are historical. Implementation remains gated by EA review of this revision and explicit user/affected-owner/Security approvals.

## 1. HubSpot integration is the first investment

Home shows HubSpot-sourced partner information, sales, leads, promotions and aggregated opportunities, including customers. Opportunities contains prices and proposals. Resources is a findable structure of HubSpot files, including battle cards. First define the account/object model, partner/customer access, metrics, content taxonomy and reliable synchronization. HubSpot remains the source, while the portal renders a scoped experience.

## 2. Marketplace produces proposals, not direct sales

List products we sell, let a partner select quantities and generate a proposal valid for 30 days. The proposal, price and structured BOM must sit in HubSpot under the opportunity. There is no checkout, payment, fulfilment or auto-order. Prefer a thin custom experience integrated with existing HubSpot capabilities, subject to account-fit proof. Medusa is a conditional catalog foundation; broader commerce/CPQ tools enter the shortlist only if a required gap warrants them.

## 3. AI Sales Support is mandatory and appears everywhere

Rename AI Solution Builder to AI Sales Support. Build an agent capability with authorized page/opportunity context, CRM/catalog/resource retrieval and human-reviewed draft assistance. It appears on every active page and has no menu item. It cannot approve prices, send proposals autonomously or bypass application grants. Priority 3 acceptance is required for the initial priorities 1–3 release.

## 4. Site Designer and Discovery wait

Site Designer replaces Floor Plan Designer and absorbs multisite profiles/overrides. Discovery aims to find all observable items on an authorized network, including endpoints/IoT, with transparent coverage limits. Both are Priority 4 and must not be initialized now. Separate AI and multisite navigation/service requirements from the earlier plan are superseded.

## Decisions still required

Confirm product/price source, HubSpot account/quote entitlement and object mapping, partner grants, Home metrics/promotions source, Resources taxonomy/privacy, and proposal approval/30-day clock policy. Select a representation that preserves price/BOM/revisions in HubSpot. Name operating and data owners, region/lifecycle bounds and budget inputs. The 30-day requirement and new priorities are confirmed; these implementation details are not.

First deliverable: HubSpot integration specification and permission/field map. Next: a scoped Marketplace fit decision and proposal/BOM contract. Then: the mandatory agent tool/context specification. All actual configuration/build work waits for approval. See [priority plan](priority-plan.md), [solution comparison](solution-analysis.md), [backlog](backlog.md) and [owner decisions](decisions/open-decisions.md).
