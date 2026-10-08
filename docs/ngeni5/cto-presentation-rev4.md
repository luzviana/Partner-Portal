# CTO presentation revision 4 — EA review target

Discussion draft, 7 October 2026. Planning baseline: `5bd91cb04951d541df0df57ff55fb742bdf572f6`. No EA approval or implementation authority is implied. Earlier decks remain historical.

[PowerPoint](../../output/ngeni5/NGENI-5_CTO_Review_rev4.pptx) · [PDF](../../output/ngeni5/NGENI-5_CTO_Review_rev4.pdf) · [Review brief](reviews/presentation-rev4-request.md)

## Slide 1

01

Partner Portal

HubSpot integration and sales support

CTO discussion draft 4

7 October 2026

### Speaker notes

Discussion draft based on exact architecture source 5bd91cb04951d541df0df57ff55fb742bdf572f6. Latest user direction supersedes the five-service topology. EA must review this export at its own committed hash. No implementation approval.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/decision-brief.md

## Slide 2

Reviewed priorities

02

Priority

Outcome

1  HubSpot integration

Home, Opportunities and findable Resources

2  Marketplace

Products we sell and 30-day proposals in HubSpot

3  AI Sales Support

Mandatory agent available across all active pages

4  Deferred

Site Designer with multisite, and Discovery

Site Designer and Discovery will not be initialized now.

### Speaker notes

Current navigation Home, Opportunities, Marketplace, Resources. No AI menu. Customers in Home, prices/quotes in Opportunities, battle cards in Resources. Priority order is user-confirmed, implementation authority remains pending.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

## Slide 3

Portal experience and ownership

03

Surface

Source and responsibility

Home

HubSpot partner, sales, leads, promotions and customers

Opportunities

HubSpot opportunities, prices, BOMs and proposals

Marketplace

Authorized products and quantities for a proposal

Resources

Findable HubSpot files, including battle cards

AI Sales Support

Persistent support control with authorized page context

Home aggregates opportunities. Each view enforces partner and customer grants.

### Speaker notes

Home means HubSpot-sourced portal rendering, not assumed dashboard embedding. Objects, sales/lead metric definitions and promotions source require actual account mapping. SSO authenticates, applications authorize. Menu areas are not automatically microservices.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/service-boundaries.md

## Slide 4

Priority 1: HubSpot integration

04

Work to define first

Evidence required

Account and field mapping

Actual objects, subscriptions, APIs, associations and owners

Partner access

Scoped reads, aggregates, files and opportunity permissions

Home and Resources

Metric definitions, freshness, taxonomy and private downloads

Recovery and operations

Reconciliation, revoked access, operator and restore evidence

The integration specification and permission map precede UI implementation.

### Speaker notes

No account features, custom object entitlement or promotions object invented. Lead can map to actual process rather than assumed Leads API. Home distinguishes zero from unavailable; do not double count proposal revisions. Resources metadata search first, full-text undecided. Private signed access is not a substitute for grants.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/contracts.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/authority-and-lifecycle.md

## Slide 5

Marketplace options for this scope

05

Option

Fit / tradeoff

Proposed position

Thin portal + HubSpot

Small catalog and proposal integration to own

Leading option if account fit passes

Medusa + HubSpot

Reusable catalog tools with added software and mapping

Conditional on catalog gaps

CloudBlue / broader commerce

Wider distribution and subscription scope

Park unless a required gap appears

This Marketplace generates proposals. It has no checkout or direct sales.

### Speaker notes

Recommendation is an inference from reduced scope, not measured cheapest route. Catalog/price source remains unknown. Verify licensing/SSO/isolation/export and operators before use. Medusa custom quote example: https://docs.medusajs.com/resources/examples/guides/quote-management . Historical CloudBlue research is in solution-research-evidence.md.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/solution-analysis.md

## Slide 6

Proposal storage and authority options

06

Route

Required proof

Position

Native HubSpot quoting

Full BOM, prices, versions, approval and expiry

First route to evaluate

Supported HubSpot record / artifact

Structured BOM and revision history, beyond a link

Conditional fallback

QuoteWerks / other CPQ

Specific fit failure that justifies another authority

Escalation option only

One price authority. Every accepted route preserves the proposal and BOM in HubSpot.

### Speaker notes

Actual account entitlement and current-versus-legacy behavior unknown. Native quote API documents required associations and expiry; approvals primarily UI/workflows. No custom-object entitlement assumed. Current quote APIs may enable payment based on account setup: verify no checkout/payment. https://developers.hubspot.com/docs/api-reference/latest/crm/objects/quotes/guide . No vendor trial or account change performed.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/solution-analysis.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/quote-and-crm-controls.md

## Slide 7

Thirty-day proposal lifecycle

07

Step

Required behavior

Select and review

Canonical products, quantities, exact price and BOM

Approve and persist

Bind exact revision and verify complete HubSpot storage

Issue with 30-day validity

Same expiry in document, portal and HubSpot

Expire or renew

Old revision stops being current; renewal creates a new version

The 30-day requirement is fixed. Issuance clock and price-honoring policy need agreement.

### Speaker notes

Proposed anchor issuance after approval and verified persistence. Calendar/timezone/end-of-day semantics owner gated. Supplier price validity shorter than 30 days requires an approved honoring policy, never silent shortening. Thirty days is commercial validity, not retention. Test native edit bypass, partial associations, delayed visibility and uncertain create; never duplicate blindly. No autonomous send, order or deal-won.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/quote-and-crm-controls.md

## Slide 8

AI Sales Support options

08

Option

Benefit

Responsibility / tradeoff

Managed inference + owned agent

Avoid operating model-serving capacity

Verify model terms, privacy, region and usage cost

Self-hosted model + owned agent

More deployment and model control

Own capacity, security, model rights and on-call

Both require governed CRM, catalog and Resources tools. No separate AI menu.

### Speaker notes

Mandatory Priority 3 capability. Retrieval and proposed drafts use per-call authorization and citations. Reauthorize/clear context when switching customers, expose current context, test revocation/injection/unknown-price refusal. Agent cannot approve prices, directly write tables, send autonomously, buy or scan. Model/provider not selected. Manual workflows remain usable during agent outage.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/solution-analysis.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

## Slide 9

Delivery and first-use gates

09

Increment

Acceptance

Priority 1: HubSpot

Scoped Home, Opportunities and human Resources journey

Priority 2: Marketplace

Verified price/BOM persistence and 30-day proposal controls

Priority 3: Agent

Support across every active page with safe context and tools

Priority 4: Later decision

Site Designer and Discovery await explicit reactivation

The initial priorities 1–3 release includes the mandatory agent.

### Speaker notes

Backlog R01-R60 is proposed. R43 superseded by R51/R52. R54 accepts HubSpot, R26 Marketplace, R60 mandatory agent/initial release. No P4 dependency blocks P1-3. SYN/REAL, contract, vendor rights, recovery/operator and security evidence precede exposure. No timeline or numerical SLO approved.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/backlog.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/release-and-operations.md

## Slide 10

Deferred capabilities and scope limits

10

Capability

Future scope

Site Designer

Site/floor design with multisite profiles and overrides

Discovery

All observable items on authorized network segments

Discovery coverage

Document unknown, unreachable or unsupported devices

Current boundary

No scaffolding, collectors, accounts or vendor trials now

Import-only assessment does not fulfill the future network discovery objective.

### Speaker notes

Latest user defers both Priority4. No standalone multisite service/menu. Future device coverage includes endpoints, servers, printers, IoT and networking gear. Cannot promise detection of powered-off or isolated devices; require measured scope, credentials and safety/stop controls. Existing iTop inventory authority preserved.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/priority-plan.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/source-evidence.md

## Slide 11

Evidence and cost before selection

11

Decision

Inputs still missing

HubSpot and catalog fit

Account capabilities, product/price source and field owners

Commercial policy

Approval, 30-day clock, tax/currency and price honoring

Data and operations

Grants, lifecycle bounds, named support and recovery owners

Three-year cost

Build/integration, licenses, operations, stewardship and exit

Re-estimate the active scope. Previous staffing and calendar envelopes are superseded.

### Speaker notes

No money estimate or cheapest winner asserted. Rates, volumes, internal/external seats, API/model usage and manual labor require owner inputs. Each candidate must first pass rights/SSO/isolation/persistence/export/lifecycle gates. All human approvals pending as applicable.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/decisions/open-decisions.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/solution-analysis.md

## Slide 12

EA review and CTO decisions

12

EA review of the revised boundaries and presentation

Named owners and confirmed HubSpot integration inputs

Evidence-backed Marketplace and agent choices

Explicit approval of scope before implementation

No implementation, procurement or deployment approval is implied.

### Speaker notes

Review exact exported PPTX/PDF plus canonical source and user overrides. Preserve original PP-EA-01 through PP-EA-12 findings and distinguish prior design review from this new scope. Review source/PDF alignment, data ownership, identity, security, APIs, deployment/operations, solution comparisons and delivery gates. A review report is not user implementation approval.

Sources

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/reviews/status.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/reviews/scope-revision-2.md

https://github.com/luzviana/Partner-Portal/blob/5bd91cb04951d541df0df57ff55fb742bdf572f6/docs/ngeni5/decision-brief.md

## Artifact checks

12 slides; package integrity, layout geometry, font policy and first-party import passed. Every rendered slide inspected individually. PDF exported. Native PowerPoint execution was not tested.

PPTX SHA-256: `ff7a3d28f329041ad52a92a74d950e9be7d7f726a43145131edfd7d9fbb37ccd`

PDF SHA-256: `16aefb6406459adf697077b857113f8807b2ccb5aa08d6488f2db2db0f21d24a`
