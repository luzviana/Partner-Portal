# Authority, placement and lifecycle design

**Scope revision:** [Latest reviewed priority plan](priority-plan.md) supersedes earlier five-service and P0–P3 sequencing. HubSpot integration is Priority 1, proposal-only Marketplace Priority 2, cross-page AI Sales Support Priority 3. Site Designer/multisite and Discovery are Priority 4, not initialized. The controls below remain applicable to relevant capabilities, not authority to launch deferred work.
Author revision 1; proposed design for PP-EA-01/03/10. No approved topology, retention policy or executed isolation evidence is asserted. Accountable roles below are proposed assignments; named acceptance remains a gate in [open decisions](decisions/open-decisions.md).

## Authority model

| Identifier | Cardinality and authority | What it does not authorize |
| --- | --- | --- |
| partner_id | Registered partner organization; one partner may serve many customers; a customer may work with several partners | No implicit access to every customer of that partner |
| customer_id | Stable end-customer identifier, assigned by agreed CRM mapping authority; one customer has many solutions | Company-name match or HubSpot association alone does not grant access |
| solution_id | Exactly one protected customer solution; bound to one customer; contains approved collaborating partners/users | No automatic access to another solution for the same customer |
| environment_id | Exactly one solution plus environment purpose; immutable deployment binding from trusted configuration | A request parameter cannot switch an executing workload to another environment |
| workspace_id | Namespaced by owning service; exactly one solution/environment; many workspaces may support that solution | Not interchangeable with partner, customer or CRM ID |
| CRM reference | Tuple of HubSpot account ID, object type and record ID; mapping registry relates references to customer/solution | Neither a deal ID nor a valid CRM token grants application resource access |
| grant_id | Service-local subject/group, action, resource scope, solution/environment, validity and revocation version | No transitive partner-to-customer access; no portal-wide grant token |

The solution owner authorizes collaboration; each application's delegated administrator administers that application's grants within that boundary. CRM adapter owner administers CRM projection grants under CRM administrator-approved policy. Named administrators and cross-partner collaboration policy are unselected OD-01/04/05 gates. SSO authenticates identity, not business permissions. A user may hold distinct grants in several solutions; each request validates issuer, audience, subject, organization, time, local membership and the specific action/resource grant.

Before a customer is confirmed, an assessment receives a dedicated provisional solution scope, never a shared unclassified workspace. It contains synthetic data only until Product and Security approve real-data classification and accountable ownership. Binding to a customer or copying between solutions requires an explicit reviewed transfer, source and destination authorization, provenance and audit; changing a URL or CRM association cannot reparent protected state.

## Proposed placement matrix

Recommend corporate navigation/public catalog with isolated customer-solution execution and state. OD-01 must select and document the actual pattern before R09 or sensitive SaaS import. This is a recommendation, not an exception approval. A multi-customer SaaS alternative needs evidence of recovery, support, residency and failure boundaries plus applicable EA/Security exception approval; vendor organization IDs, schemas and RLS alone are insufficient.

| State | Default placement / accountable role | Access, restore and sharing rule |
| --- | --- | --- |
| Public technical products | Scoped corporate catalog; Catalog steward | Published versions through API/export; no customer linkage or negotiated prices in public indexes |
| Eligible offers/prices/costs | Commercial authority, partitioned by approved commercial scope; Commercial | Explicit partner/customer grants; costs restricted to internal roles; OD-02 classifies every field before shared storage |
| Designs, observations, sites, packages, quotes | Owner service in solution/environment-isolated store; service owner | No consumer SQL; dedicated recovery/failure boundary; source references cross services only through authorized contracts |
| Files and rendered proposals | Solution/environment-scoped object storage and quarantine; service owner | Short-lived authorized downloads; no public vendor report links; quarantine jobs cannot traverse scopes |
| Search and AI indexes/context | Same protected solution scope; AI/content owner | Entitlement-filtered ingest and retrieval; no shared customer vector cache; delete derived snippets on source revocation |
| Queues, dead letters and replay | Solution/environment scope; provider operator | Scoped worker identity, payload minimization and expiry; replay reauthorizes against current policy |
| Caches and exports | Scoped by solution/environment/grant version; provider owner | Recheck authorization at read/download; expired authority fails closed; exports have independent expiry |
| Secrets and encryption keys | Solution/environment-scoped credentials/key access; Platform | Rotation and service-specific least privilege; support cannot use global data-plane credentials |
| Logs/audit/telemetry | Minimized operational envelope; detailed payload remains solution-local; Security/Platform | Redaction, scoped query grants, approved retention; no cross-customer topology or prompt pool |
| Backups | Isolated recoverable solution state/key scope; Platform plus data owner | Restore to quarantined exact scope, reapply deletion/revocation ledger before access, test no cross-solution recovery contamination |
| Support access | Time-bounded, approved exact solution/environment/session; support owner | Attributed elevation with reason and expiry; deny default access; audit exports and teardown privileges |

## Required negative-case matrix

Every resource family above must be covered, not merely the visible UI. R01/R03 define fixtures, R05 contracts, R06 policy, R11 initial proof; R15/R25/R26 and each service first-use repeat relevant cases.

| Axis | Denial case | Restore/support/lifecycle variant |
| --- | --- | --- |
| Different partners | Partner A guesses B's workspace, object URL, package, price, job or search ID | A cannot restore B's backup, replay B's dead letter or request support elevation into B's scope |
| Same partner, different customers/solutions | User serving customer X has no grant for Y; common partner membership does not permit access | X restore cannot bring Y data/keys/indexes into scope; deleting X does not delete or expose Y |
| Same customer, different grants | Viewer cannot edit/approve/export restricted fields; collaborator on solution X cannot enter solution Y | Revoked editor remains denied via old links, queued jobs, cached AI/BI results and restored snapshots |

Also test authenticated user without local membership, wrong audience/environment, forged CRM mapping, support user without active elevation and revoked grant during a job. Positive collaboration cases require explicit scoped grants and must not loosen these negative cases.

## Record-class lifecycle register

`T_revoke`, `T_cache`, `T_export`, `T_source`, `T_audit`, `T_backup` are maximum intervals selected per record class by the policy owner below, with region and legal-hold treatment. They are **unset**, not infinite defaults. No real-data ingestion/use is permitted until R03/R05 record actual values, policy version and named acceptance. Technical proof in the affected first-use item must meet those bounds. Backup retention cannot silently extend ordinary access.

| Class / authoritative role | Allowed consumers and region | Trigger and active-state treatment | Immutable residue / backup and export treatment |
| --- | --- | --- | --- |
| Identity and local grants / SSO owner for identity, application owner for grants | App-specific identity claims; SSO-approved region; CRM adapter gets only required claims | Revocation disables new actions immediately at authoritative checks; session/job/cache propagation must meet selected T_revoke; stale protected authority fails closed | Minimal security audit only under T_audit; restored grants reconciled before opening access; no revival of revoked users |
| Public product specifications / Catalog steward | Approved publication channels/regions; consumers track revision | Withdrawal tombstones source; invalidate search/export at selected publication bound | Historic non-sensitive version may remain per policy; distribution rights can require removal; bound backups T_backup |
| Partner prices, costs, customer terms / Commercial with privacy policy owner | Eligible commercial consumers, approved region only | Offer/grant expiry denies new use; price caches expire by earlier of T_cache or price validity; reprice before approval/issue | Preserve lawful quote evidence only in restricted archive; commercial export expires T_export; no protected price from stale cache |
| CRM projections and mappings / CRM administrator | Scoped adapter/services with explicit record grants; account/residency gate | Source deletion, grant removal or association change invalidates projection/jobs within T_revoke; minimize contact fields | Keep minimal reconciliation audit under T_audit; backups expire T_backup; restore reapplies tombstones |
| Source designs, files, discovery observations / solution data owner | Authorized service collaborators in selected solution region | Project closure, source deletion or expired assessment policy starts T_source purge; revoke download/job rights within T_revoke | Delete derived indexes/previews; evidence needed by a retained quote becomes separately governed minimized snapshot, not unlimited source retention |
| Packages, quote revisions and approvals / Commercial plus solution data owner | Authorized validators, approvers, renderer; restricted archive by selected region | Business immutability prevents silent edits, not lawful deletion. Tombstone availability; redact separable personal payload or cryptographically erase it where policy requires | Preserve non-sensitive digest, version and audit reason only if allowed; legal hold restricts access and expiry with explicit owner/release review; superseding redaction event documents lost replay ability |
| AI content, conversations, retrieval cache / AI and source-content owners | Solution-local retrieval; exact model/region/provider processing terms gated | Source/grant withdrawal invalidates chunks, caches and queued tools within T_revoke; conversation policy selects T_source | Minimized evaluation evidence only; provider logs/backups/deletion limits must fit policy or candidate is excluded |
| Reporting, downloads, job/dead-letter payload / source owner plus reporting operator | Approved minimized projections and formats; scoped region and recipients | Reauthorize queued work and download; expiry T_export; dead-letter TTL and cache bound explicitly selected | Previously downloaded authorized copies cannot be recalled. Minimize, label recipient/classification/expiry, record export and contractual deletion duty; exclude a route if unavoidable copies violate policy |
| Audit and recovery copies / Security with Platform/data owner | Incident/legal custodians only in approved region | Retain minimal attributable events T_audit; backup expire T_backup; holds separately approved | No passwords, tokens, full prompts or customer topology in common logs; restore quarantine and tombstone replay required before release |

R15/R20 implement immutable-record policy only after selection, R34 source revocation, R44/R45 projection/export policy, R46 exit/deletion fidelity and R47 cross-service regression. Those are future execution gates, not results. An unknown region, duration, vendor deletion limit or legal-hold decision blocks the affected data class rather than inventing a default.

## Discovery and lifecycle ownership

Discovery stores time-stamped observations and reviewed dispositions, not authoritative live inventory. KEEP/REUSE requires human technical evidence; discovery alone cannot establish suitability. NetBox is optional only if an intended inventory authority is explicitly selected in OD-10 and reconciled with iTop. Existing iTop remains the enterprise detailed CMDB/ITSM foundation within its approved boundaries; this proposal neither replaces it nor implements integration. Customer 360 and reporting use source-owned links and approved minimized summaries, not a central replica of detailed topology, tickets or monitoring policy. Any later iTop work must assess its versioned ticket contract and owner-led ICR; none is needed for the quote pilot.
