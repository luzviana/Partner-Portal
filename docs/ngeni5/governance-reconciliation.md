# EA governance reconciliation draft

**Scope revision:** [Latest reviewed priority plan](priority-plan.md) supersedes earlier five-service and P0–P3 sequencing. HubSpot integration is Priority 1, proposal-only Marketplace Priority 2, cross-page AI Sales Support Priority 3. Site Designer/multisite and Discovery are Priority 4, not initialized. The controls below remain applicable to relevant capabilities, not authority to launch deferred work.
The table preserves pre-review draft-3 corrections as history, not approvals. Current author revision 1 incorporates EA v2 through the [finding register](reviews/author-revision-1.md), [authority/lifecycle model](authority-and-lifecycle.md) and [first-use gates](release-and-operations.md). These current documents and the rewritten proposal supersede any less-specific earlier wording. No exception or approval is inferred.

| Topic | Revision-2 gap | Draft-3 position | Required EA disposition |
| --- | --- | --- | --- |
| SSO | Generic Keycloak/Auth0 selection could create a parallel identity capability | Existing ngenious SSO is first integration target; product owns authorization | Confirm SSO owner, OIDC/SAML contract, external users, workloads and ICR |
| Isolation | Tenant/schema isolation and common hosting could be read as blanket shared customer state | Declare solution scope; default to isolated customer-solution state | Choose deployment pattern or approve a bounded exception |
| Shared commercial data | Common catalog/pricing not classified by field and consumer | Separate public specs from partner prices, costs and customer-specific terms | Classify and approve eligible sharing, deletion and failure radius |
| Database access | Direct cross-product read exception | Withdrawn; provider API or governed export only | Confirm contract boundary and any narrow exception procedure |
| Exchange/BFF | Independent deployables proposed without reuse evidence | Compare provider module, reusable library/adapter and dedicated service | Require benefit, owner and operating cost before new platform runtime |
| APIs | Operation sketches lacked registration and deployment binding | Inventory exposure, authority binding and compatibility requirements | Reuse existing domain contracts before adding new endpoints |
| Infra/operations | AWS and shared queues implied a baseline | Managed cloud is illustrative; per-solution ingress/secrets/logs/queues follow approved scope | Validate enterprise platform, cost and recovery ownership |
| Cross-repository work | SSO/CRM/platform responsibilities were generic | No edits to SSO, iTop or other product repos; submit structured ICRs for needed changes | Affected owners accept and implement their portions |
| Governance | CTO decisions could look ready for execution | Every ADR proposed; EA review and explicit user approval are independent gates | Record exact reviewed commit, findings and approval scope |

## Candidate isolation patterns to compare

1. Corporate portal and commercial catalog, with independently deployed solution tools and solution-local state.
2. A single Partner-Portal product serving multiple partners, with a specifically approved customer isolation model and narrowly classified shared state.
3. Reusable portal/service software deployed per customer solution, consuming the approved corporate identity capability and eligible catalog exports.

Evaluate common purpose, sensitive data, policy variance, blast radius, lifecycle, administration, residency/retention, operating value, exit and funded ownership. Do not assign an overall score before evidence exists.

## Approval gate

EA review must cite an exact commit. Findings require disposition and re-review when material boundaries change. The user must separately and explicitly approve the consequential decisions and their scope. A documentation-only PR merge is not deployment authority. Security and affected-owner approvals apply as determined by actual risk and EA governance; no unavailable reviewer is silently waived.
