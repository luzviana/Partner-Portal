# Quote integrity and CRM reconciliation

Proposed controls for PP-EA-05/11; no quote platform selected or live workflow tested.

## Technical evidence and transitions

Canonical technical configuration includes canonical product/specification revisions, quantities/units, site/profile revisions, overrides, dependencies, disposition/reuse evidence and technical terms. A deterministic canonicalization specification yields `configuration_digest`; validation evidence binds that digest, rule-set version, validator identity, result and validity interval. A separate commercial evidence digest covers exact line prices, currency, NRC/MRC, taxes, discounts, term, pricebook/policy versions and expiry. Both bind the quote revision. Unknown change classification defaults to technical revalidation.

| State/transition | Authority and guard | Invalidation |
| --- | --- | --- |
| Draft -> TechnicallyValid | Technical validator records passing rules for exact configuration digest and rule version | Item, quantity, required license, site/profile, reuse, technical term or specification/rule change produces a new draft revision |
| TechnicallyValid -> Priced | Sole commercial authority returns valid price evidence for that revision | Expired/revoked offers or price-policy changes require fresh evaluation; no second calculator |
| Priced -> Approved | Authorized commercial approver checks current grants, technical evidence, exact price and expiry | Any commercial edit requires fresh price evidence and approval; technical changes additionally invalidate technical proof |
| Approved -> Issued | Issuing authority checks both digests, current eligibility/grants, evidence expiry and selected CRM-link policy immediately before issue | Expiry while approval/rendering waits blocks issue; queued artifacts cannot bypass final guard |
| Issued -> Revised | Editor creates a new linked revision; prior issued record stays governed by retention/hold policy | Never mutate history to make changed totals appear previously approved |

Price-only changes may reuse technical evidence only when technical digest and rule version are unchanged and still valid. Discounts with technical/contractual implications are not automatically price-only. Commercial and technical owners define classifications before R19-R21. Buyer acceptance, deal-won and order creation are separate states/authorities, excluded from automatic approval synchronization; R49 is later scope.

Native CPQ edits are part of the threat model. Selection must prove a supported workflow preventing native publish/approve of a revision without the matching validation evidence. Webhooks that report an already-issued invalid quote are insufficient. If native issuance cannot be constrained, evaluate a supported controlled issuance path with vendor roles that cannot bypass it; otherwise exclude that route from technical quoting. Unknown capability blocks OD-03, R20/R21 and real issue.

Future R19-R24 acceptance: import a valid 20-AP fixture; remove required switch/license in native CPQ; both native and integrated approval/issue must fail until the new digest passes validation. Test price-only discount, technical term/quantity change, stale rule version, expiry during approval/rendering, revoked grant and competing revisions. R23 output must match exact approved digests and hide internal costs; R24 proves reconciliation without changing totals. Vendor/current API approvals must be demonstrated in the actual entitled account; no headless approval support is assumed.

## CRM uncertain-outcome state machine

HubSpot remains CRM master. R03 assigns one field writer; R16-R18 own a durable ledger keyed by account, object type, local entity/revision and command ID, with remote ID mapping and payload hash. Do not assume a vendor idempotency header or uniquely constrained property exists. R02 must document each supported object's safe lookup/uniqueness mechanism and visibility limits.

| Ledger state | Permitted action / authority | Transition |
| --- | --- | --- |
| Prepared | Adapter records intent atomically before sending; checks mapping, grant and field ownership | Dispatch -> InFlight |
| InFlight | One serialized command attempt per entity/revision | Confirmed response -> Verifying; timeout/disconnect -> Uncertain; clear rejected request -> Failed or bounded retry according to documented semantics |
| Uncertain | No blind create retry. Read known remote ID or search approved durable correlation; use bounded backoff for delayed visibility | Unique matching outcome -> Verifying; ambiguity or elapsed reconciliation bound -> NeedsOperator; absent search alone does not prove failure |
| Verifying | Read canonical remote fields/associations and compare intended revision/hash | Match -> Confirmed; mismatch -> NeedsOperator or explicit safe update under ownership policy |
| NeedsOperator | CRM operator investigates attempts, IDs and associations; records attributable decision | Link confirmed remote result, cancel, or explicitly authorize a new create only after proving no prior outcome; retain audit |
| Confirmed / Cancelled / Failed | Terminal outcome visible to consumers with last checked time | New business intent gets new revision/command; old ledger cannot be erased to force retry |

Product/CRM owner must set maximum attempts, backoff ceiling, total uncertainty deadline, operator response target and escalation in R03 before R18. These are unset owner gates. Rate limits honor provider retry guidance; token revocation suspends dispatch and alerts owner; deletion tombstones mapping rather than triggering recreate. Reordered notifications reread canonical state. Pending sync never claims CRM success, alters a quote or automatically marks a deal won.

R17/R18/R24 future proofs include timeout after remote success with delayed search visibility, duplicate/reordered events, revocation, rate limit, deletion and conflicting remote fields. No duplicate create while uncertain. A CRM outage policy may allow continued design with a timestamped projection, but stale authorization fails closed and issue policy is an OD-07 decision.
