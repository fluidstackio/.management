# Q1 2026 OKRs - Executive Summary

## Overview

This document provides a high-level summary of Q1 2026 OKRs across all teams, highlighting key priorities and identifying opportunities for improvement and better cross-team alignment.

---

## Team Summaries

### Procurement

**Overview:** The Procurement team is focused on executing CB3 and Sanidine site deployments while simultaneously building scalable procurement processes and establishing strategic vendor partnerships for 2026+ growth. This quarter represents a critical transition from ad-hoc procurement to a systematic, scalable operation integrated with Finance.

**Key Priorities:**
- Execute CB3 and Sanidine deployments with complete logistics (warehousing, tooling, labor, IT infrastructure, WAN POPs) and new lab site selection/migration by Mar 31
- Build scalable procurement infrastructure with Zip integration for vendor onboarding (<7 days), PO/invoice tracking, and Atlas procurement integration (<24hr latency)
- Establish 2026 capacity planning and supply chain risk mitigation strategy, identifying constrained equipment (fiber, DRAM) and mitigation plans by Jan 31
- Secure strategic partnerships through sell-through relationships (Dell/SMC, Arista, Commscope/Corning) and off-site integration programs (WWT, Computacenter, Hyve)
- Grow team with 3x strategic sourcing managers and 1x AP manager

### Infra Compute

**Overview:** The Infra Compute team is executing the first Sanidine Stream sub-pod deployment at scale (576 machines) while preparing for CB3's 3-pod deployment. The focus is on proving deployment automation and building team capacity to sustain Q2+ growth.

**Key Priorities:**
- Deploy Sanidine Stream sub-pod with 576 machines provisioned in parallel at <5% failure rate and ≥80% automated remediation
- Achieve CB3 deployment readiness through validated runbooks, 2x capacity load testing, and operational lab environment with v7/CDU/VAST by Mar 31
- Build team capacity with 2 new hires contributing to deployments, 2-day onboarding for prod/dev access, and documented troubleshooting guides

### Networking

**Overview:** The Networking team is delivering the first TPU network at Stream/Sanidine while proving the deployment engine can scale to CB3's 3-pod build. Simultaneously, they're completing critical Q1 designs to unblock procurement and building a reliability foundation through observability and vendor qualification programs.

**Key Priorities:**
- Deploy Stream network successfully with 100% infrastructure validation, corporate network connectivity, and Buffalo POP operational with WAN edge to 365DC
- Achieve CB3 readiness through NetBox automation (100% cutsheets, configs, ZTP >95%), device qualification tools, and validated deployment runbooks
- Complete Q1 network designs for FIS, POPs, corporate datacenters, and Lab 2.0 to unblock procurement for Q1-Q2 builds
- Build reliability foundation with full observability stack (gNMI + Prometheus + Grafana), deployment dashboards, optic qualification program, and alerting/escalation paths
- Staff deployment team with Deployment Lead + 1 Deployment Engineer

### DCIM/Networking Tooling

**Overview:** The DCIM/Networking Tooling team is establishing NetBox as the authoritative source of truth while automating the entire asset lifecycle from shipment to deployment. Their work is foundational for enabling reliable, repeatable deployments and efficient repair operations across the organization.

**Key Priorities:**
- Establish NetBox as source of truth with 100% model completeness for Stream/CB3, cabling/config drift detection, and vendor device traceability within 24 hours of shipment
- Fully automate asset lifecycle with 100% tracking within 24 hours of delivery (zero manual entry), ASN status flowing to NetBox within 4 hours, and zero consumable stockouts
- Enable reliable pod deployment with 100% network configs from NetBox, ZTP >95% success rate, automated cutsheets for ICT, and automatic device qualification
- Streamline repairs with 100% auto-routing to on-call within 5 minutes, support console for ticket creation, and SOPs covering all non-TPU/OCS rack failures

### Infrastructure Deployment

**Overview:** The Infrastructure Deployment team is executing the physical delivery and qualification of the first v7 POD at Stream while establishing the processes, SOPs, and vendor relationships needed for repeatable future deployments. This quarter is about proving execution capability and building institutional knowledge.

**Key Priorities:**
- Deliver and qualify 1 v7 POD at Stream with CDU system L4C commissioned, network infrastructure configured, and machine capacity certified complete
- Develop comprehensive deployment SOPs (FS-authored) for CDU systems, network infrastructure, and SPOCs/OCS with process maps
- Establish infrastructure deployment project management framework with standard workflows, SOPs for each process step, and duration estimates
- Secure pre-execution deliverables: external warehouse procurement, ICT vendor selection/contracting, and CDU vendor selection/contracting for CB3/Stream

### Observability Team

**Overview:** The Observability Team is unifying fragmented monitoring/logging initiatives (Lighthouse, FSH, network observability) into a coherent architecture with clear separation between customer-facing and internal tools. This quarter establishes the foundation for scalable, cost-effective observability that supports both operational excellence and customer self-service across compute and network domains.

**Key Priorities:**
- Establish unified observability architecture with documented reference design clarifying data flow, separation boundaries (FSH for internal ops, Advanced Metrics for customer self-service, network telemetry), integration contracts between compute/network observability, and Lighthouse → Advanced Metrics transition
- Deploy Fluidstack System Health (FSH) on 100% of clusters as standard internal ops tool, reducing operator page volume by 40%, powering automated remediation (NVSentinel integration), and enabling proper alert routing to suppliers/customers
- Enable customer self-service through Advanced Metrics Add-On (Kubernetes Add-On System) with console integration showing basic FSH metrics, opt-in customer Grafana with writable dashboards, and programmatic API access (stretch)
- Optimize cost and scalability by reducing Mimir hosting cost to <$0.025/host/h (33% reduction), evaluating third-party vendors, load-testing for CB3 scale (10k+ nodes, 80k+ GPUs), and completing Stream network observability handover to operations

### Cluster Ops (Software)

**Overview:** The Cluster Ops team is standardizing and accelerating GPU cluster deployments while improving reliability through better health monitoring and alert routing. Working jointly with Customer Engineering, they're establishing supplier quality standards to ensure consistent technical capabilities across all suppliers. The migration to the new ClusterOps stack is critical for supporting the scale required in Q2+.

**Key Priorities:**
- Standardize fast deployments at minimum 1000 GPUs/hr, migrate all clusters to new ClusterOps stack (currently 19% → 100%), and adopt SLURM on k8s as default with zero bare metal deployments
- Improve cluster reliability by reducing page volume through better FS System Health alerting, ensuring FSH availability on all clusters with manageable costs, and automating escalation routing to suppliers/customers
- **(Joint with Customer Engineering)** Establish supplier quality standards through published Technical Requirements document, real-time Supplier Quality Dashboard with automated metrics collection, 100% migration to standardized offerings (managed k8s/SLURM on k8s), and enforcement via deployment tooling
- Contribute to company-wide mono-repo by merging ClusterOps, Atlas, and Lighthouse repos

### Platform Ops (Software)

**Overview:** Platform Ops is elevating the customer experience through architectural improvements (management cluster migration), deploying NVSentinel for automated remediation, building a robust observability stack, and establishing security fundamentals across production infrastructure. The Kubernetes Add-On System represents a strategic shift toward customer-controlled features, while the new security foundation ensures compliance, vulnerability management, and proper access controls.

**Key Priorities:**
- Migrate all K8s clusters to management clusters, removing Fluidstack control-plane components from customer clusters and aggregating region information at hub layer
- Deploy NVSentinel on all K8s clusters with customer toggles for enable/disable and config editing, reducing alert burden through automated remediation (default opt-out)
- Improve observability stack with third-party metrics/logging integration, proper alerting, and Mimir cost reduction (currently ~$0.0375/host/h)
- Build Kubernetes Add-On System enabling customers to opt-in to Advanced Metrics (ex-Lighthouse) with writable Grafana dashboards and configure NVSentinel
- Establish security & compliance foundation (Owner: Jason Kichen) with emergency update incident response plan, NVIDIA embargo program compliance, OS/K8s/SLURM hardening (CIS benchmarks, 80%+ clusters hardened), vulnerability scanning (bare metal + K8s with automated daily scans and SLA-based remediation), Tailscale/Teleport ACL hardening (95%+ reduction in unnecessary prod access), and security incident response team with customer communication templates
- Contribute to company-wide mono-repo

### Inference (Software)

**Overview:** The Inference team is building the technical foundation and business model for TPU-based inference as a new product line. This quarter focuses on proving technical capability through large model benchmarking, securing design partner commitments, and maintaining strategic competitive positioning by restricting TPU access to inference competitors.

**Key Priorities:**
- Build technical foundation by hiring 4-6 inference engineers (kernel + serving teams), benchmarking ≥2 reasoning models (600B+ params) on v7 hardware, and demonstrating customer deployments (Cursor, Perplexity) with <10% performance degradation
- Validate business model by securing LOIs from 3-5 tier-1 customers willing to commit to token minimums, defining $/token pricing with 50%+ margin, and securing commitment for 1-2 v7 pods for mid-2026 launch
- Maintain strategic positioning by ensuring zero TPU capacity sold to inference competitors (Fireworks/Baseten/Together), validating multi-tenant k8s for inference workloads, and communicating capability to ≥10 select customers/investors
- Prototype disaggregated prefill/decode architecture with basic routing/load balancing operational

### Customer Engineering

**Overview:** Customer Engineering is focused on reducing operational toil, improving processes for cluster lifecycle management, leveling up team capabilities, and establishing supplier quality standards jointly with Cluster Ops. These improvements are essential for scaling customer support as the business grows while maintaining consistent quality across suppliers.

**Key Priorities:**
- Reduce on-call toil by implementing P0-only paging (system down/cluster-wide degradation) and Jira work tracking for P1+ issues during business hours
- Build sustainable cluster tracking with 100% of active clusters trackable in Jira MRKT board with customer, supplier, and contractual details
- Level up team capabilities with 100% CKA certification and implement formal PoC process with Discovery Agreements for all presales engagements
- **(Joint with Cluster Ops)** Standardize supplier quality through published Technical Requirements document, real-time Supplier Quality Dashboard (uptime, incident response, deployment success), migration to managed k8s/SLURM on k8s only, and supplier scorecard integration into presales process

---

## Team Health and Hiring

### Overview

Across all teams, Q1 2026 involves aggressive hiring to support the scale required for Stream/CB3 deployments and new product lines. The organization is targeting 16+ new hires while simultaneously working to retain and repatriate team members who have moved between organizations.

### Key Hiring Targets by Team

| Team | Hiring Target | Key Roles |
|------|---------------|-----------|
| **Procurement** | +4 | 3x Strategic Sourcing Managers, 1x AP Manager |
| **Infra Compute** | +2 | Infra Compute Engineers contributing to O1/O2 |
| **Networking** | +2 | Deployment Lead, Deployment Engineer, (Stretch: Network Security Engineer) |
| **Mike Ops (Software)** | +4 | SRE with 50/50 timezone balance (west coast/London) |
| **Inference** | +4-6 | 2-3 Kernel Engineers (TPU/JAX/XLA), 2-3 Serving Engineers (k8s scheduling) |
| **Total** | **16-18** | Roles span procurement, infrastructure, and software engineering |

### Organizational Alignment (Mike Ops)

Beyond hiring, Mike Ops is focused on two critical organizational objectives:

**O1: Hire and retain the best talent**
- Add +4 SRE with 50/50 timezone balance between west coast and London
- "Repatriate" team members lost to the infra team

**O2: Align sales org around product roadmap**
- Ensure go/top40 customers are aligned to specific products
- Bridge the gap between sales organization and engineering product roadmap

### Hiring Risk Considerations

With 16-18 new hires targeted across Q1 and multiple teams citing hiring velocity as a dependency (see Critical Cross-Team Dependencies below), the organization should consider:
- **Prioritization matrix**: If hiring is slower than expected, which roles are most critical to Stream/CB3 success?
- **Onboarding capacity**: Multiple teams need new hires to be productive quickly (e.g., Infra Compute: 2-day prod/dev access, contributing to deployments by Q1 end)
- **Competitive landscape**: TPU/JAX/XLA kernel engineers and SRE talent are highly competitive markets
- **Team distribution**: Inference team specifically needs co-located engineers ("single location"), which may impact candidate pool

---

## Critical Cross-Team Dependencies

The following dependencies were explicitly called out in the Infrastructure OKRs and represent potential bottlenecks:

| Dependent Team | Dependency | Blocking Impact |
|----------------|------------|-----------------|
| **Networking** | DCIM/Software: NetBox model completeness, gNMI API access | Blocks config generation, observability |
| **Networking** | ICT: Cabling execution from cutsheets, physical infrastructure readiness | Blocks deployment timeline |
| **Networking** | HW Operations: Room access, power/cooling validation, handover acceptance | Blocks deployment start, handover |
| **Networking** | Recruiting/HR: Deployment Lead, NRE, Enterprise Eng hiring velocity | Blocks team capacity for CB3 |
| **Multiple** | Procurement: IT infrastructure, vendor selection, warehouse logistics | Blocks all physical deployments |
| **Multiple** | DCIM Tooling: Asset tracking, NetBox accuracy | Blocks automated deployments |

---

## Recommended Improvements

### 1. **Assign Missing Owners to Critical KRs**

**Issue:** Many critical key results lack assigned owners, creating accountability gaps that could delay execution.

**Examples:**
- Infra Compute O1 (Deploy Sanidine Stream sub-pod): All 4 KRs lack owners
- Infrastructure Deployment O1 (Deliver v7 POD): All 3 KRs lack owners
- Infra Compute O2 KR2 (Total sub-pod deployment time): Target is "[Y days/weeks]" - needs specific value

**Recommendation:** Assign explicit owners to every KR, especially for Stream/CB3 deployment objectives. Consider using RACI framework to clarify accountable vs. responsible parties where multiple people are involved.

### 2. **Lab 2.0 Timeline Aligned Across Teams** ✓

**Previous Issue:** Two different dates were specified for lab operational readiness (March 1 vs March 31), creating confusion across Infra Compute, Networking, and Procurement teams.

**Resolution:** All teams now aligned on **March 31** operational date with synchronized intermediate milestones:
- **Jan 31:** Lab site selected (Procurement O1 KR4)
- **Feb 15:** Lab migration plan and approved BOM complete (Procurement O1 KR4 + Networking O3 KR3.4)
- **Mar 15:** Equipment delivered, racked, and network components deployed
- **Mar 31:** Lab 2.0 operational and validated (Infra Compute O2 KR3, Networking O3 KR3.4)

**Key Benefits:**
- Clear dependency chain from Procurement → Equipment Delivery → Network/Compute Deployment → Validation
- Intermediate checkpoints enable early detection of slippage
- Aligned expectations across all teams dependent on Lab 2.0 (including optic qualification program in Networking O4 KR4.3)

### 3. **Consolidate Duplicate Objectives and Clarify Ownership**

**Issue:** Several objectives appear duplicated across teams without clear ownership boundaries:

**Company-wide Mono-repo:**
- Cluster Ops O3 KR1: Merge ClusterOps, Atlas, Lighthouse repos
- Platform Ops O6 KR1: Merge ClusterOps, Atlas, Lighthouse repos
- *Who owns this initiative? What happens if teams disagree on approach?*

**Asset Tracking within 24 hours:**
- Procurement O2 KR4: "Integration with internal asset management system to ensure that assets are tracked within 24 hours of delivery" (Owner: Hannah Mulvaney)
- DCIM O2 KR2.1: "100% of assets tracked within 24 hours of delivery (zero manual entry)" (Owner: Hannah Mulvaney)
- *Are these the same objective or different aspects? Should be consolidated or clarified.*

**Recommendation:**
- Designate a single owner/DRI for the mono-repo initiative with clear decision-making authority
- Clarify asset tracking objectives - if they're the same, consolidate into one team's OKRs; if different, specify the boundary (e.g., physical receipt vs. NetBox ingestion)

### 4. **Specify Missing Numeric Targets**

**Issue:** Several KRs use placeholder values or vague targets that make success criteria unclear:

- Cluster Ops O2 KR1: "Reduce page volume by **xx%**" - needs specific target
- Platform Ops O3 KR4: "NVSentinel installation on **yy%** of clusters" - needs specific target
- Infra Compute O2 KR2: "Total sub-pod deployment time ≤ **[Y days/weeks]**" - needs specific target

**Recommendation:** Fill in all numeric targets based on baseline measurements and desired outcomes. If baselines don't exist, add a KR to establish baseline metrics first, then set targets for subsequent quarters.

### 5. **Create Cross-Team Dependency Management Plan**

**Issue:** Critical dependencies are identified but there's no clear mitigation strategy if dependencies slip. Multiple teams cite aggressive timelines and dependencies on:
- Recruiting/HR delivering multiple roles across teams (Infra Compute +2, Networking +2, Mike Ops +4, Inference +4, Procurement +4)
- DCIM/NetBox completeness blocking Networking automation
- ICT/Physical infrastructure readiness blocking deployments

**Specific Risks:**
- **Hiring velocity**: 16+ new hires across teams in Q1 is ambitious. What's the prioritization if recruitment is slower than expected?
- **DCIM KR2.2 has "Owner: TBD"**: Shipping/ASN automation is foundational but has no owner assigned
- **NetBox completeness**: Multiple teams depend on DCIM achieving 100% NetBox model completeness for Stream/CB3, but this is a complex multi-stakeholder objective

**Recommendation:**
- Establish weekly cross-functional sync for Stream/CB3 deployment teams (Procurement, Infra Compute, Networking, DCIM, Infrastructure Deployment) with dependency tracking dashboard
- Create hiring prioritization matrix across teams - if you can only hire 8 of 16 planned roles, which are most critical?
- Assign owner to DCIM O2 KR2.2 immediately (Shipping/ASN automation)
- Add intermediate checkpoints for NetBox completeness (e.g., 80% by mid-Feb, 100% by end-Feb) so dependent teams can adjust plans if slippage occurs

### 6. **Joint Supplier Quality & Standardization Objective Established** ✓

**Previous Issue:** Customer Engineering O5 and Cluster Ops O1 KR3 both aimed to standardize suppliers but lacked joint ownership and clear coordination mechanisms.

**Resolution:** Created joint objective "Supplier Quality & Standardization" (Cluster Ops O4 / Customer Engineering O5) with shared accountability:
- **KR1: Supplier Technical Requirements document** - Mandatory capabilities (managed k8s/SLURM on k8s only), infrastructure requirements, handover checklists with leadership approval
- **KR2: Supplier Quality Dashboard** - Real-time automated metrics (uptime %, incident response time, deployment success rate, FSH coverage, ticket resolution) with Red/Yellow/Green indicators accessible to Sales, CE, and leadership
- **KR3: Supplier migration to standardized offerings** - 100% new deployments enforced via tooling, existing bare metal identified with migration plan by Feb 15, all suppliers acknowledge requirements
- **KR4: Supplier scorecard integrated into presales** - PoC/Discovery Agreement templates include quality checks, Sales team trained, 100% of Q1 engagements reference quality metrics

**Key Benefits:**
- Unified ownership (Cluster Ops Lead + Customer Engineering Lead + Sales Ops)
- Operational enforcement (deployment tooling) aligned with customer-facing commitments (presales process)
- Data-driven supplier management with automated dashboard eliminating manual reporting
- Clear technical standards prevent ad-hoc exceptions that create operational burden

### 7. **Unified Observability Team Established - Addresses Previous Fragmentation** ✓

**Previous Issue:** Multiple observability initiatives were in flight without clear integration across Platform Ops, Cluster Ops, and Networking teams.

**Resolution:** Created unified Observability Team OKRs (infra.md) that consolidate:
- **O1: Unified observability architecture** - Defines reference architecture, completes Lighthouse → Advanced Metrics transition, establishes compute/network integration contracts
- **O2: FSH as standard internal ops tool** - Deploys FSH on 100% of clusters, reduces page volume by 40%, powers automated remediation
- **O3: Customer self-service via Advanced Metrics Add-On** - Kubernetes Add-On System with console integration, customer Grafana, programmatic API access
- **O4: Cost and scalability optimization** - Reduces Mimir costs to <$0.025/host/h (33% reduction), evaluates third-party options, load-tests for CB3 scale, completes Stream network observability handover

**Key Benefits:**
- Clear separation of concerns: FSH (internal ops), Advanced Metrics (customer self-service), Network Observability (network telemetry)
- Unified ownership under Victor Blake (NRE Lead) and Platform Ops Lead
- Specific cost and performance targets with accountability
- Integration points explicitly defined to prevent duplication

---

## Strengths

- **Clear focus on Stream/CB3 deployments** with strong alignment across Procurement, Infra, Networking, DCIM, and Infrastructure Deployment teams
- **Significant investment in automation and tooling** (NetBox, ZTP, asset tracking, NVSentinel) to enable future scale
- **Security & compliance foundation** established with emergency incident response, NVIDIA embargo program, hardening standards (CIS benchmarks), vulnerability scanning, and proper access controls (Tailscale/Teleport ACLs)
- **Unified observability strategy** with dedicated Observability Team consolidating FSH, Advanced Metrics, and network observability into coherent architecture
- **Joint objectives demonstrate organizational maturity** - Supplier Quality & Standardization (Cluster Ops + Customer Engineering) and Observability Team show ability to break down silos with shared accountability
- **Customer experience improvements** with management cluster migration, Add-On System, self-service monitoring, and data-driven supplier quality management via automated dashboards
- **Team capacity building** across multiple organizations with concrete hiring targets (16-18 hires) and onboarding goals
- **Documented dependencies** provide transparency into cross-team coordination needs

---

## Summary

Q1 2026 represents a critical quarter where Fluidstack is transitioning from scrappy execution to scaled, repeatable operations. The Stream/CB3 deployments are the proving ground for processes, tooling, and team capacity that will enable 2026+ growth. Success requires tight coordination across 11 teams (including the newly established Observability Team), aggressive hiring (16-18 new team members), and rapid automation development.

The creation of a unified Observability Team exemplifies the organizational maturity being built this quarter - consolidating fragmented initiatives into coherent, scalable architectures with clear ownership. The recommended improvements focus on clarifying ownership, resolving conflicts, and strengthening coordination mechanisms to mitigate the significant execution risk inherent in this ambitious quarter.
