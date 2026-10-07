# EA review request — CTO presentation revision 4

Status: prepared for coordinator-owned routing at the commit containing this file. Review pending; no approval claimed. User requested EA review on 7 October 2026. PR: https://github.com/luzviana/Partner-Portal/pull/1.

Review [presentation, transcript and notes](../cto-presentation-rev4.md) alongside [priority plan](../priority-plan.md), [proposal](../proposal.md), [boundaries](../service-boundaries.md), [alternatives](../solution-analysis.md), [contracts](../contracts.md), [backlog](../backlog.md), [JSON](../backlog.json), [ADRs](../decisions/README.md), [source evidence](../source-evidence.md) and [open decisions](../decisions/open-decisions.md). Planning baseline: `5bd91cb04951d541df0df57ff55fb742bdf572f6`. Review the exact new presentation commit supplied by coordinator with git show.

## Requested review

- Alignment with unchanged, confirmed 24-page Platform_Strategy_Updated.pdf and subsequent user scope clarification. Distinguish intentional deferrals from omissions.
- Slides 2–4: HubSpot-first Home aggregation/customers, Opportunities with prices/quotes, findable HubSpot Resources/battle cards; authority and application-local grants.
- Slides 5–7: thin custom/HubSpot versus Medusa and broader commerce; native HubSpot versus supported record/artifact and CPQ escalation. Challenge missing rights, isolation, SSO, export and account-fit proof. Complete structured price/BOM must reside in HubSpot; no direct sales. Review 30-day validity, exact revision authority, edit invalidation, expiry and uncertain CRM commit/reconciliation.
- Slides 8–9: mandatory AI Sales Support on every active page without menu item; tool/context authorization, human-reviewed drafts and initial release acceptance.
- Slide 10: Site Designer absorbs multisite; Discovery targets all observable authorized network items. Both deferred and not initialized; import-only does not satisfy future discovery.
- Slides 11–12 and canonical documentation: service boundaries, identity/SSO, security/isolation, data ownership/lifecycle, APIs/versioning, infrastructure, operations/support/restore, build-versus-buy, dependencies, cost inputs and owner gates.
- Reassess PP-EA-01 through PP-EA-12 against the new scope and prior review evidence. Separate design adequacy from runtime proof; flag overstated selection, closure, estimates or approval.

## Acceptance and unresolved inputs

Return a versioned review with exact reviewed commit, slide/path references, severity, evidence, closure criteria and owner decisions. Distinguish fit for CTO discussion from implementation approval. Coordinator routes to existing EA worker and verifies results; no new workers or direct author-to-EA message.

Missing inputs: HubSpot entitlements/object mapping, product/price source, grants, Home metrics/promotions, Resources privacy/taxonomy, approval and 30-day clock/price-honoring policy, operators/data policy/budget. Do not invent decisions or evidence. User, EA, affected-owner and Security gates remain. No waiver or silent approval; no application/configuration, deployment, merge, procurement, task or credential changes.
