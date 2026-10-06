# Proposed API and event contract inventory

**Design inventory only. No API implementation or approved endpoint is introduced.** Search existing domain contracts before defining new operations. User, workload and deployment authority must derive from verified identity and trusted configuration, not caller-selected tenant or CRM IDs.

| Contract | Provider responsibility | Exposure / intended consumers | Required boundary and evidence |
| --- | --- | --- | --- |
| Identity/SSO | Existing SSO repository and owner | customer/partner human flows; workload flows separately | Approved audience/claims, lifecycle, revocation and supported OIDC/SAML; ICR if provider changes |
| Product/eligible offers | Selected product/pricing owner | partner for eligible browsing; workload for tools | Entitlement applied to search and ID lookup; classified price fields, versions and expiry |
| Price evaluation | Selected commercial authority | workload quote consumer | Canonical product IDs, decimal NRC/MRC, currency/term, price evidence, policy version and failure behavior |
| Package submit/read | Selected exchange owner, runtime still under review | workload source/quote consumers; authorized human review | Immutable source revision, scoped namespace, schema version, hash, idempotency and product-map errors |
| Quote lifecycle | Selected quote authority | partner/customer as approved; internal approvers | Permission/approval separation, exact version, expiry, conflict and status transition rules |
| CRM projection/commands | Partner-Portal HubSpot adapter | internal/workload, scoped product clients | HubSpot account plus external IDs, field ownership, freshness, command ledger and readback |
| Collector ingest | Discovery solution owner | workload, bound to one solution/environment | Authorized collector identity, bounded batch, provenance and dedupe; no unrestricted inventory exposure |
| Reporting export | Reporting owner within approved solution | partner/customer with explicit grants | Filters, version/as-of, data class, size limits, download authorization and retention |

Before adoption, each record needs a named owner, consumers, stable identifiers, machine-readable schemas, pagination, limits, errors, retries, timeout/idempotency rules, audit/retention, compatibility window, consumer negative tests, support/disablement and retirement path. Register the shallow contract with EA without publishing secrets, topology or runtime credentials.

## Candidate events

CatalogRevisionPublished, SolutionPackageSubmitted, QuoteApproved and CRMProjectionUpdated describe committed facts. Define event ID, occurrence time, producer, schema version, permitted solution context, ordering scope, correlation, dedupe, replay, deletion and dead-letter policy. Operational telemetry follows the EA telemetry envelope; domain payload remains provider-owned. A shared schema does not authorize a shared multi-customer broker or telemetry pool.

## Draft SSO integration request

Requesting repository: Partner-Portal. Affected repository: SSO. Status: Draft, owner acceptance pending.

Observable need: approved users access the portal and each independent service with supported single sign-on while product services retain authorization. Workload tokens need distinct audiences/scopes. Native vendor SSO compatibility must be assessed separately.

Provider ADR baseline is inspected; supported runtime claims/client onboarding still require owner confirmation. Provider changes remain unknown until the concrete integration contract is assessed. API/claims, registration, configuration and deployment effects require SSO owner assessment. Domain data/schema changes in SSO are not requested. Partner-Portal owns clients, role/grant mapping, sessions and negative tests. No edits to SSO are authorized here.

Compatibility: preserve existing clients, use approved claims and deprecation policy. Rollback: disable the new consumer registration and local routing without disrupting existing consumers. Acceptance: login/logout, revocation, wrong audience, forged solution context, support access and direct-native service tests. Required approvals: SSO owner plus applicable EA and user scope approval before implementation.

## Proposed security acceptance evidence

These are design criteria for EA and owner review, not executed tests or implemented controls. Confirm scope and measurable limits before implementation.

| Boundary | Required evidence |
| --- | --- |
| SSO and authorization | Use the existing SSO baseline in ADR-0004. Direct URLs and portal links enforce identical application-local permissions. Wrong issuer/audience, expired tokens, forged organization context and guessed resource IDs fail closed. Verify revocation and logout separately for purchased services. |
| Product and pricing | Search, ID lookup, export and quote evaluation enforce consistent eligibility. Prevent cross-partner disclosure of negotiated prices. Distinguish public catalog data from customer-sensitive discounts. |
| Solution isolation | Prove isolation across credentials, databases, files, queues, caches, telemetry, backups and AI context. Include restore, export, replay and support workflows. |
| HubSpot | Define field authority and conflict policy. Verify callbacks using provider-supported mechanisms, deduplicate deliveries, bound retries and reconcile by readback. CRM identifiers alone never authorize access. |
| Quote approval | Bind approval to immutable quote revision and price evidence; specify edit invalidation and separation of preparation, approval and override responsibilities. |
| Discovery and imports | Bind collectors to approved solution/environment and scan scope. Constrain egress, malicious imports, file parsing and resource consumption. |
| AI builder | Authorize retrieval and export; treat retrieved content as untrusted. No autonomous commercial commitment or infrastructure mutation. Establish retention, provider use terms and deletion/export behavior. |
| Operations | Specify elevation, credential rotation, audit protection, recovery objectives, restore evidence, incident ownership and vendor exit. Numerical objectives remain owner decisions. |

Map accepted evidence into existing backlog items during findings reconciliation. No implementation authority follows from this table.

## Author revision 1 binding semantics and timing

The identifier/cardinality and grant model in [authority and lifecycle](authority-and-lifecycle.md) applies to every contract: `partner_id` is not the protection boundary; `customer_id`, `solution_id`, trusted `environment_id`, service-namespaced `workspace_id` and explicit local grants are distinct. CRM references include account/object/record and never authorize access. Use server-derived environment binding and reauthorize source/destination transfers. Retention, revocation, job/cache/export/backup bounds and restore tombstones are contract requirements with owner-set numeric gates before real data.

Quote operations use the configuration digest, rule version, exact commercial evidence and state guards in [quote/CRM controls](quote-and-crm-controls.md). CRM command results expose Pending/Uncertain/NeedsOperator/Confirmed rather than hiding uncertain writes. Retries cannot create a duplicate after delayed visibility.

[CON and first-use mapping](release-and-operations.md) assigns schema, supported-version/rollback, limits and consumer evidence to R05, R12-R18, R22, R28/R33, R34/R35, R38 and R43-R45. The backlog repeats these gates in both formats. No independently released consumer waits until R46 for compatibility proof. Package API ownership/runtime is OD-09, resolved before R15 using [exchange alternatives](service-boundaries.md). No extra exchange service is selected by this inventory.
