# Enterprise Architecture review request

## Review brief

NGENI-5 proposes a Partner Portal integrating independent Marketplace, Floor Plan, Discovery, AI Solution Builder and Multi-Site Designer services. They may use different purchased or custom solutions and consume governed product/pricing data. HubSpot is the existing CRM. The work is planning-only, with no implementation authorization.

Please review the PR and exact commit supplied in the handoff. Confirm access to Platform_Strategy_Updated.pdf using its 24-page count/checksum, and identify the accepted EA baseline reviewed. The repository Markdown/JSON is draft 3; DOCX/PPTX are explicitly retained draft-2 snapshots.

## Requested scope

1. PDF alignment and user clarification: trace capabilities and identify missing/overstated scope.
2. Service boundaries: standalone usability, ownership, vendor versus custom components, necessary shared capabilities, coupling and whether exchange/BFF need dedicated runtimes.
3. Identity/SSO: reuse existing capability, supported flows/claims, external users, workloads, grants, revocation, vendor federation and affected-owner ICRs.
4. Security: threat boundaries, customer-solution isolation, privileged/support access, files, collectors, AI tools, secrets, audit, residency and retention.
5. Data ownership: products/offers/prices, CRM masters, solution state, immutable quote/packages, classification and centralization rationale.
6. APIs/events: existing contract reuse, exposure classification, trusted binding, compatibility, schemas, retries, idempotency, reconciliation and consumer tests.
7. Infrastructure: approved cloud/platform, SaaS boundaries, ingress, stores/queues/indexes, tenant/solution topology, blast radius and cost.
8. Operations: ownership, SLOs, capacity assumptions, observability, backup/restore, failure drills, vendor outages, portability and support cost.
9. Build-versus-buy: deeper primary-source evaluation of real candidates and alternatives, actual edition/API/SSO/export rights, technical fit, TCO drivers and disqualifiers. Do not simply endorse the initial shortlist.

## Requested output

Save a versioned EA review in the EA-owned repository and return its path, commit and review/PR URL. Findings must identify severity, affected repository path or R-item, evidence/source, required change and rationale. Separate blockers, recommendations and open decisions. State explicit disposition such as changes required, conditional recommendation or no blocking findings; do not infer user approval.

For each domain, return preferred and viable alternative candidates with proof status, rejection reasons and open commercial questions. Use solution-analysis.md as a research brief, not an approved shortlist. Cite dated primary sources and mark unsupported capabilities unknown.

After author revisions, re-review the new exact commit and explicitly identify resolved/unresolved findings. Preserve the original review. No application code, merges, deployments, purchases or changes in another repository are authorized. Separate explicit user approval remains mandatory.
