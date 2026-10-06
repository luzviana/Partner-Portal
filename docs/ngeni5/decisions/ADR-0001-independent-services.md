# ADR-0001 Revised portal and capability model

Status: **Proposed architecture; latest user scope confirmed.** This record supersedes the earlier mandatory five-independent-service topology. No implementation, merger, vendor selection or deployment approval.

## Current requirement

Home, Opportunities, Marketplace and Resources form the initial portal navigation. AI Sales Support is a mandatory agent on every page with no menu item. Site Designer absorbs Floor Plan and multisite concepts. Discovery covers all observable items in authorized networks. Site Designer and Discovery are Priority 4 and must not be initialized now.

## Proposed boundaries

Portal presentation and server-side HubSpot adapter serve scoped source data. Marketplace owns product selection, while Opportunities contains proposal/price/BOM workflow. Agent tools and context have explicit authorization and operational boundaries without requiring a separate standalone product. Assess modules versus services against ownership/isolation/operations, not menu labels. Existing SSO remains authentication provider and applications own grants.

## Evidence and gates

[Priority plan](../priority-plan.md), [boundaries](../service-boundaries.md) and R01/R02/R03/R51-R60 define current work. EA must re-review changed boundaries at the exact revised commit. Existing isolation/lifecycle/contract controls continue to apply. Coordinator routes review; user and applicable owners/Security must approve consequential work before implementation. Old five-service acceptance tests and independent AI/multisite menu requirements no longer apply.
