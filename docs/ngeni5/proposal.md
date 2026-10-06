# Partner Portal enterprise architecture proposal

NGENI-5 — author revision 1 responding to PP-EA-2026-10-06-v2, 6 October 2026.

**Proposed documentation only. Five blockers were outstanding in the reviewed baseline. Author corrections request EA re-review; no closure, implementation or procurement approval is claimed.** See [finding dispositions](reviews/author-revision-1.md) and [approval status](reviews/status.md). The historical revision-2 DOCX/PPTX are not this design's approval target.

## Architecture direction

Integrate five independently usable business services: Marketplace, Floor Plan, Discovery, AI Solution Builder and Multi-Site Designer. Each may be purchased, self-hosted or custom, with native access, owned state and independent release/operations. The portal supplies navigation, context selection and status. Service visibility is a projection of service-owned grants; it never grants protected access. Each application logs in directly through approved SSO and enforces local membership and resource permissions. Portal failure does not remove native access, though shared SSO and commercial dependencies still affect availability.

HubSpot remains the CRM. Existing SSO's conditional Keycloak decision remains provider-owned. Shared product/pricing data are permitted by the user, but the physical master, field writers, confidential-price scope and interfaces remain OD-02 decisions. Consumer access uses owner APIs or governed exports, never cross-product SQL. No service may write another service's internal tables.

[Service boundaries](service-boundaries.md) define ownership and runtime alternatives. Recommend scoped corporate navigation/public catalog plus isolated customer-solution execution/state. Product/Security/EA must select topology before R09 or any sensitive SaaS import. Partner, customer, solution, environment and service workspace are separate identities with explicit collaboration grants; common partner membership is not customer access. [Authority and lifecycle](authority-and-lifecycle.md) defines cardinality, state placement, negative cases, support and restore. It also defines record-class retention/revocation gates; no real-data use with unset policy values.

## Shared capabilities and microservice assessment

| Capability | Proposed boundary and runtime assessment |
| --- | --- |
| Portal/BFF | Separate portal UI; thin composition logic may be a module in its provider. No new common gateway or centralized authorization engine selected. |
| Product/pricing | One writer per field, canonical products separate from supplier offers/pricebook versions. Adapter over selected master or owned service; catalog/pricing may be modules of that authority. Protected prices/costs require explicit scope and expiry. |
| Package exchange | A versioned capability, not an automatically separate microservice. Prefer evaluating a package module in the quote provider first; compare adapter/library and separate service in OD-09 before R15. |
| Quote/proposal | One purchased/custom authority owns exact quote revisions, approval and issued totals. Technical validation may be an owned module. Rendering reads approved data and cannot recalculate totals. |
| HubSpot adapter | Owns account-scoped ID mapping, minimized grants-controlled projection, field transforms and durable reconciliation ledger. Runtime separation depends on owner/failure evidence in OD-08; CRM authority remains HubSpot. |
| File processing | Isolated bounded parser/render execution and quarantine per solution scope; sharing worker code does not authorize shared customer files/credentials. |
| Reporting/lifecycle | Approved minimized read projections and source links; independent processing where justified. No detailed cross-customer CMDB or second CRM master. |

The five business boundaries are required; their internal modules are not automatically services. Reuse contracts and provider modules before adding runtimes. Shared source repositories/templates can help delivery but confer no shared customer state or recovery authority. [ADR register](decisions/README.md) preserves proposed choices and owner gates.

## Handoff, quotes and CRM

Each service submits a versioned package: namespaced workspace plus customer/solution/environment context, source revision, canonical product/specification IDs, site/profile overrides, quantities/units, dispositions, assumptions and authorized evidence references. Server-side identity/configuration binds scope. Mapping/schema errors fail submission; repeated scoped command IDs preserve one outcome. R05 establishes contract versions/limits; every consumer proves compatibility before first use.

Technical approval binds a deterministic configuration digest and rule version; commercial approval binds exact price evidence and quote revision. Native CPQ edits cannot bypass validation. Price-only changes still need commercial reevaluation/approval; technical changes need new technical proof. Expiry is checked at approval and issue. Immutable business history is governed by explicit redaction/tombstone/hold policy rather than indefinite personal-data retention. [Quote and CRM controls](quote-and-crm-controls.md) defines transition authorities and future bypass tests.

HubSpot company/contact/deal field authority is proposed pending CRM administrator confirmation. Quote approval is not buyer acceptance, deal-won or order creation. On timeout after a possible CRM create, the adapter enters Uncertain and reconciles boundedly; absence from delayed search never permits blind duplicate create. Operator escalation, retry bounds, grant freshness and quote-issue outage policy are OD-04/07 gates. Designs may start in an isolated provisional workspace; real data requires classified ownership, and a customer quote's CRM-link policy must be approved before issue.

Discovery is observation/assessment, not an authoritative enterprise inventory. Existing iTop ownership remains intact; any future integration uses its supported contract and owner-led ICR. NetBox is optional only after OD-10 decides intended inventory scope. Customer 360 does not copy detailed topology, tickets or monitoring policy.

## Build versus buy

[Solution analysis](solution-analysis.md) and [attributed EA research](solution-research-evidence.md) compare Medusa/CloudBlue/thin custom Marketplace; HubSpot/QuoteWerks/conditional ERPNext/custom quote authority; specialist planning/discovery versus limited custom/import routes; managed/self-hosted AI; and custom/vendor-extension Multi-Site.

Evaluate HubSpot and QuoteWerks first for quoting; compare commerce foundation and channel platform before committing to custom Marketplace. Prefer specialist planning proof before building RF; preserve import-only Discovery as an explicitly limited alternative. Thin custom Multi-Site is a hypothesis for profile/override semantics. No candidate is selected: rights, SSO, isolation/recovery, export fidelity and operating ownership are pass/fail gates. Unknown evidence blocks the option or requires an explicitly accepted capability exclusion. Late R40-R42 evidence cannot authorize early use. Monetary comparisons await contractual costs and labor/volume inputs.

## Delivery, security and operations

[Release and operations](release-and-operations.md) separates synthetic fixtures from first real identity/data exposure, maps owners/checklists to each service and attaches contracts/security/recovery evidence to first use. R26 cannot approve a pilot on functionality alone; R47/R48 extend evidence rather than introduce initial controls. Upload/egress/AI-fetch containment, scoped support, audited access and restore isolation precede applicable exposure. Actual evidence remains future implementation work after approval.

| Phase | Planning outcome | Gate |
| --- | --- | --- |
| P0 R01-R08 | Scope, field authority, contracts, candidate evidence, owners and funding breakdown | Hard gates passed for included capabilities; unresolved ones explicitly excluded or blocked; EA/user/affected-owner/Security approvals as applicable |
| P1 R09-R26 | Marketplace-to-approved-quote-to-HubSpot thin pilot | First-use checklists, native CPQ bypass proof, compatibility, three-axis access and isolated restore; no real data before REAL checklist |
| P2 R27-R39 | Thin independent planning/import/AI/Multi-Site handoffs | Each service's own selection/first-exposure gate; fidelity and unsupported capabilities visible |
| P3 R40-R48 | Separately authorized specialist extension, active collector, lifecycle/report slices and broader operations | New rights/scope before expanded use; source coverage and exit/recovery evidence |
| Later R49-R50 | Order/billing business case and measured internal decomposition | Separate approval and refined work breakdown |

The original 133-person-day seed and 144–200-person-week envelope had different scopes. Expanded acceptance invalidates any unchanged schedule inference. [Estimate reconciliation](release-and-operations.md) exposes the unallocated gap and requires staffing, stewardship, vendor lead times, operations and contingency before a new commitment. No calendar, cloud, monetary budget or numerical SLO is approved.

## Decisions and strategy coverage

[OD-01–OD-10](decisions/open-decisions.md) assign accountable roles, required evidence and the exact work blocked by missing decisions. Cleber must identify accountable people and business inputs; the author cannot accept policies or vendor terms for them. [Source coverage](source-evidence.md) distinguishes planned thin slices from bounded proposed exclusions for human resources, non-Wi-Fi planning, broader rules and lifecycle/reports. No feature is implemented.

Current CTO narrative: [decision brief](decision-brief.md). Approval should bind an exact revision, funded scope, policy values and exclusions after EA re-review. Silence, a green check or a documentation merge is not approval.
