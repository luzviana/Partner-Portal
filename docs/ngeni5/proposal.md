# Partner Portal enterprise architecture proposal

NGENI-5 / Repository review draft 3 / 6 October 2026

**Status: Proposed. EA review and explicit user approval are pending. Implementation is blocked.**

This Markdown proposal is the current review source. [Governance reconciliation](governance-reconciliation.md) constrains all deployment and sharing proposals below. The DOCX/PPTX in `output/ngeni5` are retained revision-2 presentation snapshots, not approved architecture. The user has authorized drafting and review only. See [review status](reviews/status.md).

### Architecture direction

Deliver a portal that integrates independently usable services: Marketplace, Floor Plan, Discovery, AI Solution Builder and Multi-Site Designer. Each service can use a different purchased or custom solution, exposes a stable integration contract and retains its own release and operating lifecycle. HubSpot is the existing CRM. Common product and pricing capabilities connect the services to governed commercial data. [S1 pp. 1-2; S2]

The user has clarified that independent entry points are independent services. This revision replaces the earlier proposal to place those capabilities in one modular core. Independence is a product and solution boundary from the outset, even when delivery occurs in phases. A service may be a SaaS product with an adapter, a self-hosted product, or a custom application; it does not have to be a newly built microservice.

### Recommendation for shared data

Use one logical product and pricing authority with versioned APIs and controlled publication of catalog data. Service-owned databases retain floor plans, discovery observations, conversations and site designs. Shared product and pricing data do not require unrestricted database credentials for every application. A shared database host is an option only within a declared and approved solution boundary. EA isolation requirements apply across customer solutions. Consumers do not query another product's database; the earlier direct-read exception is withdrawn.

| CTO decision | Proposed direction |
| --- | --- |
| Service model | Approve five independently usable business services with a portal integration layer. |
| Existing CRM | Retain HubSpot. Define its field ownership and the integration contract during P0. |
| Commercial authority | Select one product/price master and one quote authority. Avoid competing calculators. |
| Delivery commitment | Fund P0 for 2-3 weeks. Re-estimate the integrated pilot after vendor and HubSpot fit tests. |

The proposal covers boundaries, solution choices, data contracts, security, phased delivery and unresolved decisions. The companion backlog contains 50 revised planning items. No application implementation, CRM mutation or deployment has been performed. All staffing and schedule numbers are planning assumptions.

## Independent services and the portal

The portal provides shared navigation, identity entry, service entitlements, context selection and workflow status. Each service remains reachable through its own supported interface. Start with authenticated links and API handoffs; embed a vendor UI only when its security model, licensing and browser behavior support embedding. [S1 pp. 1-2; S2]

| Service | Owns | Standalone outcome and integration |
| --- | --- | --- |
| Marketplace | Offer browsing, comparisons, saved selections and its presentation layer. | Browse entitled offers and export a selection. Consume shared catalog/pricing APIs. Hand off product IDs and quantities. |
| Floor Plan | Plan files, scale, geometry, placements and simulation jobs/results. | Create a design and export a BOM. Map vendor device IDs to canonical products. RF capability depends on selected solution. |
| Discovery | Scan/import jobs, observations, asset identity and disposition evidence. | Assess an environment and export reviewed observations. KEEP/REUSE/UPGRADE/REPLACE/ADD remains explicit. |
| AI Solution Builder | Conversations, grounded retrieval, proposed changes and evaluation traces. | Produce an explained proposal with provenance. Submit typed requests to authorized services for human review. |
| Multi-Site Designer | Site records, reusable profiles, overrides and site expansion revisions. | Compose a multisite solution and export a versioned BOM. Associate CRM references when available. |

### Independence acceptance test

Each custom service has its own deployable, versioned API, owned state, service identity, logs, health checks and rollback. A vendor service retains vendor-managed equivalents plus an owned adapter. Releasing or disabling one business service must not require redeploying the others. An outage in the portal must not disable a service's native access path. Shared identity and catalog dependencies remain explicit dependencies, not a promise of complete offline operation.

An independent assessment may begin without a HubSpot deal. It receives a namespaced service-local workspace ID mapped explicitly to the exchange context; authorization is never inferred from matching names. Before issuing a customer-specific quote, the user links the work to an authorized CRM company/contact/deal according to commercial policy. This avoids forcing every standalone workflow through the portal or an immediate CRM write.

## Shared capabilities and microservice assessment

| Capability | Boundary and ownership | Deployment assessment |
| --- | --- | --- |
| Portal and BFF | Own navigation, session composition and cross-service status. Never own CRM or design masters. | Separate portal deployment. BFF translates UI requests but does not replace service APIs. |
| Product and Pricing | Own canonical product IDs, vendor mappings, offers, eligibility, versioned pricebooks and deterministic price evaluation. | Independent shared service or adapter over selected master. Catalog and pricing can be internal modules initially. |
| Solution Exchange | Own immutable submitted BOM packages, source references and handoff status. Does not edit originating designs. | Small independent API and datastore. Decouples heterogeneous solutions and supports export/import fallback. |
| Quote and Proposal | Own quote snapshots, approval state, commercial policy and proposal artifacts. Invoke technical validation. | Independent service or purchased CPQ behind an adapter. Validation may remain an internal module here. |
| HubSpot integration | Own CRM ID mappings, sync checkpoints, event inbox/outbox, field transforms and reconciliation state. | Separate integration deployment from P1. HubSpot remains external CRM authority. |
| File processing | Own quarantine, parsing/rendering jobs and derived object lifecycle. | Isolated worker runtime due to file risk and resource use. It may serve several services through scoped jobs. |
| Reporting and lifecycle | Own read projections, metric definitions and report jobs. Customer 360 composes HubSpot and service records. | P3 independent workload and read store. Portal displays results; it does not become another CRM. |

### Boundaries do not require excessive fragmentation

The five business services are independent by requirement. Within each custom solution, use ordinary modules until a separate runtime is justified. Do not create a network service per calculation, table or screen. Likewise, an integrated vendor platform can supply several shared capabilities behind explicit contracts without forcing duplicate custom implementations.

All services can initially share a repository, container platform and CI templates. Independent deployment, ownership and data permissions must survive that operational convenience. Prefer managed infrastructure to accommodate the larger number of services.

## Shared product and pricing data

The user permits multiple services to connect to the same product and pricing database. The recommended implementation is a shared data authority exposed through contracts. Its physical location remains a decision: HubSpot product data, an existing ERP/PIM, or a dedicated catalog database may supply different mastered fields. No existing product master has been confirmed. [S2, S18]

| Pattern | Tradeoff | Recommendation |
| --- | --- | --- |
| Shared API with owned database | Consistent eligibility, auditing and version rules. Adds a service dependency and requires a supported API. | Default. All solutions resolve canonical IDs and request prices through an adapter or API. |
| Published snapshots or read models | Fast browsing and vendor import compatibility. Consumers must track version, expiry and deletions. | Use for search and offline assessment. Reprice and revalidate before quote issue. |
| Direct cross-product database reads | Lower integration effort for a compatible self-hosted tool. Couples schemas and can bypass tenant/price policy. | Rejected under the EA API standard. Use the owning product API or a governed export. Any exception needs explicit EA/Security review. |
| Multiple services write common tables | Appears simple but produces conflicting ownership and fragile migrations. | Do not adopt. Route each write to the field owner or controlled ingestion process. |

### Commercial contract

Separate Product from SupplierOffer and PriceBookVersion. A product carries technical identity; an offer adds supplier, region, currency, partner eligibility and effective dates. A price evaluation accepts an actor/tenant, eligible offer IDs, quantities, term and currency and returns exact NRC/MRC amounts, policy/rule version, effective time and expiry. Use decimal arithmetic and explicit rounding. Internal costs are permissioned fields, not general catalog attributes.

Illustrative contracts: ResolveProducts, GetEligibleOffers, EvaluatePrice and PublishCatalogRevision. Every response carries a version and provenance. CatalogChanged invalidates downstream caches. When HubSpot or a purchased CPQ is selected as price master, the shared service becomes its facade and does not run a competing commercial calculator.

A database outage may allow browsing a labeled cached catalog, but it must not silently produce a new approved quote from stale prices. Fail closed for issue/approval when required commercial evidence is missing or expired.

## HubSpot CRM ownership and mapping

HubSpot is confirmed as the current CRM. Proposed ownership is HubSpot for companies, contacts, deals, sales owners and pipeline stages. This is a recommendation to validate with the CRM administrator, not evidence that the current account already follows that model. No HubSpot account configuration or subscription has been inspected. [S2, S17]

| Information | Proposed master | Portal and service behavior |
| --- | --- | --- |
| Customer and contact | HubSpot company/contact | Store scoped external references and minimal read projections. Contact edits route through the integration contract. |
| Opportunity and sales stage | HubSpot deal and pipeline | Link designs and quotes to a deal. Portal uses mapped internal stage IDs, never display labels as identifiers. |
| Partner tenant and access | Identity/access configuration | Maintain partner-to-CRM visibility grants. A HubSpot company or account ID is not sufficient proof of tenant access. |
| Sites, profiles and designs | Multi-Site Designer / origin service | Persist technical detail in the owning solution. Link to HubSpot records with canonical workspace and source IDs. |
| Product and price | D01 selected shared authority | Map to HubSpot product IDs where needed. HubSpot availability does not decide ownership automatically. |
| Quote and proposal | D02 selected quote authority | Publish approved version, value/status and controlled link to HubSpot. Define which system can change each field. |
| Customer 360 and reporting | Rebuildable projections | Combine CRM, design, quote and later support references. Display source and synchronization freshness. |

### Context across solutions

Carry tenant ID, authorized actor, workspace ID and optional HubSpot company/contact/deal references. The connector resolves external IDs within the correct HubSpot account. Services validate context server-side rather than trusting IDs from a URL. Avoid copying the entire CRM into every service.

One shared HubSpot account for internal operations is the planning assumption. Multiple partner-owned accounts would require per-account authorization, credentials, mapping and operational isolation. Custom objects, app model, API scopes, commercial capabilities and external partner access depend on the actual account and remain open decisions.

## HubSpot integration and recovery

The integration service presents a narrow CRM contract to the other solutions. It consumes supported CRM change notifications, re-reads canonical records, and maintains a tenant-filtered local projection. Scheduled reconciliation recovers missed changes. The selected API version, event model and account limits must be verified during P0. [S17]

| Flow | Behavior | Failure policy |
| --- | --- | --- |
| HubSpot to services | CRM updates refresh mapped company/contact/deal projections and publish authorized change events. | Verify request authenticity for the chosen app model. Deduplicate events and handle out-of-order delivery by reading current state. |
| Services to HubSpot | Approved quote summary, proposal link and permitted deal updates enter a durable command queue. | Use a command ledger and stored external IDs. Read back after uncertain timeouts before recreating a record. |
| Retry and reconciliation | Use bounded retry/backoff, account-aware rate limiting, dead-letter handling and reconciliation reports. | Surface pending/failed status and an operator action. Prevent a sync echo from rewriting the same field indefinitely. |
| Data deletion or access change | Propagate tombstones, revoke projections and invalidate service caches/indexes. | Apply a documented retention policy and preserve only required audit evidence. |
| HubSpot outage | Previously linked standalone work may continue against a timestamped projection if policy permits. | Do not claim CRM synchronization succeeded. Block workflows requiring fresh CRM authorization/context until recovery. |

### Quote synchronization policy

A QuoteApproved event means a particular immutable version was approved. It does not automatically mean the deal is won or an order exists. Publish quote amount, currency, approved version and proposal link using agreed properties/associations. If quote revisions update deal value, define which accepted or active quote contributes and how NRC versus MRC is represented. Do not sum every revision into pipeline revenue.

Recommended pilot policy: associate the work with a confirmed HubSpot deal before issuing a customer proposal. A failed summary sync after approval stays visible as Pending CRM sync, retries durably and never regenerates or changes the quote total. The commercial owner must approve this degraded-mode policy.

## Solution handoff and quote integrity

Each tool owns its source state. A user explicitly submits a versioned solution package to the exchange. The exchange provides a stable envelope for vendor exports, APIs and custom services, allowing the quote workflow to operate without live access to the originating tool.

| Package field | Purpose |
| --- | --- |
| Identity and context | Package ID/revision, tenant, workspace, optional HubSpot deal reference, origin service and source revision. |
| Technical content | Site/profile references, product and supplier IDs, quantities, units, disposition and provenance. Include schema version and content hash. |
| Evidence | Source artifact links, assumptions, validation findings, product-map version and approved simulation evidence when applicable. |
| Commercial references | Catalog/price versions if known. These are references for validation, not permission for the originating service to approve a quote. |

### Lifecycle

The source exports a draft package. The exchange validates its schema, tenant and product mappings and records it immutably. The user reviews a diff before importing it into another solution or submitting it to Quote and Proposal. Unsupported or unmapped products enter a resolution queue. Concurrent edits produce a conflict; a later source change creates a new package revision.

Quote and Proposal resolves product eligibility, runs deterministic technical checks, requests authoritative pricing and stores the returned versions and inputs in its own immutable snapshot. Approval binds to that exact quote version. Rendering reads only the approved snapshot. A material design, policy or price change requires a new quote and approval. Distributed services do not share a cross-database transaction.

### Consistency rules

Use local transactions and outboxes for committed events, unique command IDs and deduplicating consumers. A timed-out price request must be retried or reconciled before continuing. The quote transaction checks response validity and expiry. Where inventory reservation or a binding price hold is needed, specify a reservation/expiry contract before promising it; these capabilities are not assumed in the pilot. [S7]

The AI service may propose an exchange package or request a reviewed design change. It cannot approve pricing, send a customer proposal, place an order or write another service's tables. Manual service workflows remain available when AI is unavailable.

## Solution options by business service

Select solutions independently against a common acceptance contract. “Open source” below distinguishes an existing product from a library used to build a custom service. License, integration rights and support must be checked for the selected deployment; the paid candidates are not procurement commitments. [S3-S9, S11-S15, S18]

| Service | Open-source path | Paid path and recommendation |
| --- | --- | --- |
| Marketplace | Custom catalog application using PostgreSQL and a web UI. More engineering, full control of eligibility and selection workflow. | Evaluate the incumbent supplier catalog capabilities after rights discovery. Recommend a thin custom marketplace over shared catalog APIs initially; no suitable paid marketplace has yet been established. |
| Floor Plan | Custom service using Konva for placement and geometry. It provides a canvas, not validated RF propagation. | Hamina candidate for specialist planning. Prefer proof of fit before building RF capability. API/export, SSO and licensing remain unverified. |
| Discovery | NetBox plus approved inventory imports as a service foundation. NetBox alone does not perform active discovery. | runZero candidate for discovery. Prefer licensed discovery if device coverage and export rights fit; retain import-based assessment as fallback. |
| AI Solution Builder | Custom service with vLLM serving and pgvector retrieval. Model weights have separate license/resource requirements. | Managed model via Amazon Bedrock plus owned orchestration. Recommended initial route if residency and data terms fit. |
| Multi-Site Designer | Custom independent app and API for reusable profiles, overrides and expansion. Own domain-specific behavior. | Evaluate extension of selected planning/CPQ vendor only if multisite semantics and standalone access fit. Recommend custom until that proof exists. |

### Vendor acceptance contract

Test native standalone access, identity/SSO, tenant isolation, product ID mapping, versioned export/import or API handoff, supported file formats, error recovery and data export on exit. A vendor can integrate initially through a reviewed file exchange if API embedding is unavailable. Record the manual cost and residual scope explicitly.

Different solutions need not use the same language or database. They must agree on identifiers, commercial authority and package contracts. Avoid vendor selection based only on screen resemblance to the strategy mockups.

## Shared platform and commercial options

| Capability | Open source or custom | Paid option and recommendation |
| --- | --- | --- |
| CRM | Do not introduce a replacement CRM as part of this plan. | Retain existing HubSpot and fund the adapter, mapping and operational ownership. |
| Product and pricing | Custom PostgreSQL catalog/pricing service; ERPNext pricing features are an alternative after isolation and fit tests. | Evaluate existing HubSpot product/CPQ capabilities or an incumbent ERP/PIM. Choose field masters before adding another commercial source. |
| Quote and proposal | Custom independent quote service for technical validation and snapshot control; ERPNext as a candidate engine. | Evaluate HubSpot CPQ first because HubSpot is established. Confirm tier, API automation, approval, NRC/MRC and external partner needs. No Salesforce migration is proposed. |
| Identity | Keycloak provides control but requires operations and recovery ownership. | Integrate with the existing ngenious SSO capability first, subject to owner acceptance. Keycloak/Auth0 are alternatives for a capability gap review, not parallel identity platforms selected by Partner-Portal. |
| Hosting and data | Self-managed containers, PostgreSQL and RabbitMQ offer control at higher operating effort. | Managed containers, PostgreSQL and queue are recommended. AWS is illustrative, not selected. |
| Reporting | Apache Superset with an isolated tenant-filtered projection. | Power BI Embedded if existing skills/licensing fit. Prove external-user isolation and exports. |
| Workflow and telemetry | Service outboxes and OpenTelemetry. Temporal only for demonstrated orchestration complexity. | Managed queue and approved telemetry service. Temporal Cloud remains optional. |

### One quote authority

HubSpot documents commercial quoting, pricing and approval capabilities, but current packaging and access vary. The account's entitlement and technical multisite fit are unverified. If HubSpot CPQ is selected, it becomes the quote authority behind the adapter; technical validation and solution exchange can remain separate services. Otherwise, the independent quote service owns issued totals and sends summaries to HubSpot. Never maintain two authoritative quote calculations. [S18]

Evaluate total cost using subscriptions, partner seats, API rights, model usage, cloud resources, implementation, data stewardship and support. Compare the same availability and recovery requirements. No vendor price or commercial entitlement is assumed.

## Security and service operations

Use common identity and entitlement policy across the portal and independent services. Each service still authenticates requests and authorizes actor, tenant and resource. A portal login is not a blanket authorization to every vendor or customer record. Use service-to-service identity with narrow scopes and separate credentials for each integration.

| Area | Required control | Acceptance evidence |
| --- | --- | --- |
| Tenant and CRM access | Bind partner grants to permitted CRM records. Apply authorization to direct service access as well as portal access. | Two-tenant tests for APIs, URLs, jobs, files, quote exports, retrieval and BI. |
| Data stores | Service-owned schema/database roles. PostgreSQL RLS where suitable, non-owner runtime roles and safe pooled tenant context. | Cross-tenant reads/writes denied; schema migration does not require other service releases. |
| Files and collectors | Quarantine and restricted parsing. Discovery requires authorized network scope, local secret handling and a stop control. | Malicious-file fixtures rejected; collector cannot scan outside agreed scope. |
| AI | Entitlement-filtered retrieval, typed tools, human-reviewed changes, tenant budgets and cancellation. | Grounding evaluation plus malicious-source and cross-tenant test cases. |
| Events and integration | Durable inbox/outbox, retry limits, idempotency, reconciliation and trace IDs across handoffs. | Repeat and reorder events, simulate timeout after commit and prove no duplicate quote or CRM record. |
| Recovery and lifecycle | Backups, restore exercises, schema compatibility windows, versioned packages and operator runbooks. | Restore each authoritative store and reconcile dependent projections. |

### Proposed operational targets

P0 must confirm a load scenario. Initial planning fixture: 10 partner tenants, 100 named users, 25 concurrent users, 60 sites and 5,000 expanded BOM lines per quote, with 10,000 eligible offers. Target 99.9% monthly portal and critical shared API availability, local API reads p95 under 500 ms, local quote evaluation under 5 s and a 20-page proposal within 60 s including queue wait. External vendor latency is reported separately.

Propose RPO 15 minutes, RTO 4 hours and CRM/report projection freshness within 15 minutes under normal operation. These are targets for testing, not promises about HubSpot or purchased tools. Measure complete user journeys as well as individual services, since shared dependencies affect end-to-end reliability.

## Phased delivery and acceptance gates

Independent service boundaries apply from the first delivery. Phasing determines when a service becomes available, not whether it is independent. P0 selects candidate products and confirms integration rights before building replacements. The previous 8-10 / 18-24-week estimate is superseded by the provisional ranges below.

| Phase | Range | Outcome | Exit gate |
| --- | --- | --- | --- |
| P0 | 2-3 weeks | HubSpot mapping, product/quote authority, five service contracts, solution fit and pilot scope. | Named owners accept contracts, governed samples and revised funding estimate. |
| P1 | Next 6-8 weeks | Portal shell, Marketplace, shared product/pricing, exchange, quote path and HubSpot integration. | Marketplace works standalone and through portal; exact approved quote reconciles to HubSpot. |
| P2 | Next 6-8 weeks | Independent Floor Plan, Discovery, AI and Multi-Site thin workflows with common package handoff. | Each service works standalone and through portal; own deployment and failure tests pass. |
| P3 | Next 4-6 weeks | Selected specialist integrations, lifecycle/reporting, hardening and operational readiness. | Vendor evidence, restore/security tests and accepted release scope. |
| Later | Not scheduled | Billing, ordering, additional countries, deeper RF automation and additional integration scope. | Separate business case and refined backlog. |

### Planning envelope

The revised pilot range is week 8-11. Broader integrated capability is provisionally week 18-25 from kickoff. P2 delivers thin but independent services; specialist accuracy, universal device coverage, all vendor workflows and unsupported APIs are not implied by that range. If a vendor cannot meet the contract, the corresponding scope must be re-estimated or explicitly deferred.

Assume 8 FTE: five engineers including the lead, one quality engineer, one platform/security engineer, half-time product and half-time design. This yields 144-200 FTE-weeks across 18-25 weeks. Catalog, commercial and HubSpot administration stewards and specialist reviews are additional availability requirements. No staffing or monetary budget has been approved.

The revised 50-item backlog is a seed of focused 2-3-day outcomes. It does not account for every production feature or the full staffing envelope. Vendor fit tests produce more small implementation tasks before commitments expand. Service teams may work concurrently once their contract and foundation dependencies are accepted.

## Assumptions and decisions

| ID and decision | Proposed position or uncertainty | Owner and timing |
| --- | --- | --- |
| D01 Product and price master | One logical authority. Evaluate existing sources and HubSpot product model; physical data location unconfirmed. | Catalog / Commercial, P0 |
| D02 Quote authority | Compare HubSpot CPQ with independent custom/OSS quote engine using the same golden cases. Choose one. | Commercial / CTO, P0 |
| D03 HubSpot account model | HubSpot CRM is confirmed. Account count, tier, app model, scopes, objects and partner permissions remain unknown. | CRM administrator, P0 |
| D04 Field ownership and sync | Propose CRM ownership of company/contact/deal and explicit outbound quote fields. Agree conflict and outage policy. | CRM admin / Product, P0 |
| D05 Identity and residency | Request the existing SSO contract and owner acceptance. Confirm cloud, data regions, retention and per-solution isolation. No shared customer data plane is approved. | Security / CTO, P0 |
| D06 Independent solution selection | Marketplace, Floor Plan, Discovery, AI and Multi-Site each need native access and a supported handoff contract. | Solutions lead, P0 then P2 gates |
| D07 Pilot and commercial policy | One country/currency, two partners, narrow catalog. Confirm NRC/MRC, approval, expiry and catalog rights. | Product / Commercial, P0 |
| D08 Capacity and funding | 8 FTE and 18-25 weeks are new planning assumptions. Procurement and vendor findings may change them. | CTO / Delivery, P0 gate |

### Material risks

Independent solutions may have incompatible SSO, product models, export fidelity or API rights. Mitigate with early acceptance contracts and file-based fallback where acceptable. Shared pricing is a critical dependency; use versioned snapshots and clear expiry policy. HubSpot synchronization can drift; field ownership, command ledgers and reconciliation are required. Service autonomy adds operating cost; budget platform ownership and contract tests from P1.

The PDF establishes desired workflows, not measured scale, validated RF coverage or current supplier integrations. User clarification establishes service independence and HubSpot usage. Other architecture choices are recommendations. This planning work did not inspect or change the live HubSpot account and does not establish licensed capabilities.

## Sources and evidence

S1 and S2 establish requirements. S3-S16 were researched for the initial proposal on 5 October 2026. S17-S18 were checked on 6 October 2026. Product selection and commercial terms require a fresh proof of fit at P0. Page references are physical PDF pages. Mockup metrics are illustrative.

### S1  Platform_Strategy_Updated.pdf

User-confirmed source, 24 pages, created 2 October 2026. SHA-256 fe6fd6bd2b90f74c245376e4a901cc1f9e02a7ec4430beb698ae488e6ab830d9. Page numbers in this proposal refer to physical PDF pages.

### S2  Authoritative task brief and architecture clarification

User brief of 5 October and clarification of 6 October 2026. Independent entry points mean independent services with potentially different solutions. The portal integrates them. HubSpot is the existing CRM. Shared product and pricing data are allowed. This revision supersedes the earlier modular-core proposal.

### S3  Keycloak administration and project

https://www.keycloak.org/docs/latest/server_admin/
https://github.com/keycloak/keycloak

### S4  Auth0 Organizations and pricing

https://auth0.com/docs/manage-users/organizations/create-first-organization
https://auth0.com/pricing

### S5  PostgreSQL row security and license

https://www.postgresql.org/docs/current/ddl-rowsecurity.html
https://www.postgresql.org/about/licence/

### S6  Managed PostgreSQL and containers

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html

## Sources and evidence continued

### S7  Reliable messaging and outbox

https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/standard-queues-at-least-once-delivery.html
https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/transactional-outbox.html
https://www.rabbitmq.com/docs/quorum-queues

### S8  Temporal workflow options

https://docs.temporal.io/temporal
https://docs.temporal.io/cloud
https://github.com/temporalio/temporal

### S9  ERPNext quoting and pricing

https://docs.frappe.io/erpnext/quotation
https://docs.frappe.io/erpnext/pricing-rule
https://github.com/frappe/erpnext

### S11  AI serving and retrieval

https://docs.vllm.ai/en/latest/
https://github.com/vllm-project/vllm
https://github.com/pgvector/pgvector

### S12  Amazon Bedrock

https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html
https://docs.aws.amazon.com/bedrock/latest/userguide/data-protection.html

### S13  Floor-plan options

https://konvajs.org/
https://github.com/konvajs/konva/blob/master/LICENSE
https://docs.hamina.com/hamina

## Sources and evidence continued

### S14  Discovery and inventory options

https://netboxlabs.com/docs/netbox/
https://github.com/netbox-community/netbox
https://www.runzero.com/platform/
https://nmap.org/book/man-legal.html

### S15  Business intelligence options

https://github.com/apache/superset
https://learn.microsoft.com/en-us/power-bi/developer/embedded/embedded-row-level-security
https://learn.microsoft.com/en-us/power-bi/guidance/powerbi-implementation-planning-usage-scenario-embed-for-your-customers

### S16  Telemetry standards and metrics

https://opentelemetry.io/docs/what-is-opentelemetry/
https://prometheus.io/docs/introduction/overview/

### S17  HubSpot CRM and integration documentation

https://developers.hubspot.com/docs/reference/api/overview
https://developers.hubspot.com/blog/a-developers-guide-to-hubspot-crm-objects-deals-object
https://developers.hubspot.com/docs/apps/developer-platform/add-features/configure-webhooks

### S18  HubSpot commercial capabilities

https://knowledge.hubspot.com/cpq/getting-started-with-hubspot-cpq
https://knowledge.hubspot.com/products/create-and-manage-products
https://legal.hubspot.com/hubspot-product-and-services-catalog
