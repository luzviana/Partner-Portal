# First exposure, delivery and operations gates

**Scope revision:** [Latest reviewed priority plan](priority-plan.md) supersedes earlier five-service and P0–P3 sequencing. HubSpot integration is Priority 1, proposal-only Marketplace Priority 2, cross-page AI Sales Support Priority 3. Site Designer/multisite and Discovery are Priority 4, not initialized. The controls below remain applicable to relevant capabilities, not authority to launch deferred work.
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

## Gate attachment to current first use

| Priority / items | Operating owner | Gate |
| --- | --- | --- |
| 1 R02/R03/R06/R08-R11/R16/R17/R51-R55 | CRM adapter, portal, SSO and content owners | Account/field/grant/metric/file contracts and SYN/REAL controls before any real Home/Opportunities/Resources exposure |
| 2 R04/R05/R07/R12-R15/R18-R26/R56/R57 | Commercial, catalog, proposal/adapter operator | Priority 1 accepted for delivery; candidate rights and full HubSpot price/BOM persistence, 30-day validity, no checkout, native edit and recovery proof |
| 3 R34-R39/R58-R60 | AI owner, application operators, content owner | Priority 2 accepted for delivery; model terms, governed tools and cross-page context/revocation/evaluation; mandatory agent release acceptance |
| 4 R27-R33/R40-R42 | Future Site Designer/Discovery owners | Deferred, no initialization. Explicit reactivation after priorities 1–3 and then capability-specific rights, scan/file/restore gates |
| Later R44-R50 | Data/Platform/Delivery owners | Separate expanded reporting/exit/operations scope; no deferred item introduces initial launch controls retroactively |

Home/customer composition moves from late R43 into Priority 1 R51/R52. R43 is superseded, not a second implementation task. R38/R39 now accept active portal and AI context, not five independent applications. Initial release completion requires R60. Every first-use item includes CON and SYN/REAL evidence appropriate to its scope. No numerical objective or owner acceptance is fabricated.

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

R54 accepts the HubSpot integration increment, R26 the Marketplace proposal increment, and R60 the initial release including mandatory AI; R48 reconciles actual supported scope and cost. A thin slice cannot be sold as complete strategy coverage. [Source coverage](source-evidence.md) names excluded capabilities and the decision to revisit them.
