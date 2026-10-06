# Partner Portal enterprise architecture proposal

**Author revision 2: HubSpot-first scope. Planning only; implementation approval pending.** The latest reviewed user list supersedes the five-entry-point model. [Priority plan](priority-plan.md) is the authoritative scope and sequence. Existing EA reports cover earlier commits, not this boundary change.

## User experience and priorities

| Priority | Outcome | Boundary |
| --- | --- | --- |
| 1 | HubSpot integration: Home with partner information, sales, leads, promotions, customers and aggregated opportunities; Resources and Opportunities views | Portal presentation, server-side adapter and application-owned grants; HubSpot remains source |
| 2 | Marketplace listing products we sell and producing a 30-day proposal stored in HubSpot with price and BOM | Thin catalog/selection capability and one proposal authority within Opportunities; no checkout/direct sale |
| 3 | Mandatory AI Sales Support on every portal page | Context-aware agent capability with governed tools; no menu item or standalone AI product |
| 4 | Site Designer and Discovery | Deferred, not initialized. Site Designer includes multisite. Discovery targets all observable items on authorized networks |

Navigation is Home, Opportunities, Marketplace and Resources. Battle cards belong in Resources; customer information belongs in Home; prices/quotes belong in Opportunities. Rename Floor Plan Designer to Site Designer and Network Discovery to Discovery. Keep independent ownership/contracts where useful, but do not equate every screen with a microservice.

## Proposed architecture

Portal UI consumes a server-side integration facade. The facade authorizes application-local grants and calls supported HubSpot APIs. Existing SSO handles authentication; direct login and local authorization principles remain unchanged. Minimal scoped caches/read projections improve aggregation with freshness and explicit outage states. HubSpot owns CRM/source content; no second CRM or file master is proposed. The product/price master still requires confirmation.

Home aggregates only permitted HubSpot records. Account/object/record mappings, partner/customer/solution bindings and metric definitions must precede UI implementation. Resources supplies searchable authorized HubSpot file metadata and controlled downloads, including battle cards. HubSpot account subscription, actual object model and folder/access conventions remain unknown. Detailed integration design is in [priority plan](priority-plan.md) and [contracts](contracts.md).

Marketplace selects canonical products and quantities. Prefer a thin custom experience integrated with existing HubSpot capabilities if account fit passes. Native HubSpot quotes are the first persistence/approval route to assess. A supported alternative must preserve a versioned proposal, structured BOM and prices in HubSpot, not just an external link. See [solution analysis](solution-analysis.md). Medusa is a conditional catalog foundation; broad commerce platforms and independent CPQ are escalation options only after specific fit failures.

The approved issuance workflow binds exact BOM/configuration, rules and price evidence. The 30-day customer validity requirement is fixed; issuance anchor and calendar/timezone semantics require Commercial confirmation. No payment/checkout/order generation, auto-deal-won or automatic customer send. Quote integrity and uncertain CRM outcome controls in [quote/CRM controls](quote-and-crm-controls.md) still apply.

AI Sales Support provides authorized product/resource/CRM assistance and proposes drafts. Server-side typed tools reauthorize each action. The agent cannot approve its own prices or bypass commercial review. Its UI appears on all active portal pages; customer context must not leak across navigation. The agent is mandatory for the initial priorities 1–3 release, but no model/runtime/vendor has been selected.

## Data, deployment and approval

[Authority/lifecycle](authority-and-lifecycle.md) retains explicit partner/customer/solution/environment/grant distinctions, bounded revocation, lawful immutable-record handling and isolated recovery. Consolidating interfaces does not grant shared customer access. [Service boundaries](service-boundaries.md) now distinguishes UI areas, source systems and internal capabilities. A separate exchange microservice is not a prerequisite to HubSpot Home or the simple Marketplace.

[Release/operations gates](release-and-operations.md) still apply before each first exposure. Synthetic and real-data evidence are distinct. Vendor rights/isolation/SSO/export gates apply to the selected current capability; deferred tool proofs must not block Priority 1, and their missing proofs never authorize later use.

[Backlog](backlog.md) keeps R01–R50 traceability, adds R51–R60, reprioritizes active work and explicitly parks Priority 4. All are proposed future actions, not initialized tasks or completed runtime proof. OD-01–OD-10 remain gated with the new scope in [open decisions](decisions/open-decisions.md). Old staffing/calendar totals are superseded pending sizing of active work.

Coordinator owns EA routing of the new exact commit. No prior EA finding is self-closed by this scope change. Explicit user/EA/affected-owner/Security approvals remain prerequisites to consequential implementation. Current CTO narrative is [decision brief](decision-brief.md); all previously exported decks predate this reviewed scope and must not be presented as current.
