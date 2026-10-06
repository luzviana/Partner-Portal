# Partner Portal implementation backlog

NGENI-5 / Repository review draft 3 / 6 October 2026

**Implementation blocked pending EA review and explicit user approval.**

R01-R50 remain proposed planning items. Their listed dependencies are necessary but not sufficient: all build, provisioning, configuration and deployment actions also require the [approval gate](reviews/status.md). R02-R08 can be refined as documents while review is pending, but access changes, paid trials, live CRM writes and deployment are not authorized. SSO, customer-solution isolation and API constraints in [governance reconciliation](governance-reconciliation.md) override generic platform options.

The DOCX is the previous revision-2 snapshot. This Markdown and backlog.json are the current review sources.

These 50 revised items implement the independent-service architecture and the confirmed HubSpot CRM integration. R01-R50 supersede the earlier B01-B50 planning list. They are local planning IDs, not created task-system records. All begin in Backlog and retain the [Partner-Portal] prefix.

The portal integrates Marketplace, Floor Plan, Discovery, AI Solution Builder and Multi-Site Designer as independent solutions. Shared product/pricing, solution exchange and quote authority connect them. P1 includes HubSpot integration; choosing a CRM is no longer a discovery item.

Each estimate is 2-3 focused person-days for one accountable role. Split a task if its acceptance outcome cannot fit that timebox. The seed totals 133 person-days and is not a complete program estimate. Vendor assessments and thin integration slices must produce further small tasks before full capability commitments.

### Definition of done

Reviewed contracts and code/configuration, focused acceptance evidence, tenant and failure checks, service owner and rollback notes where relevant. Vendor fixtures do not prove production rights or universal device coverage. P0 and phase gates distinguish verified behavior from assumptions.

### Dependency and autonomy rules

A dependency means its acceptance outcome is required. Teams can work concurrently once dependencies pass. A service must retain native access, owned state, supported handoff and its own release/operating boundary. Shared identity/data dependencies remain documented.

| Phase | IDs | Outcome |
| --- | --- | --- |
| P0 | R01-R08 | Authority, HubSpot, solution fit and contracts |
| P1 | R09-R26 | Independent Marketplace and integrated quote pilot |
| P2 | R27-R39 | All five independent service workflows |
| P3 | R40-R48 | Specialist proof and operating readiness |
| Later | R49-R50 | Additional investment decisions |

References use the companion architecture proposal revision 2: S1 is the 24-page PDF, S2 the user brief and clarification, S17-S18 HubSpot primary sources. No application implementation or CRM modification has occurred in preparing this backlog.

## Backlog items R01 to R05

### R01  [Partner-Portal] Agree pilot scope and service autonomy

P0   /   High priority   /   Owner: Product   /   2 person-days

Acceptance: Name two partners, country, currency and portfolio. Define standalone and portal acceptance for all five services. Confirm Marketplace as the first pilot entry point.

Depends on: None.  Source: S2 and architecture revision 2.

### R02  [Partner-Portal] Inventory HubSpot integration capabilities

P0   /   High priority   /   Owner: CRM admin   /   2 person-days

Acceptance: Record actual account count, subscription, app model, API version, scopes and relevant objects. Identify an approved test environment and gaps without changing production data.

Depends on: R01.  Source: S17-S18.

### R03  [Partner-Portal] Agree CRM field owners and tenant mapping

P0   /   High priority   /   Owner: CRM admin   /   2 person-days

Acceptance: Map company/contact/deal fields, partner visibility, source IDs and outbound quote fields. Approve conflict, deletion and outage rules. No field has two uncontrolled writers.

Depends on: R02.  Source: S2 and architecture revision 2.

### R04  [Partner-Portal] Choose product pricing and quote authorities

P0   /   High priority   /   Owner: Commercial   /   3 person-days

Acceptance: Compare HubSpot, existing catalog/ERP and custom or OSS options on 10 golden quote cases. Record D01/D02, costs, entitlement gaps and one authoritative calculator.

Depends on: R02.  Source: S9, S18.

### R05  [Partner-Portal] Publish the solution package contract

P0   /   High priority   /   Owner: Technical lead   /   2 person-days

Acceptance: Version schema for tenant, workspace, source revision, sites, products, quantities and provenance. Validate examples from all five services, including an unmapped product.

Depends on: R01, R03, R04.  Source: S2 and architecture revision 2.

## Backlog items R06 to R10

### R06  [Partner-Portal] Approve identity and service access contracts

P0   /   High priority   /   Owner: Security   /   2 person-days

Acceptance: Define direct-service and portal login, service identity, CRM record grants and data regions. Document two-tenant access cases and vendor SSO dependencies.

Depends on: R01, R03.  Source: S2 and architecture revision 2.

### R07  [Partner-Portal] Assess five service solution candidates

P0   /   High priority   /   Owner: Solutions lead   /   3 person-days

Acceptance: Record build/buy candidate and standalone/handoff fit for each service. Check API/export and licensing evidence or mark it unknown. Produce small follow-on tasks for gaps.

Depends on: R05, R06.  Source: S2 and architecture revision 2.

### R08  [Partner-Portal] Approve governed data and delivery baseline

P0   /   High priority   /   Owner: Delivery lead   /   2 person-days

Acceptance: Obtain 20 entitled offers and 10 expected-price cases from named stewards. Re-estimate the pilot, staffing and unresolved vendor work. Record the P0 go/no-go decision.

Depends on: R04, R07.  Source: S2 and architecture revision 2.

### R09  [Partner-Portal] Establish independent deployment templates

P1   /   High priority   /   Owner: Platform   /   3 person-days

Acceptance: Create a reusable service template with separate identity, state credentials, health endpoint and release pipeline. Deploy two empty services and update one without redeploying the other.

Depends on: R08.  Source: S2 and architecture revision 2.

### R10  [Partner-Portal] Build the portal shell and service registry

P1   /   High priority   /   Owner: Engineering   /   2 person-days

Acceptance: Display entitled service links and active workspace context. Label unavailable services honestly. One service failure does not prevent navigation to available services.

Depends on: R06, R09.  Source: S2 and architecture revision 2.

## Backlog items R11 to R15

### R11  [Partner-Portal] Prove tenant authorization in two services

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Implement verified actor/tenant/resource checks in two pilot APIs. Direct URLs and forged tenant IDs cannot expose another partner. Portal access and native access use the same policy.

Depends on: R06, R09.  Source: S2 and architecture revision 2.

### R12  [Partner-Portal] Publish a canonical catalog API slice

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Publish 20 versioned offers with product/vendor IDs, eligibility and price references. Both list and ID lookup enforce grants. Revoke an offer and invalidate a sample consumer.

Depends on: R04, R08, R11.  Source: S2 and architecture revision 2.

### R13  [Partner-Portal] Implement authoritative price evaluation

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Pass the 10 approved NRC/MRC cases with decimal arithmetic, term, currency, version and expiry. If a vendor is master, use its supported result through the facade rather than a second calculator.

Depends on: R04, R12.  Source: S2 and architecture revision 2.

### R14  [Partner-Portal] Launch a standalone marketplace slice

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: A user opens Marketplace without the portal, browses entitled offers and exports a selection. The portal launches the same service with authorized context. Persist source revision.

Depends on: R12, R13.  Source: S2 and architecture revision 2.

### R15  [Partner-Portal] Accept immutable solution packages

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Exchange API stores a validated package and hash. Reject schema/tenant errors and unresolved product mappings. Repeating a submission ID returns the same package.

Depends on: R05, R09, R11.  Source: S2 and architecture revision 2.

## Backlog items R16 to R20

### R16  [Partner-Portal] Create the HubSpot connector read projection

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Using the approved test environment, import a company/contact/deal association with account-scoped IDs. Service consumers see only granted CRM records and a freshness timestamp.

Depends on: R02, R03, R09, R11.  Source: S2 and architecture revision 2.

### R17  [Partner-Portal] Recover HubSpot inbound changes

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Verify supported notification authenticity, deduplicate and re-read canonical state. Simulate missed and reordered changes; reconciliation restores the correct projection.

Depends on: R16.  Source: S17.

### R18  [Partner-Portal] Publish quote summaries to HubSpot safely

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Implement an outbound command ledger in the test environment. A timeout after remote success does not create duplicates. Readback verifies mapped quote fields and controlled proposal link.

Depends on: R03, R16.  Source: S2 and architecture revision 2.

### R19  [Partner-Portal] Validate one technical quote fixture set

P1   /   High priority   /   Owner: Engineering   /   2 person-days

Acceptance: Reject insufficient ports, 500 W load on a 370 W budget and a missing license. Persist rule version and findings with each package. Passing examples retain provenance.

Depends on: R08, R15.  Source: S1 p. 16.

### R20  [Partner-Portal] Create the immutable quote snapshot

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Bind an exchange revision to exact catalog, rules and price evidence. Reject expired price responses. One command ID produces one quote; later catalog changes leave it unchanged.

Depends on: R13, R15, R19.  Source: S2 and architecture revision 2.

## Backlog items R21 to R25

### R21  [Partner-Portal] Apply quote approval and revision rules

P1   /   High priority   /   Owner: Engineering   /   2 person-days

Acceptance: Only the authorized approver can approve the exact quote version. A material revision requires new approval. Missing CRM linkage blocks issue under the proposed pilot policy.

Depends on: R20.  Source: S2 and architecture revision 2.

### R22  [Partner-Portal] Deliver durable service events

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: An outbox survives service restart. Consumers deduplicate repeated package/quote events. Failed messages expose retry and operator state with end-to-end trace IDs.

Depends on: R09, R15, R20.  Source: S2 and architecture revision 2.

### R23  [Partner-Portal] Render and quarantine proposal artifacts

P1   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: An isolated worker renders an approved fixture, verifies totals and hides internal cost. Inputs are validated, object access is scoped and retry creates no conflicting final version.

Depends on: R21, R22.  Source: S2 and architecture revision 2.

### R24  [Partner-Portal] Reconcile an integrated pilot quote

P1   /   High priority   /   Owner: Quality   /   2 person-days

Acceptance: Marketplace selection reaches exchange and approved proposal, then verified HubSpot summary. Induce CRM outage and show pending sync without changing quote totals.

Depends on: R14, R17, R18, R23.  Source: S2 and architecture revision 2.

### R25  [Partner-Portal] Test standalone and cross-tenant failures

P1   /   High priority   /   Owner: Quality   /   3 person-days

Acceptance: Portal outage leaves native Marketplace access working. Test shared-data outage, forged context and cross-tenant file/API attempts. Expected denials and degraded status are explicit.

Depends on: R24.  Source: S2 and architecture revision 2.

## Backlog items R26 to R30

### R26  [Partner-Portal] Restore and accept the pilot

P1   /   High priority   /   Owner: Platform   /   3 person-days

Acceptance: Restore pilot authoritative stores, verify references and reconcile HubSpot projection. Measure agreed targets. Product owner records pilot acceptance or precise blocking defects.

Depends on: R25.  Source: S2 and architecture revision 2.

### R27  [Partner-Portal] Prove independent floor plan access

P2   /   High priority   /   Owner: Engineering   /   2 person-days

Acceptance: Configure selected solution or custom service with native access and separate state. Upload and calibrate one approved floor-plan file; identity and tenant boundaries pass.

Depends on: R07, R09, R11, R26.  Source: S2 and architecture revision 2.

### R28  [Partner-Portal] Map floor plan output to a package

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Map placed devices to canonical products and export source revision/geometry references. Review the BOM diff. Do not label unvalidated placement as RF coverage.

Depends on: R15, R27.  Source: S1 pp. 6-7.

### R29  [Partner-Portal] Launch standalone discovery import

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: A user imports one supported inventory file without the portal. Persist observation time/source and device identity. Repeated imports do not duplicate the same observation batch.

Depends on: R07, R09, R11, R26.  Source: S2 and architecture revision 2.

### R30  [Partner-Portal] Publish reviewed discovery dispositions

P2   /   High priority   /   Owner: Engineering   /   2 person-days

Acceptance: Review KEEP/REUSE/UPGRADE/REPLACE/ADD and export a versioned package. Only confirmed reuse reduces net-new quantities. Retain observation provenance.

Depends on: R15, R29.  Source: S1 pp. 8-9.

## Backlog items R31 to R35

### R31  [Partner-Portal] Launch the independent multisite workspace

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Create a standalone workspace and stage a 60-site CSV. Show row errors and confirm before save. Optional CRM references preserve grants and do not force immediate CRM creation.

Depends on: R09, R11, R26.  Source: S2 and architecture revision 2.

### R32  [Partner-Portal] Version profiles and site overrides

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Apply a profile revision to 40 sites and one local override. Preview later changes and preserve source revisions. A repeated application creates no duplicate quantities.

Depends on: R31.  Source: S2 and architecture revision 2.

### R33  [Partner-Portal] Export the multisite solution package

P2   /   High priority   /   Owner: Engineering   /   2 person-days

Acceptance: Expanded BOM equals per-site totals. Source sites/profile revisions and overrides remain traceable. Existing issued quotes do not change after a new site revision.

Depends on: R15, R32.  Source: S2 and architecture revision 2.

### R34  [Partner-Portal] Publish entitled AI knowledge

P2   /   High priority   /   Owner: Catalog steward   /   2 person-days

Acceptance: Publish approved specifications and battle cards with owner, version, entitlement and expiry. Revocation propagates to retrieval and cached snippets.

Depends on: R12, R26.  Source: S1 pp. 10-15, 24.

### R35  [Partner-Portal] Launch independent AI retrieval

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: AI service has its own endpoint, conversations and retrieval store. Direct native use and portal launch respect the same tenant grants. Add cancellation and per-tenant usage budgets.

Depends on: R09, R11, R34.  Source: S2 and architecture revision 2.

## Backlog items R36 to R40

### R36  [Partner-Portal] Submit reviewed AI solution proposals

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Typed tool produces a proposed package/diff for user review. Receiving service reauthorizes and validates. AI has no table-write, approval, proposal-send or order capability.

Depends on: R15, R35.  Source: S2 and architecture revision 2.

### R37  [Partner-Portal] Evaluate AI quality and failure isolation

P2   /   High priority   /   Owner: Quality   /   3 person-days

Acceptance: Run 50 grounded cases plus malicious retrieval and cross-tenant attempts. Report quality and cost. Disable AI and prove Marketplace/manual quoting still works.

Depends on: R36.  Source: S2 and architecture revision 2.

### R38  [Partner-Portal] Complete portal handoff contracts

P2   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Portal launches all five services with checked context and shows package handoff status. A bad vendor token or unavailable service gives a contained error and recovery path.

Depends on: R28, R30, R33, R37.  Source: S2 and architecture revision 2.

### R39  [Partner-Portal] Accept five independent service workflows

P2   /   High priority   /   Owner: Quality   /   3 person-days

Acceptance: Demonstrate native access, own state/release boundary and common quote handoff for every service. Deploy one custom service without changing others; document vendor equivalents.

Depends on: R38.  Source: S2 and architecture revision 2.

### R40  [Partner-Portal] Prove specialist RF integration rights

P3   /   High priority   /   Owner: Solutions lead   /   3 person-days

Acceptance: Test a licensed RF candidate with one floor-plan fixture. Record API/export/SSO rights, fidelity, accuracy evidence and remaining work. Unsupported scope gets explicit follow-on items.

Depends on: R28, R39.  Source: S2 and architecture revision 2.

## Backlog items R41 to R45

### R41  [Partner-Portal] Authorize a discovery collector scope

P3   /   High priority   /   Owner: Security   /   2 person-days

Acceptance: Approve customer/lab scope, protocols, local secrets, outbound identity and kill switch. Verify chosen scanner rights before any active scan.

Depends on: R30, R39.  Source: S2 and architecture revision 2.

### R42  [Partner-Portal] Demonstrate one discovery collector feed

P3   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: In the authorized lab or vendor sandbox, ingest one observation batch, preserve mapping and retry safely. Produce follow-on items for additional devices/protocols.

Depends on: R41.  Source: S2 and architecture revision 2.

### R43  [Partner-Portal] Compose a HubSpot customer lifecycle view

P3   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Show authorized CRM records with package/quote links and one supported lifecycle feed. Source/freshness is visible. No second editable CRM master is created.

Depends on: R17, R18, R39.  Source: S2 and architecture revision 2.

### R44  [Partner-Portal] Build a reconciled reporting projection

P3   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: Replay service events and CRM snapshots into a separate tenant-filtered read model. Reconcile quote version counts and values without counting revisions as new revenue.

Depends on: R22, R39, R43.  Source: S2 and architecture revision 2.

### R45  [Partner-Portal] Prove report formats and BI isolation

P3   /   High priority   /   Owner: Engineering   /   3 person-days

Acceptance: One approved report exports to PDF, Excel, CSV and PPT with correct filters and timestamp. Test tenant isolation. Record vendor/API gaps and more small tasks.

Depends on: R44.  Source: S1 pp. 22-23.

## Backlog items R46 to R50

### R46  [Partner-Portal] Test compatibility and vendor exit

P3   /   High priority   /   Owner: Quality   /   3 person-days

Acceptance: A previous supported package version still imports. Export one solution's state and canonical references for exit/recovery. Record vendor lock-in gaps and migration ownership.

Depends on: R40, R42, R45.  Source: S2 and architecture revision 2.

### R47  [Partner-Portal] Exercise enterprise security and recovery

P3   /   High priority   /   Owner: Security   /   3 person-days

Acceptance: Run cross-service tenant tests, credential rotation and restore/reconciliation drills. Resolve critical findings or record accountable risk decisions before release.

Depends on: R46.  Source: S2 and architecture revision 2.

### R48  [Partner-Portal] Accept integrated service operations

P3   /   High priority   /   Owner: Delivery lead   /   2 person-days

Acceptance: Each service has a named operating owner, SLO evidence, runbook and supported scope. Measure cost and accept release gates or list blocked capabilities.

Depends on: R47.  Source: S2 and architecture revision 2.

### R49  [Partner-Portal] Scope order and billing integration

Later   /   Medium priority   /   Owner: Commercial   /   3 person-days

Acceptance: Specify ERP/order master, idempotency, tax and subscription handoff. Produce a funded, small-item backlog before committing implementation.

Depends on: R48.  Source: S2 and architecture revision 2.

### R50  [Partner-Portal] Review internal service decomposition

Later   /   Medium priority   /   Owner: Technical lead   /   2 person-days

Acceptance: Keep the five independent business boundaries. Use measured load and team ownership to decide whether any shared/internal component needs further separation.

Depends on: R48.  Source: S2 and architecture revision 2.
