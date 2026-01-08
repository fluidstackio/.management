# Q1 2026 OKRs - Executive Summary

## Overview

This document provides a high-level summary of Q1 2026 OKRs across all teams, highlighting key priorities and identifying opportunities for improvement and better cross-team alignment.

**For organization-level OKRs, see [org_level.md](org_level.md)**

**For detailed team-level OKRs, see:**
- [software.md](software.md) - Cluster & Platform Ops, Inference, Mike Ops
- [infra.md](infra.md) - Infra Compute, Networking, DCIM/Networking Tooling, Infrastructure Deployment, Observability Team
- [customer_success.md](customer_success.md) - Customer Engineering
- [procurement.md](procurement.md) - Procurement

---

## Organization-Level Objectives (Summary)

Q1 2026 represents a critical quarter where Fluidstack is transitioning from scrappy execution to scaled, repeatable operations. The organization has 5 key objectives:

1. **Execute Stream/CB3 deployments successfully** - Proving the deployment engine at scale
2. **Build ClusterMAX Platinum foundation** - Industry-leading operational excellence
3. **Validate TPU-based inference business** - New product line with technical + commercial validation
4. **Improve customer experience and supplier quality** - Scalable processes for growth
5. **Build world-class engineering team and culture** - Hiring, retention, learning, AI adoption

See [org_level.md](org_level.md) for complete details on organization-level OKRs and how team OKRs roll up.

---

## Team Health and Hiring

### Hiring Targets

Across all teams, Q1 2026 involves aggressive hiring to support the scale required for Stream/CB3 deployments and new product lines. The organization is targeting 16-18 new hires:

| Team | Hiring Target | Key Roles |
|------|---------------|-----------|
| **Procurement** | +4 | 3x Strategic Sourcing Managers, 1x AP Manager |
| **Infra Compute** | +2 | Infra Compute Engineers contributing to O1/O2 |
| **Networking** | +2 | Deployment Lead, Deployment Engineer, (Stretch: Network Security Engineer) |
| **Software (SRE)** | +4 | SRE with 50/50 timezone balance (west coast/London) |
| **Inference** | +4-6 | 2-3 Kernel Engineers (TPU/JAX/XLA), 2-3 Serving Engineers (k8s scheduling) |
| **Total** | **16-18** | Roles span procurement, infrastructure, and software engineering |

### Hiring Success Criteria

- **Velocity:** 100% of hiring targets met with interview to offer latency <2 weeks
- **Retention:** <10% voluntary attrition across engineering organization
- **Professional development:** 100% of team members complete ≥1 professional development activity (conference, certification, training)
- **AI adoption:** ≥3 custom AI tools/agents built and operational, existing AI tools adopted across workflows

### Hiring Risks

With 16-18 new hires targeted across Q1 and multiple teams citing hiring velocity as a dependency, key risks include:
- **Prioritization:** If hiring is slower than expected, which roles are most critical to Stream/CB3 success?
- **Onboarding capacity:** Multiple teams need new hires productive quickly (e.g., Infra Compute: 2-day prod/dev access, contributing to deployments by Q1 end)
- **Competitive landscape:** TPU/JAX/XLA kernel engineers and SRE talent are highly competitive markets
- **Geographic requirements:** SRE roles need 50/50 west coast/London balance

---

## Critical Cross-Team Dependencies

The following dependencies represent potential bottlenecks for Stream/CB3 execution:

| Dependent Team | Dependency | Blocking Impact |
|----------------|------------|-----------------|
| **Networking** | DCIM/Software: NetBox model completeness, gNMI API access | Blocks config generation, observability |
| **Networking** | ICT: Cabling execution from cutsheets, physical infrastructure readiness | Blocks deployment timeline |
| **Networking** | HW Operations: Room access, power/cooling validation, handover acceptance | Blocks deployment start, handover |
| **Networking** | Recruiting/HR: Deployment Lead, NRE, Enterprise Eng hiring velocity | Blocks team capacity for CB3 |
| **Multiple** | Procurement: IT infrastructure, vendor selection, warehouse logistics | Blocks all physical deployments |
| **Multiple** | DCIM Tooling: Asset tracking, NetBox accuracy | Blocks automated deployments |
| **Multiple** | Recruiting/HR: Hiring velocity across all teams | Blocks team capacity for Q2+ scale |

**Mitigation:** Weekly cross-functional sync for Stream/CB3 deployment teams (Procurement, Infra Compute, Networking, DCIM, Infrastructure Deployment) with dependency tracking dashboard

---

## Outstanding Issues and Recommendations

### 1. **Assign Missing Owners to Critical KRs**

**Issue:** Many critical key results lack assigned owners, creating accountability gaps that could delay execution.

**Examples:**
- Infra Compute O1 (Deploy Sanidine Stream sub-pod): All 4 KRs marked "Owner: TBD"
- Infrastructure Deployment O1 (Deliver v7 POD): All 3 KRs marked "Owner: TBD"
- Cluster & Platform Ops: Majority of KRs across O1-O4 marked "Owner: TBD"
- DCIM O2 KR2.2 (Shipping/ASN automation): Owner: TBD

**Recommendation:** Assign explicit owners to every KR by Feb 1, especially for Stream/CB3 deployment objectives. Consider using RACI framework to clarify accountable vs. responsible parties where multiple people are involved.

**Action Item:** Team leads to assign owners for all "Owner: TBD" KRs by Jan 31.

---

### 2. **Create Cross-Team Dependency Management Plan**

**Issue:** Critical dependencies are identified but there's no clear mitigation strategy if dependencies slip.

**Specific Risks:**
- **Hiring velocity:** 16+ new hires across teams in Q1 is ambitious. What's the prioritization if recruitment is slower than expected?
- **DCIM O2 KR2.2 has "Owner: TBD":** Shipping/ASN automation is foundational but has no owner assigned
- **NetBox completeness:** Multiple teams depend on DCIM achieving 100% NetBox model completeness for Stream/CB3

**Recommendation:**
- Establish weekly cross-functional sync for Stream/CB3 deployment teams with dependency tracking dashboard
- Create hiring prioritization matrix across teams - if you can only hire 8 of 16 planned roles, which are most critical?
- Assign owner to DCIM O2 KR2.2 immediately (Shipping/ASN automation)
- Add intermediate checkpoints for NetBox completeness (e.g., 80% by mid-Feb, 100% by end-Feb) so dependent teams can adjust plans if slippage occurs

**Action Item:** Weekly deployment sync to start by Jan 15 with first dependency review.

---

## Key Strengths

- **Clear organization-level objectives** with explicit roll-up from team OKRs to org OKRs, making priorities transparent
- **Strong focus on Stream/CB3 deployments** with alignment across Procurement, Infra, Networking, DCIM, and Infrastructure Deployment teams
- **Significant investment in automation and tooling** (NetBox, ZTP, asset tracking, NVSentinel, AI tools) to enable future scale
- **Security & compliance foundation** with vulnerability scanning and remediation as highest priority (90%+ Critical CVEs remediated within SLA, NVIDIA embargo program)
- **Team integration demonstrates organizational maturity** - Cluster & Platform Ops integration brings unified ownership; dedicated Observability Team consolidates fragmented initiatives
- **ClusterMAX Platinum foundation** establishes industry-leading operational excellence through automated remediation, comprehensive security, production-grade SSO, and competitive developer experience
- **Strategic inference bet** with clear technical and commercial validation criteria for TPU-based inference product line
- **Team health and culture focus** with explicit OKRs around hiring velocity, retention, professional development, and AI adoption
- **Documented dependencies** provide transparency into cross-team coordination needs

---

## Quarter in Context

Q1 2026 is the proving ground for Fluidstack's transition to scaled operations. Success requires:
- **Tight coordination** across 10+ teams with clear dependency management
- **Aggressive hiring** (16-18 new team members) with <2 week interview-to-offer latency
- **Rapid automation development** to enable 2026+ scale
- **Clear ownership** with all KRs assigned by Feb 1
- **Strong execution** on Stream deployment to validate processes for CB3

The integration of Cluster & Platform Ops and the creation of a unified Observability Team exemplify the organizational maturity being built this quarter - consolidating fragmented initiatives into coherent, scalable architectures with clear ownership.

For complete details on objectives and key results:
- **Organization level:** [org_level.md](org_level.md)
- **Team level:** [software.md](software.md), [infra.md](infra.md), [customer_success.md](customer_success.md), [procurement.md](procurement.md)
