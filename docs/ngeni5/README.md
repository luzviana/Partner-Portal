# NGENI-5 architecture review package

**Draft 3. Documentation only. EA review pending. User approval pending. No implementation authority.**

The portal integrates five independent services, potentially supplied by different solutions. HubSpot is the existing CRM. Shared product/pricing data are a candidate capability with a scoped authority and isolation decision, not permission to centralize customer data.

## Review order

1. [EA review request](reviews/ea-review-request.md) and [approval status](reviews/status.md)
2. [Source evidence and strategy traceability](source-evidence.md)
3. [Current proposal](proposal.md) and [service boundaries](service-boundaries.md)
4. [EA governance reconciliation](governance-reconciliation.md)
5. [Solution analysis and evidence gaps](solution-analysis.md)
6. [API and event contract inventory](contracts.md)
7. [Architecture decision register](decisions/README.md)
8. [Backlog](backlog.md) and [machine-readable records](backlog.json)

## Source of truth

Markdown and JSON in this directory are the reviewable repository sources. The files under `output/ngeni5` are retained revision-2 Word/PowerPoint snapshots previously delivered to the CTO. They predate the EA reconciliation in draft 3 and must not be treated as the latest or approved baseline. After review findings are reconciled, regenerate presentation artifacts from the agreed repository content before requesting user approval.

The strategy PDF is intentionally not published in this public repository. Its verified checksum and authorized reviewer access are recorded in source-evidence.md. User clarification of independent services and HubSpot usage is authoritative.

No application code, runtime dependency, infrastructure deployment or live CRM configuration is introduced by this PR. No PR merge, reviewer silence, automated check or proposed ADR confers implementation approval.
