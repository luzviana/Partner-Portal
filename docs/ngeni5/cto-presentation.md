# CTO presentation review draft 3

Prepared from canonical architecture commit `abfaf501324deaefdf3c747b2d085544e37bb21c`. This deck summarizes the author revision responding to EA v2; it does not claim a later EA disposition or approval. All user/EA/affected-owner/Security gates remain in force.

[Editable PowerPoint](../../output/ngeni5/NGENI-5_CTO_Review_rev3.pptx) and [PDF for review](../../output/ngeni5/NGENI-5_CTO_Review_rev3.pdf).

Slides 5–7 compare Marketplace, quote authority and specialist services. Slides 16–18 contain common proof cases, cost inputs and owner decisions. Speaker notes include caveats and pinned source references. Original revision-2 files remain historical. No runtime configuration, external review messages or implementation accompanied this presentation update.

## Slide text

### 1. Partner Portal

Architecture and solution choices

CTO discussion draft

6 October 2026

### 2. Proposed direction

Five independently usable services

Marketplace, Floor Plan, Discovery, AI Solution Builder

and Multi-Site Designer can use different solutions.

A portal that connects their workflows

Governed product and pricing contracts support a common quote.

HubSpot remains the CRM. Existing SSO supplies authentication.

Each application owns access permissions and supports direct entry.

### 3. Independent service boundaries

Service

Owned state

Handoff

Marketplace

Selections and comparisons

Canonical product selection

Floor Plan

Plans, placements and simulations

Versioned design and BOM

Discovery

Observations and assessments

Reviewed reuse/replacement

AI Builder

Conversations and grounded proposals

Human-reviewed changes

Multi-Site

Sites, profiles and overrides

Expanded site BOM

Each service needs native access, its own operating owner and a supported exit.

### 4. Customer and solution protection

Case

Required boundary

One partner, several customers

A customer grant never extends to another customer

One customer, several collaborators

Each application checks the specific action and resource

Detailed solution state

Isolate files, jobs, AI context, credentials and recovery

Shared commercial information

Classify public products, negotiated prices and internal costs

Topology, policy durations and vendor recovery boundaries remain owner decisions.

### 5. Marketplace options

Option

Advantage

Tradeoff / deciding evidence

Thin custom

Precise partner experience

Own catalog tools, permissions and support

Medusa

Reusable commerce foundations

Prove recurring terms, grants and price history

CloudBlue

Channel and subscription scope

Verify purchased scope, rights and integration cost

Compare all three on the same offers, partner prices, revocation and export cases.

### 6. Quote authority options

Option

Advantage

Tradeoff / deciding evidence

HubSpot

Existing CRM relationship

Prove entitlement, approvals and proposal fit

QuoteWerks

Specialist quoting with CRM integration

Prove partner SSO, API rights and edit controls

ERPNext

Broader commercial lifecycle

Justify ERP scope and avoid competing masters

Custom

Exact technical and revision controls

Own commercial correctness and maintenance

Evaluate HubSpot and QuoteWerks first. Keep ERPNext conditional on a wider need.

### 7. Specialist service options

Service

Alternatives

Evaluation direction

Floor Plan

Hamina/incumbent or custom editor

Specialist proof before custom RF

Discovery

runZero, imports or custom scanner

Compare scoped discovery with import pilot

AI Builder

Managed inference or vLLM

Same quality, privacy and cost tests

Multi-Site

Custom or vendor extension

Compare profile and override semantics

Each option must pass rights, SSO, isolation, handoff and operating gates.

### 8. Integration and source ownership

Capability

Proposed contract and responsibility

Product and pricing

One field writer, eligible APIs and governed exports

Package handoff

Versioned source and canonical IDs with scoped receipt

Quote and proposal

One authority owns exact revisions and issued totals

HubSpot adapter

Scoped mappings and a durable reconciliation ledger

Lifecycle and reporting

Minimized projections with source-owned references

Exchange deployment remains open: provider module, adapter or separate service.

### 9. Quote integrity and CRM uncertainty

Exact configuration, exact approval

A native CPQ edit that removes required switching or licensing

must invalidate technical approval before the quote can issue.

A timeout can hide a successful CRM write

Reconcile the existing command and remote result.

Escalate uncertainty without creating a duplicate.

Future release tests include native edits, price expiry and delayed CRM visibility.

### 10. First-use security and operations

Exposure

Evidence before use

Synthetic development

Fabricated data, restricted scope and exact teardown

Real identities or customer data

Accepted grants, data policies and named operators

Files, imports and AI fetching

Quarantine, resource limits and controlled network access

Support and recovery

Attributed access, isolated restore and revoked-grant replay

Each service passes its gate before exposure. Later hardening cannot replace it.

### 11. Phased delivery with evidence gates

Phase

Planned outcome

Exit evidence

P0

Scope, authorities and candidate evaluation

Owners, vendor proof and funded work breakdown

P1

Marketplace, quote and HubSpot pilot

Valid quote, reconciliation and isolated recovery

P2

Independent thin service workflows

Native access and safe package handoffs

P3

Specialist and lifecycle/report extensions

New capability scope, exit and operating proof

Calendar commitments follow re-estimation. Each first-use gate also applies within phases.

### 12. Pilot scope and proposed exclusions

Thin pilot includes

Expansion needs separate scope

Eligible offers and selection

Human battle-card and resource experiences

Calibrated planning and supported handoff

Non-Wi-Fi planning and specialist accuracy

Seed technical rules and quote integrity

GPU, SD-WAN, IoT and additional rule families

Selected lifecycle/report slices

Complete customer lifecycle and report suite

Product and Cleber must accept narrowed scope or fund its expansion.

### 13. Estimate and ownership inputs

133 historical seed person-days

Expanded acceptance needs new task sizing.

The earlier program envelope was a different, unreconciled scope.

A credible plan needs accountable capacity

Include vendor lead times, commercial stewardship, security,

service operations and ongoing support in the funding decision.

No current calendar, budget or numerical reliability commitment.

### 14. EA review and implementation gates

Status

Meaning for this proposal

EA v2: five blockers remained

Isolation, lifecycle, vendors, quote integrity and first use

Author revision supplied

Design and backlog corrections await exact-commit review

SSO ownership resolved in design

Provider acceptance and runtime evidence still pending

Implementation approval pending

Separate user and applicable owner/Security gates

No blocker waiver or accepted exception is recorded in this deck’s source baseline.

### 15. Decisions for the CTO discussion

Accountable people for commercial, data and service ownership

Pilot users, data, countries and included capabilities

Evidence required to select vendors and commercial authorities

Capacity and cost inputs for a funded delivery plan

Implementation waits for EA review and explicit scope approval.

### 16. Appendix: comparable vendor proof

Candidate group

Common deciding demonstration

Marketplace

Same 20 offers, distinct partner prices, revocation and export

Quote authority

NRC/MRC, approvals, 60 sites, expiry and native edit bypass

Planning / Discovery

Known source fixtures, lost fields and authorized scope

AI / Multi-Site

Grounded/revoked-access cases and repeatable profile changes

Evidence labels: documented, demonstrated, contractual, unknown or failed.

### 17. Appendix: three-year ownership cost

Cost component

Inputs still required

Initial work

Implementation, integration, migration and assurance

36 months of operation

Licenses, cloud, support, stewardship and operators

Lifecycle costs

Upgrades, regression proof, export and exit

Low / base / high scenarios

Named seats, assets, API volume, inference and manual labor

No monetary winner can be declared without contractual prices and owner-supplied rates.

### 18. Appendix: pending owner decisions

Decision group

Accountable roles

Before

Isolation and lifecycle

Product, Security, data owners

Topology or real data

Commercial and vendors

Commercial, Catalog, Solutions

Selection or configuration

CRM and SSO

CRM admin, SSO and app owners

Registration / integration

Runtime and package provider

Platform, Delivery, Technical lead

Deployment / package use

Lifecycle / inventory scope

Product, data and affected iTop owner

Expanded persistence / reporting

OD-01–OD-10 retain exact gates. Named acceptance and policy values remain pending.
