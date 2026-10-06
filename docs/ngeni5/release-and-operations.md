# First exposure, delivery and operations gates

Proposed PP-EA-06/09/12 response. Documentation is the only authorized activity. These checklists describe future evidence; no checklist has passed. No service may infer permission from a dependency passing, an EA agent report, a documentation merge or silence.

## Two different release checklists

**SYN — synthetic development:** Product records fabricated fixtures, no real identities/customer files/CRM data, no production credentials and exact environment/teardown target. Platform assigns an operator, access restriction, secrets/TLS for any network exposure, upload/job/egress limits and kill switch. Security reviews the applicable threat scope. State is either explicitly disposable with owner-approved loss and teardown criteria, or has demonstrated restore. No external account change, scan, procurement or configuration is authorized by this planning document. A development exception needs owner, bounded scope, expiry/exit and approval evidence; it cannot admit real data by convenience.

**REAL — first real identity/data/external-user exposure:** before that exposure, attach all of the following evidence for the exact service/version/environment. R26 is pilot acceptance, not permission to defer these checks until after exposure.

1. Product-approved users, data classes, solution boundaries, purpose, region and retention/revocation/cache/export/backup bounds; OD-01/07 plus affected policy owners.
2. Service owner and Security-approved scoped threat model; SSO provider acceptance/client flow; direct and portal local authorization, grant-revocation bounds and three-axis negative cases from authority-and-lifecycle.md.
3. Platform operator proves TLS, secrets protection/rotation, encryption and key scope, bounded resource use/jobs/queues/egress and exact rollback/teardown; secrets and identity changes remain affected-owner work.
4. Before first file upload: quarantine, type/size/decompression limits, malicious-file checks and isolated parser/render worker. Before any URL/media/AI fetch: allowlisted purpose/destination policy, private/link-local/metadata address denial, redirect/DNS-rebinding defenses, time/size limits and audit; failed containment blocks the feature.
5. Attributable audit with redaction; test no tokens, customer payload or prompts in shared logs. Approved time-bounded support elevation, unauthorized-support denial and incident escalation.
6. Demonstrated restore to isolated quarantine, reference reconciliation, deletion/revocation replay and recovery objectives; destructive restore rehearsals use approved test targets. Real authoritative state is not declared disposable to bypass recovery.
7. Vendor hard gates and first-use contract evidence passed; named service operator, backup operator, business steward and escalation contact accept responsibility. Applicable independent Security/EA/affected-owner approvals and explicit user scope approval are recorded.

Unknown controls, operators or policy values block that service's exposure. Material exceptions require applicable independent approval; none are accepted here. SYN to REAL is a new gate, not a data-file substitution.

## Gate attachment to first use

| First-use items | Accountable operating role (named acceptance pending) | Required before first use |
| --- | --- | --- |
| R09-R11 platform, portal, identity | Platform operator, application owner, SSO owner | OD-01/05/08, SYN or REAL, service registration and access evidence |
| R12-R14 catalog/pricing/Marketplace | Catalog and commercial steward plus Marketplace operator | OD-02/06, protected-price lifecycle, contract baseline and applicable checklist |
| R15 package capability | Selected package provider operator | OD-09, record lifecycle, schema/compatibility and restore proofs |
| R16-R18 CRM | CRM adapter operator and CRM administrator | OD-04, scoped account grants, reconciliation limits and applicable checklist |
| R19-R24 quote/render | Quote operator, Commercial and technical validator | OD-03/07, native bypass proof, expiry guards, file controls and checklist |
| R26 initial pilot exit | Product accepts scope; Platform/Security attest evidence | All prior applicable checklists already passed, integrated restore/journey evidence and unresolved exclusions visible |
| R27-R28 Floor Plan | Planning operator / Solutions | Reconfirmed vendor rights/fidelity, upload/egress and isolated plan recovery |
| R29-R30 Discovery import | Discovery operator / customer scope owner | Import only; observation lifecycle, malicious-file containment and no scanning |
| R31-R33 Multi-Site | Multi-Site operator / solution owner | Isolated staged data, grants, immutable profile expansion and rollback |
| R34-R37 AI | AI operator / content owner / Security | Model terms, retrieval revocation, prompt/tool abuse evaluation, fetching controls, costs and cancel/disable |
| R38-R39 integrated workflows | Each service operator; Product coordinates | All exposed services' gate records; portal failure and independent rollback |
| R40 specialist extension; R41-R42 active scan | Planning/Discovery operator and Security | New capability-specific rights/scope before use; scanner authorization/kill switch/local secrets before any scan |
| R43-R45 lifecycle/reporting | Source/data owners and reporting operator | OD-10, approved minimized projections, export/download/cache/restore isolation |
| R46-R48 broader readiness | Platform/Security/Delivery and all service owners | Regressions, expanded exit and recovery drills; cannot retroactively approve earlier use |

## First-use contract checklist (CON)

Before a provider is used by its first independent consumer: locate/reuse the provider-owned contract; record schema and example versions, namespaced IDs, server-derived solution/environment binding, auth/exposure class, page/size/rate limits, errors, timeout/retry and idempotency scope, supported-version window, deprecation and rollback. For events include producer ownership, committed-fact meaning, ordering/dedupe, replay, dead-letter TTL and reauthorization. Run positive/negative consumer compatibility against current and previous supported versions (or document initial single-version baseline plus evolution test). Register shallow metadata with EA; operational telemetry uses the EA envelope, not customer domain payloads.

R05 defines the common envelope and review checklist. R12/R13/R15 implement first commercial/package contracts; R16-R18 CRM; R22 events; R28/R33 tool exports; R34/R35 AI content/retrieval; R38 portal; R43/R44/R45 reporting. Each item records provider/consumer signoff and evidence before use. R46 is a broader exit/upgrade exercise, not the first compatibility test.

## Reliability and accountable operations

| Journey / accountable role | SLIs and vendor outage behavior | Recovery evidence |
| --- | --- | --- |
| Direct login / application operator with SSO escalation | Login success/latency and local grant denial correctness; SSO outage reported as journey failure | Client rollback, session revocation and incident contact |
| Browse/price / Marketplace + commercial operator | Authorized browse success, price freshness/expiry; protected pricing fails closed when authority unavailable | Catalog rollback and offer revocation proof |
| Design/package / owning tool + package provider | Submit success, fidelity, queue age; vendor outage visible, supported export fallback only | Source/package restore and idempotent replay |
| Approve/issue / quote operator + Commercial | Valid issue success, approval wait, technical rejection correctness, render latency | Immutable revision restore, native bypass/expiry denial |
| CRM sync / adapter operator | Time to confirmed remote state, uncertainty backlog/age; pending status remains visible | Ledger restore, delayed visibility and operator reconciliation |
| AI / AI operator | Grounded acceptance, unauthorized actions, latency/cost per accepted solution; manual workflows remain available | Disable/model rollback, context revocation and reindex |
| Reports / reporting operator | Freshness, reconciliation error, authorized export success | Source-led replay and revoked export/restore denial |

Include vendor failures in user-journey availability; also report provider attribution separately. Product and Platform set alert thresholds, on-call coverage, escalation and numerical objectives in OD-08. Earlier illustrative 99.9%, 15-minute RPO/freshness, 4-hour RTO and latency targets are unapproved hypotheses, not inherited promises. Do not infer journey reliability from component SLAs.

## Estimate reconciliation

The original 50-item seed was 133 focused person-days, or 26.6 five-day person-weeks. The former 8-FTE × 18–25-week envelope was 144–200 person-weeks (720–1,000 person-days). The 587–867-day gap was **unallocated**, not a validated contingency or additional committed work. Revised acceptance is broader; all retained day values are historical timeboxes pending re-estimation, not assertions that new proof fits unchanged effort.

R08 must produce an owner-backed work breakdown: discovery/procurement/contracting and SSO onboarding; source/catalog stewardship and commercial policy; product/adapter implementation; security/QA and migration; per-service operations/runbooks; launch/support; explicit contingency. Separate one-time engineering, ongoing operations and elapsed vendor/legal lead times. Assign staffing/skills, concurrent constraints, blocked inputs and low/base/high volumes. Vendor proof and integration gaps become small follow-on tasks before work is funded. No current calendar commitment survives this revision; 2–3-week P0 and 18–25-week program ranges are superseded as delivery commitments.

R26 accepts a funded pilot slice and its operators; R48 reconciles actual supported scope and cost. A thin slice cannot be sold as complete strategy coverage. [Source coverage](source-evidence.md) names excluded capabilities and the decision to revisit them.
