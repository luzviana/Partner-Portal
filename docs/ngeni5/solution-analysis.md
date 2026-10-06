# Solution alternatives and selection evidence

Author revision 1. This comparison incorporates the [EA research](solution-research-evidence.md) at exact commit `5b9fc35daad180e05ee564eb80bbf16eff6124bb`; its cited primary sources were checked by EA on 6 October 2026. Author desk review is not fresh vendor-account verification. No vendor is selected. Actual licenses, prices, rights, account features, region, support and runtime results remain unverified.

## Non-tradeable selection gates

For **each capability and candidate**, R04/R07 must record: authorized partner/customer/solution/environment isolation (including support/restore); approved SSO/direct access and local grants; versioned API or reviewed export/import with fidelity; legal rights for intended users, distribution and embedding where used; field ownership; region/lifecycle/deletion/backup; export/exit; and funded operator. Evidence labels are documented, demonstrated, contractually confirmed, unknown or failed. A documented feature is not proof of an end-to-end gate. Unknown or failed hard gates prevent selection/configuration/use. R08 may exclude the capability with explicit Product scope acceptance and user/EA gates; it cannot call an unknown a pass or substitute an undocumented exception.

Manual import is a separately scoped capability: record fields retained/lost, human mapping/validation, labor per handoff, error recovery, authorized storage and supported outcome. It cannot claim automated round-trip, RF accuracy, active scanning or full technical validation. R40-R42 test expanded capability later; they cannot retroactively authorize R27/R29 or earlier vendor use.

## Candidate evidence and provisional direction

All candidates below are **not selected**. “D” identifies documented research evidence only; all unproven hard gates remain unknown. Accountable roles must obtain named acceptance; no reviewer or vendor has supplied it here.

| Capability / candidate | Evidence and differentiating tradeoff | Unknown hard gates / decision-changing proof | Accountable role |
| --- | --- | --- | --- |
| Marketplace: thin custom | Maximum control over comparison/eligibility; all stewardship/search/support must be built | Complete same 20-offer proof as purchased routes; isolation, recoverability and 3-year staffing cost unknown | Product + Technical lead |
| Marketplace: Medusa | D: product variants and pricing rules; commerce foundation, not complete technical CPQ | NRC/MRC, historic price reproduction, partner costs/grants, edition-specific rights and support/exit need proof | Catalog + Solutions |
| Marketplace: CloudBlue Commerce/Connect | D: Commerce channel/storefront/billing; Connect catalog/API has different scope | Purchased scope/price, portfolio, HubSpot coexistence, SSO, regional partner rights and export; exclude unneeded billing master | Commercial + Solutions |
| Quoting: HubSpot current Quotes | D: qualifying subscription, associations, UI/workflow-centered approval and template constraints | Actual account/API version, native-edit guard, recurring terms, 20-page/site/diagram proposal and cost hiding unknown | CRM admin + Commercial |
| Quoting: QuoteWerks Web | D: HubSpot integration, item/deal mapping, configurable deal completion | API/SSO/partner rights, narrow permissions, native bypass prevention, multisite/NRC/MRC/version export unknown; no automatic deal-won | Commercial + CRM admin |
| Quoting: conditional ERPNext | D: quotations/pricing; GPLv3 code licensing per researched release | Wider ERP need unconfirmed; no competing CRM/product master; recurring terms, grants, audit, extensions and operations proof needed | Commercial + Platform |
| Quoting: custom | Exact technical digest/approval semantics possible; highest correctness/maintenance ownership | No implementation evidence; compare 3-year costs and own all commercial rules, security and exit | Commercial + Technical lead |
| Planning: Hamina | D: OpenIntent import/export; survey data and some switch power/port/geometry fields omitted; named users and controlled report-sharing needed | Partner/SSO/API/embedding rights, identity/data region, isolation/restore and fidelity unknown; missing technical facts require governed enrichment | Solutions + Security |
| Planning: incumbent specialist / custom geometry | Incumbent license/API unknown; custom placement is not RF simulation | No Ekahau integration claim; prove chosen supported handoff. Custom needs file/geometry/exit evidence; specialist accuracy separate | Solutions |
| Discovery: runZero | D: scoped export/API, tier differences, richer JSON than CSV and SAML constraints | SaaS organization does not prove isolated restore/failure; partner federation, account rights, scope and coverage unknown | Discovery owner + Security |
| Discovery: approved importer / optional NetBox | Limited assessment without scanner; D: NetBox is network source of truth, not observation collection | Select observation schema and permitted source files. NetBox only after OD-10/iTop reconciliation; no implicit new master | Discovery + data owner |
| Discovery: custom scanner | Maximum integration responsibility, protocol maintenance and operational risk | Nmap/other distribution rights, authorized targets, secrets and kill switch must pass before scans | Security + Solutions |
| AI: managed inference + owned orchestration | D: managed provider shared responsibility; avoids model-serving operation | Exact model terms/region/logging, prompt retention, isolation, cost and deletion unknown; service still owns tools/grants/evaluation | AI owner + Security |
| AI: vLLM + separately licensed model | D: serving software, API-key protection does not cover every endpoint | Model rights, full endpoint/egress security, GPU cost/on-call and context isolation unknown | AI owner + Platform |
| Multi-Site: thin custom / supported vendor extension | Custom suits versioned profiles/overrides; researched vendors do not establish turnkey fit | Same 60-site diff/repeat/rollback test for both; independent access, contracts and total ownership cost determine choice | Product + Technical lead |
| Runtime: incumbent / Fargate / Container Apps | D: task isolation or revision/jobs/scaling features; commodity managed services possible | Region, networking, separate state recovery, keys, operator and cost unknown. No new Kubernetes or cloud selected | Platform |
| Reporting: owned projection / Power BI / Superset | D: BI identity/security models need separate export/cache verification; Superset configuration not endorsed by research | External rights, scoped service principals, all formats and revocation/backup proof unknown; start with minimized scope | Reporting + Security |

Existing ngenious SSO is consumed, not re-procured. SSO's conditional Keycloak selection and application-local authorization remain in ADR-0004. IdP substitution requires an enterprise capability decision, not a portal-local shortcut.

## Comparable proof cases and decision rule

Marketplace: the same 20 authorized offers, two partners with different prices/grants, revocation, historic quote, human comparison, protected cost, canonical export and restore. Add same-partner/different-customer and same-customer/different-grant cases.

Quote: hardware NRC; service MRC/term; mixed NRC/MRC; partner prices; volume tiers; discount/margin; country/currency/tax; 60-site overrides; expiry/revision; rejected technical dependency and corrected resubmission. Commercial supplies expected answers. Add native 20-AP switch/license removal bypass, delayed CRM visibility, revoked grants and 20-page proposal/template tests. Unknown expected amounts block evaluation; vendor output cannot grade itself.

Planning: representative calibrated multiple-floor plan with APs/wired devices and canonical mappings; enumerate every lost field, accuracy source and manual enrichment. Non-Wi-Fi capabilities remain separately scoped. Discovery: known inventory with unknown devices, scoped targets, local credentials, kill switch, duplicates/reordering/offline recovery and human dispositions; imports do not prove scans. AI: same 50 grounded domain cases plus adversarial/revocation cases, accepted-solution cost and unauthorized-action rate. Multi-Site: 60 sites, 40-profile application, one override, profile diff, repeat, totals, rollback and unchanged historic quote.

After all hard gates pass, propose scoring workflow fit 30%, integration/fidelity 25%, three-year TCO 20%, operating/recovery fit 15%, exit 10%. Product/Commercial must ratify weights. No unknown receives a passing score. Provisional sequence: HubSpot versus QuoteWerks first; Medusa/CloudBlue versus thin custom; Hamina/incumbent specialist before bespoke RF; scoped discovery/import before custom scanning; owned Multi-Site unless a supported extension wins. These are evaluation priorities, not awards.

## Cost and exit model

`3-year TCO = implementation + integration + migration + 36 × (licenses + cloud + support + stewardship + operations) + upgrades + assurance + exit`.

Low/base/high scenarios must use owner-supplied volumes and loaded labor rates. Two pilot partners and ten-partner load scenarios remain unapproved fixtures. Separate internal/external named seats, scanned assets, API quotas, inference, storage/export, support tiers and manual handoff labor. Pin actual release/edition/extensions/model licenses; Medusa enterprise carve-outs, ERPNext GPLv3, NetBox/vLLM Apache-2.0 are research leads, not blanket rights determinations. No monetary winner is calculable yet.

For each candidate obtain export sample and restore/exit procedure, deletion and backup expiry, identity/grant portability, deprecation/version support, data processing/residency, incident support, contractual permitted use and estimated migration labor. If necessary data cannot leave, state the excluded capability or reject selection. R04/R07 produce evidence and follow-on tasks; R08 records owner-backed selection or explicit exclusion before any configuration. Procurement, trials with spend/account changes and real data remain outside current authorization.
