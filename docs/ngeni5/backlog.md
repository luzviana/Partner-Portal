# Partner Portal prioritized planning backlog

**Author revision 2. All implementation remains blocked pending revised-scope EA review, explicit user approval and applicable owner/Security gates.** No issue tracker records have been created or changed. User priorities are confirmed; no runtime proof or named owner acceptance is implied.

[Priority plan](priority-plan.md): 1 HubSpot integration/Home/Opportunities/Resources; 2 simplified Marketplace and HubSpot proposals valid for 30 days; 3 mandatory AI Sales Support across every page; 4 Site Designer (including multisite) and Discovery deferred, not initialized. No deferred item is a prerequisite to priorities 1–3. R43 is superseded by R51/R52, not completed. R44–R50 remain later/parked work; initial security/operations gates remain with every first use.

R01–R50 preserve historical traceability; titles/acceptance/dependencies now reflect reviewed scope. R51–R60 add Home, Resources, 30-day validity and agent acceptance. IDs are not execution order: dependencies deliberately reference new prerequisite IDs. All changes are planning records only.

R01–R50 retain historical 2–3-day timeboxes (133 days in the old scope). They are not estimates for the revised acceptance. R51–R60 are unestimated. Re-size focused tasks after account/policy evidence; do not invent a new program total. Definition of done includes exact acceptance, gates, named owners, first-use evidence and rollback, not elapsed time.

## R01 — [Partner-Portal] Agree revised portal scope and priorities

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Product

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Record Home/Opportunities/Marketplace/Resources navigation and always-available AI Sales Support. Customers sit in Home; prices/proposals in Opportunities; battle cards in Resources. Confirm HubSpot first, proposal-only Marketplace second, mandatory agent third. Site Designer includes multisite; Discovery covers observable network items. Both Priority 4, not initialized. Name scope/data/service owners and current pilot data/classification.

Depends on: None

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R02 — [Partner-Portal] Inventory HubSpot integration capabilities

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: CRM admin

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Record actual account count, subscription, app model, API version, scopes and relevant objects. Identify an approved test environment and gaps without changing production data.

Depends on: R01

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R03 — [Partner-Portal] Map HubSpot fields, grants and source ownership

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: CRM admin

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Map partner, customer, opportunity, leads, sales, promotions, product/price and resources to actual account objects/properties/associations with one field writer. Define partner/customer/action grants, aggregate visibility, metrics/currency/time filters, retention/revocation and CRM uncertainty limits. No invented Promotions/Leads object or assumed custom-object entitlement. Unknown business definitions remain owner gates.

Depends on: R02

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R04 — [Partner-Portal] Select simplified Marketplace and proposal route

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Commercial

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Compare thin custom UI plus HubSpot native quotes against supported HubSpot proposal/BOM representation; consider Medusa only for measured catalog gaps. Verify catalog/price source, actual account rights, protected prices, structured BOM/version history, no payments and 30-day proposal fit. Broader commerce/CPQ parked unless a specific gap justifies escalation. Record recommendation/evidence, no selection from unknown hard gates.

Depends on: R54

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R05 — [Partner-Portal] Define Marketplace to HubSpot proposal and BOM contract

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Technical lead

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Specify canonical products, quantities/units, technical digest, exact price/currency/term/tax, version, approval, issued/expiry dates and artifact. Define scoped HubSpot associations, complete structured BOM persistence/readback and retry/reconciliation. Compare provider module/adapter before a separate exchange runtime. Require current Marketplace consumer compatibility; deferred Site Designer/Discovery are not prerequisites.

Depends on: R03, R04, R56

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R06 — [Partner-Portal] Approve identity and service access contracts

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Security

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Obtain SSO/application owner acceptance of direct login and local grants, application audience/issuer/subject/organization/time checks, vendor federation and revocation/logout bounds. Define authenticated-without-membership, wrong-audience, revoked-grant and three-axis customer/solution tests, including support/restore. Complete owner-accepted ICR before registration; portal tokens confer no blanket vendor authority.

Depends on: R01, R03

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R07 — [Partner-Portal] Prove current Marketplace candidate fit

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Solutions lead

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Apply rights/SSO/isolation/export/operator gates only to current selected Marketplace/proposal capability and common 30-day persistence cases. Record all unknowns and blocked routes. Do not initialize planning/discovery trials or require their selection to complete priorities 1–3. Split uncovered evidence into focused follow-on tasks.

Depends on: R04, R05, R06

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R08 — [Partner-Portal] Accept HubSpot-first integration design baseline

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Delivery lead

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Review account/field/grant, Home metrics and Resources contracts with named CRM/Product/SSO/Security owners. Select SYN versus REAL proof plan and operating ownership; record unresolved inputs and affected scope. Size Priority 1 work separately; do not wait for deferred planning/discovery proof. This design gate is not runtime acceptance or implementation approval.

Depends on: R03, R06, R51, R53

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R09 — [Partner-Portal] Establish approved portal integration deployment boundary

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Platform

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Only after approval, establish the minimum portal and server-side adapter deployment with scoped credentials, release/rollback, health and operating evidence. Do not scaffold five services or Priority 4 components. Record which capabilities remain modules and any separate runtime justified by isolation/ownership.

Depends on: R08

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R10 — [Partner-Portal] Build current navigation and HubSpot context shell

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Provide Home, Opportunities, Marketplace and Resources navigation from application-local grants. No AI Sales Support menu, Customers, Prices/Quotes, Battle Cards or Multi-Site entries. Reserve a shared support integration point for mandatory Priority 3 without claiming the agent exists. No Site Designer/Discovery initialization.

Depends on: R06, R09

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R11 — [Partner-Portal] Prove customer and solution authorization

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Prove local actor/action/resource grants in two pilot services using different partners, same partner/different customers or solutions, and same customer/different grants. Deny forged scope/CRM mapping, wrong audience and authenticated users without membership. Exercise revoked cached grants, direct URLs/files/jobs and unauthorized support. Record approved revocation bounds and restore-case evidence for first exposure.

Depends on: R06, R09

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R12 — [Partner-Portal] Publish a canonical catalog API slice

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Publish 20 versioned offers with product/vendor IDs, eligibility and price references. Both list and ID lookup enforce grants. Revoke an offer and invalidate a sample consumer.

Depends on: R04, R07, R11

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R13 — [Partner-Portal] Implement authoritative price evaluation

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Pass the 10 approved NRC/MRC cases with decimal arithmetic, term, currency, version and expiry. If a vendor is master, use its supported result through the facade rather than a second calculator.

Depends on: R04, R12

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R14 — [Partner-Portal] Deliver proposal-only product selection

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: List only products we sell with authorized prices and quantities. Selection transfers canonical BOM to Opportunities proposal workflow. No cart checkout, payment, fulfilment, direct-sale order or auto-deal-won. Maintain source/product version and handle unavailable price authority explicitly.

Depends on: R12, R13

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R15 — [Partner-Portal] Persist scoped proposal input revisions

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Selected proposal provider/module records exact input BOM revision/digest and deduplicated receipt. Prove contracts, authorization, lifecycle and recovery for Marketplace input. No separate exchange runtime or deferred-tool adapters without evidence/approval.

Depends on: R05, R07, R09, R11

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R16 — [Partner-Portal] Create the HubSpot connector read projection

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Using the approved test environment, import a company/contact/deal association with account-scoped IDs. Service consumers see only granted CRM records and a freshness timestamp.

Depends on: R02, R03, R09, R11

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R17 — [Partner-Portal] Recover HubSpot inbound changes

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Verify notification authenticity, deduplicate and reread source state; test missed/reordered events, grant/token revocation, rate limits and deletion. Projection freshness is visible and stale authorization fails closed; deletion does not trigger recreate. Follow quote-and-crm-controls.md state and lifecycle rules.

Depends on: R16

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R18 — [Partner-Portal] Persist full proposals, prices and BOMs in HubSpot

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Use durable command ledger and account/opportunity-scoped associations to persist full versioned price and structured BOM, proposal artifact and validity in HubSpot. Verify all required state by readback, not only a link/summary. Timeout after success or partial association enters Uncertain/NeedsOperator, never blind duplicate create. No customer send, payment or deal-won automation.

Depends on: R03, R16, R20

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R19 — [Partner-Portal] Validate one technical quote fixture set

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Specify canonical technical configuration digest and rule-set version. Test ports, 500 W versus 370 W, required license and valid 20-AP fixtures; classify price-only versus technical changes with Commercial/technical owners. Unsupported rule families are blocked or expressly excluded per source coverage. Persist exact digest, findings and validity; executed evidence is a future gate.

Depends on: R04, R07, R15

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R20 — [Partner-Portal] Create immutable 30-day proposal evidence

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Bind BOM/configuration digest, rule version and exact commercial evidence to a proposal revision. Prepare 30-day validity under R56 policy, preserve history and govern personal-data retention. Supplier validity shorter than 30 days requires accepted honoring policy before issuance. Native technical changes invalidate proof; do not silently mutate an issued revision.

Depends on: R13, R15, R19, R56

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R21 — [Partner-Portal] Apply proposal approval and renewal controls

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Enforce exact revision technical/commercial approval and native-edit bypass prevention. Check grant/evidence validity before issue. Require verified HubSpot persistence; customer validity is 30 days under R56. Expired proposal cannot act as current offer; renewal creates a new priced/approved revision. Buyer acceptance/order/payment are outside automatic workflow.

Depends on: R20

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R22 — [Partner-Portal] Deliver durable service events

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Durable outbox and deduplicating consumers survive restart. Before first consumer, publish provider-owned event schemas, supported versions, ordering/idempotency/retry limits, solution-bound replay and dead-letter lifecycle; demonstrate compatibility/rollback and operator handling. Audit uses redacted operational envelope, not unrestricted domain payload.

Depends on: R09, R15, R20

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R23 — [Partner-Portal] Render and quarantine proposal artifacts

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Render only exact approved configuration/commercial digests, hide internal cost and validate totals. Quarantine/bound input, files, worker resources and egress before use. Recheck expiry/grants/technical evidence at issue, including native CPQ edits while rendering; revoke downloads within policy bounds and expire exports. Repeated jobs cannot issue conflicting revisions.

Depends on: R21, R22

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R24 — [Partner-Portal] Reconcile Marketplace proposal to Opportunities

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Quality

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Trace authorized products/quantities through reviewed proposal, complete HubSpot price/BOM persistence and Opportunities view. Test native technical edits, revoked grant, delayed CRM visibility and partial write. Pending does not mean issued/saved. Include R57 expiry and no-payment evidence.

Depends on: R14, R17, R18, R23, R57

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R25 — [Partner-Portal] Test standalone and cross-tenant failures

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Quality

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Portal outage preserves native access; shared-data/vendor outage reports accurate degradation. Exercise all three authority axes across API/files/jobs/AI/export surfaces in pilot scope, with forged context, revoked grants and unauthorized support. Include deletion/replay/restore denial cases, not just different partner IDs.

Depends on: R24

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R26 — [Partner-Portal] Accept Marketplace proposal increment

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Platform

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Require R54 HubSpot integration acceptance, complete price/BOM persistence, 30-day controls, no checkout/payment, exact approvals and first-use security/restore/operator evidence. This accepts Priority 2 only; initial priorities 1–3 release remains incomplete until mandatory AI R60.

Depends on: R25, R54

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 1 integration acceptance R54 before delivery; source/rights/30-day HubSpot proposal fit gates before use

## R27 — [Partner-Portal] Deferred: define Site Designer scope

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: When explicitly reactivated, define one Site Designer incorporating floor/site geometry and multisite profiles/overrides. Evaluate specialist/custom options and first-use controls then; no initialization now.

Depends on: R60

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R28 — [Partner-Portal] Deferred: map Site Designer BOM output

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: After reactivation and provider selection, map Site Designer products/sites/profiles/geometry and fidelity into existing Opportunities proposal contract. Future accuracy/rights evidence required; no new adapter now.

Depends on: R27, R15

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R29 — [Partner-Portal] Deferred: define network-wide Discovery coverage

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: When reactivated, scope authorized segments, device classes, protocols/credentials and safety limits to find all observable network items including endpoints, servers, printers, IoT and network equipment. Measure known/unknown/unreachable coverage; import alone is insufficient. No active scan or initialization now.

Depends on: R60

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R30 — [Partner-Portal] Deferred: review discovery observations

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: After authorized discovery, review provenance and KEEP/REUSE/UPGRADE/REPLACE/ADD. Unknown/unreachable items remain explicit. Observations do not replace iTop inventory authority; import can supplement, not fulfill network discovery.

Depends on: R29

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R31 — [Partner-Portal] Deferred: add multisite context inside Site Designer

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: After explicit reactivation, add sites/profile workspace inside Site Designer, not a separate menu/product. Bind each workspace to solution/environment and validate staged site inputs.

Depends on: R27

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R32 — [Partner-Portal] Deferred: version Site Designer profiles and overrides

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Apply a profile revision to 40 sites and one local override. Preview later changes and preserve source revisions. A repeated application creates no duplicate quantities.

Depends on: R31

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R33 — [Partner-Portal] Deferred: export Site Designer multisite BOM

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: After reactivation, reproducible site/profile expansion exports one versioned BOM into Opportunities, preserving historical quotes. No independent Multi-Site service initialization.

Depends on: R28, R32

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R34 — [Partner-Portal] Prepare authorized AI Sales Support knowledge

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Catalog steward

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Use governed product evidence and HubSpot Resources/battle cards with citations, rights/version/expiry and scoped CRM context. Human Resources remains a first-class Priority 1 feature. Revoke cached chunks/tool context within approved bounds; stale protected authority fails closed.

Depends on: R12, R26, R55

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 2 acceptance R26 before delivery; agent is mandatory for initial release, with no menu item

## R35 — [Partner-Portal] Build AI Sales Support agent capability

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Implement approved agent orchestration with scoped CRM/catalog/Resources read tools, grounded answers and separate context per authorized customer/opportunity. Provider/model terms and first-use controls precede exposure. No standalone AI menu/application or broad HubSpot API credential. Support cancellation, budgets and safe unavailable state.

Depends on: R09, R11, R34, R58

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 2 acceptance R26 before delivery; agent is mandatory for initial release, with no menu item

## R36 — [Partner-Portal] Propose human-reviewed sales drafts

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Agent can suggest products, BOM changes and proposal drafts through typed reauthorized contracts. Show source evidence and exact proposed changes for human review. No autonomous pricing approval, customer send, order, deployment, scanning or direct database write. Any later CRM write requires separately approved preview/confirmation and ledger.

Depends on: R15, R35

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 2 acceptance R26 before delivery; agent is mandatory for initial release, with no menu item

## R37 — [Partner-Portal] Evaluate AI Sales Support behavior

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Quality

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Test grounded CRM/product/resource cases, unknown-price refusal, malicious resource content, revoked grants and cross-customer navigation. Measure quality/cost/latency and confirm manual Home/Opportunities/Marketplace/Resources workflows during agent outage. No unexecuted result claimed.

Depends on: R36

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 2 acceptance R26 before delivery; agent is mandatory for initial release, with no menu item

## R38 — [Partner-Portal] Verify active portal context and handoff contracts

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Verify context/grants across Home, Opportunities, Marketplace, Resources and persistent AI Sales Support. Service-owned contracts/versions remain compatible. Site Designer/Discovery integration is excluded until reactivation.

Depends on: R26, R59

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 2 acceptance R26 before delivery; agent is mandatory for initial release, with no menu item

## R39 — [Partner-Portal] Accept active portal workflows with mandatory AI

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Quality

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Verify priority 1–3 journeys and persistent agent context without separate AI navigation. Confirm full 30-day proposal evidence in HubSpot and human review. Do not require or claim five independent applications; deferred Site Designer/Discovery remain uninitialized.

Depends on: R37, R38

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Priority 2 acceptance R26 before delivery; agent is mandatory for initial release, with no menu item

## R40 — [Partner-Portal] Expand specialist RF accuracy and fidelity proof

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Solutions lead

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Expand RF accuracy/fidelity proof only for a candidate with selection rights/SSO/isolation/export gates passed before its first use. Test approved fixture and document remaining work; this later item cannot authorize earlier R27/R28 use. Non-Wi-Fi functions need their own scope/evidence before claims.

Depends on: R28

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R41 — [Partner-Portal] Authorize a discovery collector scope

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Security

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Before any active scan, reconfirm selected scanner rights and approve exact customer/lab targets, protocols, local secrets, identity, egress/kill switch, operator and SYN/REAL checklist. R07/R08 selection evidence precedes configuration; late approval does not legalize prior scans.

Depends on: R29

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R42 — [Partner-Portal] Demonstrate one discovery collector feed

Phase: Priority 4 | Priority: Deferred | Status: deferred_not_initialized | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Only after R41, ingest one authorized lab/vendor collector batch with source mapping, bounded retry and observation expiry; test disconnected/duplicate recovery and scoped credential handling. Record known/unknown device coverage and follow-on scope; no universal discovery claim.

Depends on: R41

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure
- Explicit Priority 4 reactivation required; do not initialize services, UI routes, collectors, accounts, trials or infrastructure now

## R43 — [Partner-Portal] Superseded: customer information now in Home

Phase: Later | Priority: Superseded | Status: superseded | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Do not execute this former late Customer 360 item. Its current CRM/customer composition scope moves to R51/R52 in Priority 1. Additional lifecycle feeds remain separately scoped future work.

Depends on: None

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

Superseded by: R51, R52

## R44 — [Partner-Portal] Build a reconciled reporting projection

Phase: Later | Priority: Later | Status: parked | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Create only approved minimized solution-scoped reporting projection. Reconcile version counts/values without revision double counting. Apply three-axis grants, selected retention/region, source tombstones, cache/export expiry and restore replay; no central detailed customer data lake. CON and REAL/SYN proof precede first use.

Depends on: R60

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R45 — [Partner-Portal] Prove report formats and BI isolation

Phase: Later | Priority: Later | Status: parked | Owner: Engineering

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Prove one approved report in PDF/Excel/CSV/PPT with filters/as-of and genuine format fidelity. Test all three authority axes including cached/scheduled/export/service-principal paths, download revocation and expiry; document unavoidable downloaded-copy limits. Remaining strategy reports require separate scope/funding.

Depends on: R44

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R46 — [Partner-Portal] Test compatibility and vendor exit

Phase: Later | Priority: Later | Status: parked | Owner: Quality

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Expand prior first-use compatibility tests into vendor exit/recovery: supported previous versions, solution state/canonical references, lost fields, deletion/backup expiry, legal holds and revoked grants after export/restore. Record migration owner and gaps; this is not the first consumer contract proof.

Depends on: R60

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R47 — [Partner-Portal] Exercise enterprise security and recovery

Phase: Later | Priority: Later | Status: parked | Owner: Security

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Regress earlier service launch controls across all approved scope: three-axis isolation, support elevation denial, credentials, bounded revocation, lifecycle purge, immutable redaction and backup/restore reconciliation. Record independent Security decisions for material exceptions; none are preapproved. Do not defer initial controls to this item.

Depends on: R46

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R48 — [Partner-Portal] Accept integrated service operations

Phase: Later | Priority: Later | Status: parked | Owner: Delivery lead

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Reconcile actual supported scope, staffing/TCO, vendor/manual-handoff costs, named operators/on-call, journey SLIs and recovery evidence with funded baseline. Each vendor outage counts in journey measurement. Accept precise release scope or keep unresolved capabilities blocked; no assumption-based schedule or SLO claim.

Depends on: R47

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R49 — [Partner-Portal] Parked: order and billing business case

Phase: Later | Priority: Later | Status: parked | Owner: Commercial

Timebox: 3 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Direct sales, checkout, payment and order/billing are outside the current Marketplace. This is not a prerequisite or scheduled delivery item. Reopen only on a separate explicit scope change.

Depends on: R48

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R50 — [Partner-Portal] Parked: reassess internal decomposition

Phase: Later | Priority: Later | Status: parked | Owner: Technical lead

Timebox: 2 person-days (historical)

Estimate status: historical_timebox_reestimate_required

Acceptance: Reassess modules/services only with measured ownership/load/isolation evidence. Earlier mandatory five-service topology is superseded. No automatic new repositories, gateway or deferred-service scaffolds.

Depends on: R48

Source: Latest reviewed user scope in priority-plan.md; original PDF and EA controls where applicable

Gates:

- EA review of revised scope, explicit user implementation approval and applicable affected-owner/Security acceptance; prior reports do not approve this revision
- CON and SYN/REAL first-use evidence in release-and-operations.md before applicable exposure

## R51 — [Partner-Portal] Define HubSpot Home aggregation

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Product

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Document partner information, sales, leads, promotions, customers and opportunity mapping from actual HubSpot source. Define sales/count/date/currency/dedupe metrics, partner/customer grants, promotion validity and source timestamps. Unknown sources/definitions block claims; no mock data treated as actual results.

Depends on: R02, R03

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R52 — [Partner-Portal] Prove scoped Home and Opportunities reads

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Render authorized HubSpot Home aggregate and opportunity drilldown with source/freshness and customer context. Test other partner, same partner/different customer, different grants, missing data versus outage, revoked access, duplicate revisions and currency treatment.

Depends on: R10, R16, R51

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R53 — [Partner-Portal] Define HubSpot Resources contract

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Content owner

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Agree HubSpot file/folder taxonomy, discoverable metadata, battle-card location, owner/version/validity/audience and per-partner read/download policy. Evaluate private access, search/filter semantics and cache invalidation. Full-text search and any indexing entitlement remain explicit decisions.

Depends on: R02, R03

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R54 — [Partner-Portal] Accept HubSpot integration increment

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Product

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Accept approved Home/Opportunities/Resources proof with source mappings, aggregate accuracy, grants, private downloads, revocation and outage/recovery. Named CRM/content/operator owners confirm evidence and missing inputs. This is the delivery predecessor to Marketplace, not an implementation approval.

Depends on: R17, R52, R55

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R55 — [Partner-Portal] Provide findable HubSpot Resources

Phase: Priority 1 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Implement authorized file metadata browse/search/filter and controlled open/download from HubSpot, including battle cards. Test guessed file ID, revoked grant, expired/withdrawn resource and caches; no public sharing used to bypass rights. Confirm human findability separately from AI retrieval.

Depends on: R10, R16, R53

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R56 — [Partner-Portal] Specify 30-day proposal clock and persistence

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Commercial

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Confirm issuance anchor, calendar/timezone/end-of-day rule and exact 30-day validity, consistent HubSpot representation, renewal/version behavior and commercial price-honoring policy. Choose native quotes or proven supported proposal/BOM representation. No automatic payment/checkout/send; unresolved policy or shorter supplier commitment blocks issue.

Depends on: R04

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R57 — [Partner-Portal] Prove proposal expiry and complete HubSpot persistence

Phase: Priority 2 | Priority: High | Status: proposed_pending_approval | Owner: Quality

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Verify canonical BOM lines, quantities, prices/totals/currency, artifact/version and 30-day validity in HubSpot and portal. Test day 30 boundary, timezone, draft ageing, expired old revision and renewal. Assert no payment/checkout/order/deal-won behavior, native-edit bypass or duplicate create after timeout.

Depends on: R18, R23, R56

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R58 — [Partner-Portal] Define AI Sales Support tools and context

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: AI owner

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Specify mandatory all-page agent, current context visibility and permission-scoped CRM/catalog/Resources read tools. Draft-only commercial suggestions need human review. Select model/data terms and tool allowlist; prohibit broad API access and autonomous sends/approvals. Clear/reauthorize context on customer/page changes.

Depends on: R26, R53

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R59 — [Partner-Portal] Integrate AI support across active pages

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Engineering

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Expose a persistent agent control on Home, Opportunities, Marketplace and Resources, without menu item. Supply minimal authorized page/opportunity context, source links and clear context switching. Test revoked access, previous-customer leakage, unsupported actions and agent outage without disabling page functions.

Depends on: R10, R35, R55

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure

## R60 — [Partner-Portal] Accept mandatory agent and initial release

Phase: Priority 3 | Priority: High | Status: proposed_pending_approval | Owner: Product

Timebox: Not estimated

Estimate status: not_estimated

Acceptance: Accept priorities 1–3 only when the agent works on every active page with grounded authorized assistance, human-reviewed draft actions, source revocation and outage fallback. Record named operator/model/retention/cost evidence; agent cannot be silently deferred. Site Designer and Discovery remain deferred and uninitialized.

Depends on: R37, R39, R59

Source: Latest reviewed user scope in priority-plan.md

Gates:

- Exact-revision EA review and explicit user implementation approval plus applicable owner/Security acceptance
- CON and SYN/REAL first-use checks before applicable exposure
