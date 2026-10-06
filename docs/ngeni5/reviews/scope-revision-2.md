# User scope revision 2 — review handoff

Baseline before change: `491c16a551b85154cb2bd767dcd775bb26fdd58e`. This record incorporates the latest reviewed user list. It is not a completed EA review, accepted exception or implementation approval. Coordinator owns any subsequent EA routing; author sends no external messages.

## Confirmed changes

- HubSpot integration becomes Priority 1. Home aggregates HubSpot partner information, sales, leads, promotions and opportunities, including customers.
- Marketplace is a list of products we sell and a proposal-generation flow, Priority 2. Exactly 30-day proposals persist with price and BOM in HubSpot and belong under Opportunities. Direct checkout/sale/payment is excluded.
- AI Solution Builder becomes mandatory AI Sales Support, Priority 3. Agent present on every active page, no menu item.
- Floor Plan becomes Site Designer and absorbs multisite. Discovery targets all observable network items. Both Priority 4, not initialized.
- Battle cards move into findable HubSpot Resources. Customers and Prices/Quotes cease to be separate destinations.

## Reconciliation and review impact

Proposal, boundaries, contracts, solution comparison, current CTO narrative, source coverage, ADRs and owner gates now reflect this direction. R01-R50 remain traceable but reprioritized; R43 is superseded by R51/R52. R51-R60 add focused Home/Resources/proposal-expiry/agent outcomes. No Priority 4 dependency blocks priorities 1–3. No actual tasks or services initialized.

All twelve prior EA finding IDs retain historical dispositions in author-revision-1.md. Their control concerns continue: customer isolation, local SSO grants, lifecycle, vendor fit, native quote edits, first-use operations, source completeness, exchange form, contracts, inventory authority, CRM uncertainty and estimates. The new surface/boundary changes require fresh exact-commit review; no prior design closure is carried forward as blanket approval.

Re-review especially: HubSpot aggregation and file access, full price/BOM persistence (beyond summary sync), 30-day commercial honoring and expiry, agent context on every page, consolidated Site Designer, and removal of the mandatory five-service/runtime assumption. Resources is now active human functionality, not merely AI indexing.

## Assumptions / unresolved inputs

Catalog and price source unanswered; actual HubSpot subscription/object/quote/file capabilities unverified. Opportunity-to-Deal mapping, source versus embedded rendering, and issuance-based 30-day clock are proposed interpretations. Confirm Home metric/promotions definitions, resource taxonomy/access, commercial approvals/renewals and retention/operator inputs. No account rights, prices, owner acceptance or runtime results invented.

No slide export was regenerated in this scope-prioritization pass. Prior artifacts are explicitly superseded; decision-brief.md contains current CTO content. This avoids presenting a renamed deck as reviewed architecture. Documentation and artifact refresh may proceed under existing drafting authorization, but all consequential work remains gated.

## Documentation checks

Verified R01–R60 unique IDs, existing acyclic dependency references, no direct or transitive Priority 4 prerequisite for priorities 1–3, and Markdown/JSON field and gate consistency. Relative document links resolve and Git whitespace checks pass. Validation concerns planning records only; no API, model, scanner or application tests ran.
