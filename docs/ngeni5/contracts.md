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

Provider changes: unknown until existing contract is inspected. API/claims, registration, configuration and deployment effects require SSO owner assessment. Domain data/schema changes in SSO are not requested. Partner-Portal owns clients, role/grant mapping, sessions and negative tests. No edits to SSO are authorized here.

Compatibility: preserve existing clients, use approved claims and deprecation policy. Rollback: disable the new consumer registration and local routing without disrupting existing consumers. Acceptance: login/logout, revocation, wrong audience, forged solution context, support access and direct-native service tests. Required approvals: SSO owner plus applicable EA and user scope approval before implementation.
