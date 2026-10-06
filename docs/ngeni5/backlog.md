# Partner Portal implementation backlog

Author revision 1, 6 October 2026. Proposed items only; no task-system records mutated.

**Implementation blocked pending exact-revision EA re-review, explicit user scope approval and applicable affected-owner/Security gates.** Dependencies alone never authorize work. Documentation may continue; no live configuration, trial, procurement or deployment is authorized. All R01-R50 remain planning records, not executed results.

The retained 2–3-day values are historical focused timeboxes: 133 person-days in the original seed. Expanded acceptance requires re-estimation and smaller follow-on tasks before execution. A task cannot be marked accepted merely because its timebox expired. [Estimate reconciliation](release-and-operations.md) explains the difference from the former program envelope. No staffing or calendar commitment is approved.

P0 R01-R08 produces evidence/decisions; P1 R09-R26 is the Marketplace/quote/CRM pilot; P2 R27-R39 comprises independent thin services; P3 R40-R48 expands separately authorized scope and operations; R49-R50 are later decisions. Vendor unknowns block the affected use or require an explicit approved exclusion. R40-R42 cannot authorize earlier use. SYN/REAL checklists apply before first exposure, not merely phase exit; CON applies before first independent consumer, not only R46.

Definition of done: item acceptance plus its gates, named accountable owner, versioned evidence, failure/negative cases, compatibility and rollback appropriate to approved scope. No runtime proof is claimed in this documentation revision. [Authority/lifecycle](authority-and-lifecycle.md), [quote/CRM controls](quote-and-crm-controls.md), [release/operations](release-and-operations.md) and [open decisions](decisions/open-decisions.md) are incorporated requirements. Historical revision-2 DOCX is not authoritative. Markdown below is generated from backlog.json so every field matches.

## R01 — [Partner-Portal] Agree pilot scope and service autonomy

Phase: P0 | Priority: High | Accountable role: Product | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Record proposed pilot partners/users, customer/solution/environment/workspace mapping, country/currency/catalog and synthetic versus real-data scope; none is assumed accepted. Define three-axis access fixtures and native/portal outcomes. Identify Product, Security, solution and operating owners; OD-01/07 acceptance is required before affected use.

Depends on: None

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R02 — [Partner-Portal] Inventory HubSpot integration capabilities

Phase: P0 | Priority: High | Accountable role: CRM admin | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Record actual account count, subscription, app model, API version, scopes and relevant objects. Identify an approved test environment and gaps without changing production data.

Depends on: R01

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R03 — [Partner-Portal] Agree CRM field owners and tenant mapping

Phase: P0 | Priority: High | Accountable role: CRM admin | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Document one writer per CRM field and account-scoped mappings, application-owned CRM visibility grants, explicit partner/customer/solution collaboration and conflict/deletion/outage policy. Complete record-class lifecycle owners/regions and numeric revocation/cache/export/backup/audit bounds; unknowns block real-data use. Define CRM correlation, retry/uncertainty/operator bounds before R16/R18.

Depends on: R02

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R04 — [Partner-Portal] Compare product pricing and quote authorities

Phase: P0 | Priority: High | Accountable role: Commercial | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Compare Medusa/CloudBlue/thin custom for catalog and HubSpot/QuoteWerks/conditional ERPNext/custom for quotes using solution-analysis.md evidence register and ten owner-supplied expected cases. Record field/quote authority candidates, native edit-bypass feasibility, rights gaps and low/base/high TCO inputs. This is a comparison, not selection: unknown hard gates block OD-02/03 and R08 selection.

Depends on: R02

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R05 — [Partner-Portal] Publish the solution package contract

Phase: P0 | Priority: High | Accountable role: Technical lead | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Review versioned package envelope with partner/customer/solution/environment/service-workspace identity, trusted scope binding, configuration digest/rule version, provenance and lifecycle references. Define schemas, limits, errors, supported versions, idempotency/replay and first-consumer compatibility checklist. Compare module/adapter/service and durable package custodian for OD-09. Unknown policy values or provider ownership block affected implementation; follow-on schema work is sized separately.

Depends on: R01, R03, R04

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R06 — [Partner-Portal] Approve identity and service access contracts

Phase: P0 | Priority: High | Accountable role: Security | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Obtain SSO/application owner acceptance of direct login and local grants, application audience/issuer/subject/organization/time checks, vendor federation and revocation/logout bounds. Define authenticated-without-membership, wrong-audience, revoked-grant and three-axis customer/solution tests, including support/restore. Complete owner-accepted ICR before registration; portal tokens confer no blanket vendor authority.

Depends on: R01, R03

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R07 — [Partner-Portal] Assess five service solution candidates

Phase: P0 | Priority: High | Accountable role: Solutions lead | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: For each candidate record documented/demonstrated/contractually confirmed/unknown/failed evidence for rights, standalone SSO, isolation/restore/support, API/export fidelity, lifecycle/region and operator. Include EA compared alternatives and manual fallback lost fields/labor/outcome. Unknown or failed hard gates prohibit selection/use; scope any exclusion for explicit Product approval. Produce small proof tasks for outstanding evidence; no false completion of a vendor proof in this timebox.

Depends on: R05, R06

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R08 — [Partner-Portal] Approve governed data and delivery baseline

Phase: P0 | Priority: High | Accountable role: Delivery lead | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Record selected or explicitly excluded capabilities only after R04/R07 hard-gate evidence and owner acceptance. Unknowns block affected work, not silently waive it. Obtain entitled offers and expected commercial cases; record OD-01 through OD-09 as applicable, scoped threat model and first-exposure plan/operators. Reconcile seed versus program work breakdown, stewardship, staffing, vendor lead times, operations and TCO. EA/user/affected-owner/Security approvals remain separate from this baseline.

Depends on: R03, R04, R05, R06, R07

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R09 — [Partner-Portal] Establish independent deployment templates

Phase: P1 | Priority: High | Accountable role: Platform | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Create a reusable service template with separate identity, state credentials, health endpoint and release pipeline. Deploy two empty services and update one without redeploying the other.

Depends on: R08

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R10 — [Partner-Portal] Build the portal shell and service registry

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Display navigation projected from service-owned grants and checked workspace context; never administer universal access. One unavailable service does not block other links; direct service login works without portal. Identity self-service gains no launcher.

Depends on: R06, R09

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R11 — [Partner-Portal] Prove customer and solution authorization

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Prove local actor/action/resource grants in two pilot services using different partners, same partner/different customers or solutions, and same customer/different grants. Deny forged scope/CRM mapping, wrong audience and authenticated users without membership. Exercise revoked cached grants, direct URLs/files/jobs and unauthorized support. Record approved revocation bounds and restore-case evidence for first exposure.

Depends on: R06, R09

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R12 — [Partner-Portal] Publish a canonical catalog API slice

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Publish 20 versioned offers with product/vendor IDs, eligibility and price references. Both list and ID lookup enforce grants. Revoke an offer and invalidate a sample consumer.

Depends on: R04, R08, R11

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R13 — [Partner-Portal] Implement authoritative price evaluation

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Pass the 10 approved NRC/MRC cases with decimal arithmetic, term, currency, version and expiry. If a vendor is master, use its supported result through the facade rather than a second calculator.

Depends on: R04, R12

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R14 — [Partner-Portal] Launch a standalone marketplace slice

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: A user opens Marketplace without the portal, browses entitled offers and exports a selection. The portal launches the same service with authorized context. Persist source revision.

Depends on: R12, R13

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R15 — [Partner-Portal] Accept immutable solution packages

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: After OD-09 selection, the named package provider records immutable accepted package/digest and receipt through the selected module/adapter/service contract. Reject scope/schema/mapping errors and deduplicate scoped command IDs. Prove first-consumer versions/limits, authorized evidence links, tombstone/redaction/hold policy, bounded exports, revocation during replay and isolated restore; no indefinite personal-data retention.

Depends on: R05, R08, R09, R11

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R16 — [Partner-Portal] Create the HubSpot connector read projection

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Using the approved test environment, import a company/contact/deal association with account-scoped IDs. Service consumers see only granted CRM records and a freshness timestamp.

Depends on: R02, R03, R08, R09, R11

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R17 — [Partner-Portal] Recover HubSpot inbound changes

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Verify notification authenticity, deduplicate and reread source state; test missed/reordered events, grant/token revocation, rate limits and deletion. Projection freshness is visible and stale authorization fails closed; deletion does not trigger recreate. Follow quote-and-crm-controls.md state and lifecycle rules.

Depends on: R16

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R18 — [Partner-Portal] Publish quote summaries to HubSpot safely

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Implement durable account/object/entity-revision command ledger and mapping through Prepared/InFlight/Uncertain/Verifying/NeedsOperator/terminal states. Timeout after success with delayed visibility never causes blind duplicate create. Prove bounded retries, uncertainty deadline/escalation, safe operator decision, unique readback and field ownership; absent search is not proof of no commit.

Depends on: R03, R16

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R19 — [Partner-Portal] Validate one technical quote fixture set

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Specify canonical technical configuration digest and rule-set version. Test ports, 500 W versus 370 W, required license and valid 20-AP fixtures; classify price-only versus technical changes with Commercial/technical owners. Unsupported rule families are blocked or expressly excluded per source coverage. Persist exact digest, findings and validity; executed evidence is a future gate.

Depends on: R04, R07, R08, R15

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R20 — [Partner-Portal] Create the immutable quote snapshot

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Bind quote revision to package/configuration digest, technical rule version, exact catalog and price evidence, currency/NRC/MRC/term and expiry. One scoped command produces one snapshot. Preserve lawful history under selected retention/redaction/hold policy. Native technical edits create a new draft and invalidate matching proof; no platform selected without supported enforcement.

Depends on: R08, R13, R15, R19

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R21 — [Partner-Portal] Apply quote approval and revision rules

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Enforce Draft/TechnicallyValid/Priced/Approved/Issued transition authorities in quote-and-crm-controls.md. Native 20-AP edit removing switch/license must prevent native and integrated approval/issue until new digest validates. Price-only edits require reprice/reapproval; unknown changes revalidate technically. Expiry during approval blocks issue. Buyer acceptance/deal-won/order are separate; selected CRM-link policy enforced.

Depends on: R20

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R22 — [Partner-Portal] Deliver durable service events

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Durable outbox and deduplicating consumers survive restart. Before first consumer, publish provider-owned event schemas, supported versions, ordering/idempotency/retry limits, solution-bound replay and dead-letter lifecycle; demonstrate compatibility/rollback and operator handling. Audit uses redacted operational envelope, not unrestricted domain payload.

Depends on: R09, R15, R20

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R23 — [Partner-Portal] Render and quarantine proposal artifacts

Phase: P1 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Render only exact approved configuration/commercial digests, hide internal cost and validate totals. Quarantine/bound input, files, worker resources and egress before use. Recheck expiry/grants/technical evidence at issue, including native CPQ edits while rendering; revoke downloads within policy bounds and expire exports. Repeated jobs cannot issue conflicting revisions.

Depends on: R21, R22

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R24 — [Partner-Portal] Reconcile an integrated pilot quote

Phase: P1 | Priority: High | Accountable role: Quality | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Demonstrate Marketplace/package/quote/proposal/CRM journey. Include native switching/license removal, price-only change, expiry during approval/render and timeout-after-success with delayed CRM visibility. No invalid quote issue or duplicate create; Pending CRM sync stays visible without altered totals. Apply selected outage policy and retain exact evidence versions.

Depends on: R14, R17, R18, R23

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R25 — [Partner-Portal] Test standalone and cross-tenant failures

Phase: P1 | Priority: High | Accountable role: Quality | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Portal outage preserves native access; shared-data/vendor outage reports accurate degradation. Exercise all three authority axes across API/files/jobs/AI/export surfaces in pilot scope, with forged context, revoked grants and unauthorized support. Include deletion/replay/restore denial cases, not just different partner IDs.

Depends on: R24

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R26 — [Partner-Portal] Restore and accept the pilot

Phase: P1 | Priority: High | Accountable role: Platform | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Accept only scoped pilot with each earlier first-exposure SYN/REAL checklist already satisfied, named accountable operators and applicable approvals. Prove isolated restore, revocation/tombstone replay, support denial, credential rotation and audit redaction; reconcile HubSpot and journey reliability. Product records acceptance or blocked capabilities; unknown controls/data policies cannot pass on functional success.

Depends on: R25

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R27 — [Partner-Portal] Prove independent floor plan access

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Before any selected planner configuration/upload, R07/R08 must hold passing rights/SSO/isolation/region/export evidence for this capability, plus SYN/REAL checklist. Demonstrate independent access and calibrated approved file, upload/egress containment and separate state/recovery. Unknown Hamina/incumbent rights block use; a synthetic custom geometry slice does not claim RF or non-Wi-Fi simulation.

Depends on: R07, R08, R09, R11, R26

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R28 — [Partner-Portal] Map floor plan output to a package

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Map canonical devices, source revision and geometry references through a supported contract and consumer compatibility proof. Enumerate lost export fields (including unavailable power/port/geometry facts), manual enrichment and labor. Missing evidence blocks applicable technical validation; successful import is not RF accuracy or full round-trip proof.

Depends on: R15, R27

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R29 — [Partner-Portal] Launch standalone discovery import

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Launch only approved file-import assessment with first-use checklist and isolated observation store. Persist source/time/device and deduplicate batches; validate malicious/oversized files. Observations are not authoritative inventory or iTop replacement. NetBox requires OD-10; no active scan is authorized by this item.

Depends on: R07, R08, R09, R11, R26

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R30 — [Partner-Portal] Publish reviewed discovery dispositions

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Review KEEP/REUSE/UPGRADE/REPLACE/ADD and export versioned provenance. Only confirmed technically acceptable reuse reduces new quantities; unknown devices remain unresolved. Define observation expiry and source-owned references; no new detailed CMDB authority.

Depends on: R15, R29

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R31 — [Partner-Portal] Launch the independent multisite workspace

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Apply service-specific first-use/isolation/restore gates before staging a 60-site file in a standalone workspace bound to one solution/environment. Show row errors and confirmation; prove same-partner/different-customer separation. Optional CRM references do not grant access or cause immediate create.

Depends on: R08, R09, R11, R26

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R32 — [Partner-Portal] Version profiles and site overrides

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Apply a profile revision to 40 sites and one local override. Preview later changes and preserve source revisions. A repeated application creates no duplicate quantities.

Depends on: R31

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R33 — [Partner-Portal] Export the multisite solution package

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Expanded BOM equals per-site totals. Source sites/profile revisions and overrides remain traceable. Existing issued quotes do not change after a new site revision.

Depends on: R15, R32

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R34 — [Partner-Portal] Publish entitled AI knowledge

Phase: P2 | Priority: High | Accountable role: Catalog steward | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Publish governed specifications/battle cards with owner, rights, class, version, region and expiry. Source/grant revocation invalidates retrieval, chunks, caches and queued jobs within approved bounds; stale authority fails closed. AI content publication is not the deferred human comparison/resources experience.

Depends on: R03, R12, R26

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R35 — [Partner-Portal] Launch independent AI retrieval

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: First-use AI checklist verifies provider/model rights/region/retention, protected endpoint and URL/egress controls, scoped conversations/indexes, direct login/local grants, cancellation and budgets. Prove all three authority axes, revocation during retrieval and source deletion/restore behavior before real-data exposure.

Depends on: R07, R08, R09, R11, R34

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R36 — [Partner-Portal] Submit reviewed AI solution proposals

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Typed tool produces a proposed package/diff for user review. Receiving service reauthorizes and validates. AI has no table-write, approval, proposal-send or order capability.

Depends on: R15, R35

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R37 — [Partner-Portal] Evaluate AI quality and failure isolation

Phase: P2 | Priority: High | Accountable role: Quality | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Run 50 grounded cases plus malicious retrieval and cross-tenant attempts. Report quality and cost. Disable AI and prove Marketplace/manual quoting still works.

Depends on: R36

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R38 — [Partner-Portal] Complete portal handoff contracts

Phase: P2 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Before each portal consumer uses a provider contract, prove version/limits/error/rollback compatibility and context/grant validation. Portal composes service visibility without authority; native access survives portal failure. Contain unavailable vendor/bad token and make handoff status truthful.

Depends on: R28, R30, R33, R37

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R39 — [Partner-Portal] Accept five independent service workflows

Phase: P2 | Priority: High | Accountable role: Quality | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Demonstrate five independent thin workflows only for expressly included capabilities, each with native access/state/release ownership, first-use checklist and supported package contract. Release one without changing others; record vendor equivalents and source-coverage exclusions. This does not accept deferred RF/non-Wi-Fi/rule/lifecycle breadth.

Depends on: R38

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R40 — [Partner-Portal] Expand specialist RF accuracy and fidelity proof

Phase: P3 | Priority: High | Accountable role: Solutions lead | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Expand RF accuracy/fidelity proof only for a candidate with selection rights/SSO/isolation/export gates passed before its first use. Test approved fixture and document remaining work; this later item cannot authorize earlier R27/R28 use. Non-Wi-Fi functions need their own scope/evidence before claims.

Depends on: R28, R39

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R41 — [Partner-Portal] Authorize a discovery collector scope

Phase: P3 | Priority: High | Accountable role: Security | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Before any active scan, reconfirm selected scanner rights and approve exact customer/lab targets, protocols, local secrets, identity, egress/kill switch, operator and SYN/REAL checklist. R07/R08 selection evidence precedes configuration; late approval does not legalize prior scans.

Depends on: R07, R08, R30, R39

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R42 — [Partner-Portal] Demonstrate one discovery collector feed

Phase: P3 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Only after R41, ingest one authorized lab/vendor collector batch with source mapping, bounded retry and observation expiry; test disconnected/duplicate recovery and scoped credential handling. Record known/unknown device coverage and follow-on scope; no universal discovery claim.

Depends on: R41

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R43 — [Partner-Portal] Compose a HubSpot customer lifecycle view

Phase: P3 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: After OD-10, compose authorized HubSpot context, source-owned package/quote links and one explicitly selected lifecycle feed with freshness. No second CRM or detailed inventory/ticket/topology replica; preserve iTop and use owner ICR if affected. First-use checklist and grant/source revocation apply; broader lifecycle remains excluded pending approval.

Depends on: R03, R17, R18, R39

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R44 — [Partner-Portal] Build a reconciled reporting projection

Phase: P3 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Create only approved minimized solution-scoped reporting projection. Reconcile version counts/values without revision double counting. Apply three-axis grants, selected retention/region, source tombstones, cache/export expiry and restore replay; no central detailed customer data lake. CON and REAL/SYN proof precede first use.

Depends on: R03, R22, R39, R43

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R45 — [Partner-Portal] Prove report formats and BI isolation

Phase: P3 | Priority: High | Accountable role: Engineering | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Prove one approved report in PDF/Excel/CSV/PPT with filters/as-of and genuine format fidelity. Test all three authority axes including cached/scheduled/export/service-principal paths, download revocation and expiry; document unavoidable downloaded-copy limits. Remaining strategy reports require separate scope/funding.

Depends on: R44

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required
- CON checklist and provider/consumer compatibility evidence before first use; R46 cannot substitute

## R46 — [Partner-Portal] Test compatibility and vendor exit

Phase: P3 | Priority: High | Accountable role: Quality | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Expand prior first-use compatibility tests into vendor exit/recovery: supported previous versions, solution state/canonical references, lost fields, deletion/backup expiry, legal holds and revoked grants after export/restore. Record migration owner and gaps; this is not the first consumer contract proof.

Depends on: R40, R42, R45

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R47 — [Partner-Portal] Exercise enterprise security and recovery

Phase: P3 | Priority: High | Accountable role: Security | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Regress earlier service launch controls across all approved scope: three-axis isolation, support elevation denial, credentials, bounded revocation, lifecycle purge, immutable redaction and backup/restore reconciliation. Record independent Security decisions for material exceptions; none are preapproved. Do not defer initial controls to this item.

Depends on: R46

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R48 — [Partner-Portal] Accept integrated service operations

Phase: P3 | Priority: High | Accountable role: Delivery lead | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Reconcile actual supported scope, staffing/TCO, vendor/manual-handoff costs, named operators/on-call, journey SLIs and recovery evidence with funded baseline. Each vendor outage counts in journey measurement. Accept precise release scope or keep unresolved capabilities blocked; no assumption-based schedule or SLO claim.

Depends on: R47

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
- Service-specific vendor/authority/policy decisions and SYN or REAL checklist in release-and-operations.md before first exposure; named operators required

## R49 — [Partner-Portal] Scope order and billing integration

Phase: Later | Priority: Medium | Accountable role: Commercial | Historical timebox: 3 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Specify ERP/order master, idempotency, tax and subscription handoff. Produce a funded, small-item backlog before committing implementation.

Depends on: R48

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work

## R50 — [Partner-Portal] Review internal service decomposition

Phase: Later | Priority: Medium | Accountable role: Technical lead | Historical timebox: 2 person-days

Estimate status: historical_timebox_reestimate_required

Acceptance: Keep the five independent business boundaries. Use measured load and team ownership to decide whether any shared/internal component needs further separation.

Depends on: R48

Source: Platform_Strategy_Updated.pdf and user brief; EA v2; source-evidence.md

Gates:

- Exact-revision EA re-review, explicit user scope approval, and applicable affected-owner/Security acceptance before consequential work
