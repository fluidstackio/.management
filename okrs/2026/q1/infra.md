# Infra Compute OKRs

## O1: Deploy Sanidine Stream sub-pod successfully

### KR1: Provision 576 machines in parallel (1 row) with <5% failure rate requiring manual intervention

**Owner:** TBD

### KR2: Total sub-pod deployment time ≤ 10 days from rack-ready to workload-ready

**Owner:** TBD

### KR3: 100% of deployed machines export metrics to TPU-CC and are exported to the observability pipeline within 10 minutes of provisioning

**Owner:** TBD

### KR4: ≥80% of hardware qualification failures handled end-to-end by automated remediation (reboot, re-image, ticket escalation)

**Owner:** TBD

## O2: Achieve deployment readiness for Bloom CB3 (3 pods)

Readiness means we've validated the tooling/process can scale, even if deployment happens later

### KR1: Deployment runbook validated: complete dry-run of 1 pod equivalent in staging/lab environment

**Owner:** TBD

### KR2: Provisioning system load-tested to handle 2x current parallel capacity (baseline for 2 concurrent pods)

**Owner:** TBD

### KR3: Lab environment operational by March 31st with 1 rack V7, 1 Deschutes CDU, VAST cluster

- Lab site selected by Jan 31 (dependency: Procurement O1 KR4)
- Lab migration plan and approved BOM by Feb 15 (dependency: Procurement O1 KR4)
- Equipment delivered and racked by Mar 15
- Lab 2.0 operational and validated by Mar 31

**Owner:** TBD

## O3: Build team capacity to sustain Q2+ scale

### KR1: All new hires have secure access to prod/dev resources within 2 business days of start date

**Owner:** TBD

### KR2: Deployment runbook and troubleshooting guides documented and reviewed by ≥2 team members

**Owner:** TBD

### KR3: 2 infra compute hires onboarded and contributing to O1/O2 work by end of Q1

**Owner:** TBD


# Networking OKRs

## O1: Deploy Sanidine/Stream Network Successfully

Execution: deliver first TPU network and validate deployment engine

### KR1.1: 100% of Stream network infrastructure deployed and passing validation healthchecks

**Owner:** Deployment Lead Thomas Toquothty

### KR1.2: Handover checklist completed with Operations sign-off; Observability/Dashboards Established

**Owner:** NRE/OPs Victor Blake

### KR1.3: Corporate network operational at Sanidine site; on-site staff have secure connectivity

**Owner:** Enterprise NetEng Chris Wykoff

### KR1.4: Buffalo POP operational with WAN edge connectivity to 365DC; BGP peering validated

**Owner:** NE, Core Lukasz Sulek

## O2: Achieve CB3 Deployment Readiness

Capability: prove deployment engine can scale to 3-pod builds

### KR2.1: Cutsheet automation generates 100% of ICT materials from NetBox for Stream and CB3 (NET-73)

**Owner:** NE, Core Lukasz Sulek

### KR2.2: 100% of network configs generated from NetBox; ZTP success rate >95% on first boot (NET-74, NET-75)

**Owner:** NE, Core Lukasz Sulek

### KR2.3: Device qualification tool validates intended state for deployment; catches 100% of config drift (NET-76)

**Owner:** NE, Core Lukasz Sulek

### KR2.4: Deployment runbook validated via Stream execution; comprehensive handover artifacts documented

**Owner:** Deployment Lead Thomas Toquothty

### KR2.5: Network Deployment team staffed: Deployment Lead + 1 Deployment Engineer onboarded and contributing

**Owner:** Thomas Toquothty

## O3: Complete Q1 Network Designs

Engineering: design authority for Q1-Q2 builds; unblock procurement

### KR3.1: FIS Network HLD and LLD approved; BOM finalized and procurement unblocked

**Owner:** NE, Core Lukasz Sulek

### KR3.2: POP Network HLD and LLD approved; 2 additional POPs in design/procurement phase

**Owner:** NE, Core Lukasz Sulek

### KR3.3: Corporate Network Design for datacenters approved; standardized for future DC builds

**Owner:** Enterprise NetEng Chris Wykoff

### KR3.4: Lab 2.0 design complete; operational by March 31 with Network components procured/deployed

- Lab site selected by Jan 31 (dependency: Procurement O1 KR4)
- Network design complete and BOM approved by Feb 15
- Network components procured and deployed by Mar 15
- Lab 2.0 operational by Mar 31

**Owner:** NE, Core Lukasz Sulek

### KR3.5 (Stretch): Network Security Engineer onboarded; initial security strategy reviewed with CISO

**Owner:** Thomas Toquothty

## O4: Build Network Reliability Foundation

Observability: monitoring operational, qualification proven, dashboards live

### KR4.1: Observability stack operational (gNMI + Prometheus + Grafana); 100% of Stream devices reporting metrics (NET-95)

**Owner:** NRE Lead Victor Blake

### KR4.2: Deployment validation dashboards live; supports real-time deployment monitoring and handover verification

**Owner:** NRE Lead Victor Blake

### KR4.3: Optic qualification program operational; first vendor optics qualified per documented plan in Lab 2.0 (Dependency)

**Owner:** NRE Lead Victor Blake

### KR4.4: Alerting configured for critical network failures; escalation paths documented and tested

**Owner:** NRE Lead Victor Blake

# Cross-Team Dependencies

| Team | Dependency | Impact if Delayed |
|------|------------|-------------------|
| DCIM/Software | NetBox model completeness for Stream/CB3; gNMI API access | Blocks config generation, observability |
| ICT | Cabling execution from cutsheets; physical infrastructure readiness | Blocks deployment timeline |
| HW Operations | Room access, power/cooling validation, handover acceptance | Blocks deployment start, handover |
| Recruiting/HR | Deployment Lead, NRE, Enterprise Eng hiring velocity | Blocks team capacity for CB3 |

# DCIM/Networking Tooling OKRs

## O1: NetBox is the authoritative source of truth for all deployed infrastructure

### KR1.1: 100% model completeness and accuracy for Stream and CB3 (audit-verified)

**Owner:** Anshul Kamath

### KR1.2: Netbox model enables ability for tooling to identify cabling discrepancies and config (firmware, OS, IP, etc.) drift detection

**Owner:** Anshul Kamath, Aaron Jeyaraj

### KR1.3: 100% of necessary vendor Device traceability data ingested within 24 hours of shipment

**Owner:** Hannah Mulvaney

## O2: Asset lifecycle is fully automated from receipt to deployment

### KR2.1: 100% of assets tracked within 24 hours of delivery (zero manual entry)

**Owner:** Hannah Mulvaney

### KR2.2: Shipping/ASN status flows into NetBox within 4 hours automatically

**Owner:** TBD

### KR2.3: Zero consumable stockouts

**Owner:** Mubarak Jibril

### KR2.4: 100% of asset types have security classification and EOL defined

**Owner:** Hannah Mulvaney, Anshul Kamath

## O3: Network tooling enables reliable, repeatable pod deployment

### KR3.1: 100% of Network configs generated from Netbox

**Owner:** Anshul Kamath

### KR3.2: ZTP success rate > 95% on first boot

**Owner:** Sean Banko

### KR3.3: Cutsheet automation enabled to provide ICT materials Stream, CB3

**Owner:** Aaron Jeyaraj

### KR3.4: DCImporter automatically kicks off device qualification

**Owner:** Anshul Kamath

## O4: Repairs

### KR4.1: 100% of tickets auto-routed to correct on-call within 5 min

**Owner:** Thomas Barrett

### KR4.2: Customers can create tickets via support console (0 email/Slack-only requests)

**Owner:** Thomas Barrett, Aaron Jeyaraj

### KR4.3: Repair SOPs cover 100% of failures for non TPU, OCS racks (google to provide SOPs for these)

**Owner:** David Craig, Thomas Barrett


# Infrastructure Deployment OKRs

## O1: Deliver and Qualify 1 v7 POD at Stream

### KR1: CDU System fully installed and L4C Commissioned

**Owner:** TBD

### KR2: Network Infrastructure installed and fully configured

**Owner:** TBD

### KR3: v7 Machine Capacity fully installed and commissioned with Certificate of Completion

**Owner:** TBD

## O2: Deployment SOP Readiness

### KR1: FS Authored CDU SOPs and Process Map Developed

**Owner:** Lance Gardner

### KR2: FS Authored Network Infrastructure SOPs and Process Map Developed

**Owner:** Tom Marsh, David Schlotthauer

### KR3: FS Authored SPOCs/OCS SOPs and Process Map Developed

**Owner:** David Schlotthauer

## O3: Infrastructure Deployment Project Standup

### KR1: Develop standard project development process and workflow

**Owner:** Collin Phillips

### KR2: Develop SOPs for each of the project development process steps

**Owner:** Collin Phillips, Fangfei Chen

### KR3: Estimate durations for each of the project development process steps

**Owner:** Collin Phillips, Fangfei Chen

## O4: Pre-Execution Deliverables

### KR1: External Warehouse procured for CB3/Stream

**Owner:** Arjun Chimni

### KR2: ICT Vendor selection and contracting complete for CB3/Stream

**Owner:** Tom Marsh

### KR3: CDU Vendor selection and contracting complete for CB3/Stream

**Owner:** Lance Gardner

# Observability Team OKRs

## O1: Establish unified observability architecture with clear separation of concerns

Unify Lighthouse (customer-facing), Fluidstack System Health (internal operations), and network observability tooling into a coherent, scalable architecture

### KR1: Define and document observability reference architecture

- Clarify data flow from collection (compute, network, storage) → ingestion (Prometheus, gNMI) → storage (Mimir) → presentation (Grafana, dashboards)
- Specify separation boundaries: FSH (internal alerting/operations) vs Advanced Metrics (customer self-service) vs Network Observability (network-specific telemetry)
- Document cost model and optimization strategy with target metrics per layer

**Owner:** Victor Blake, Platform Ops Lead

### KR2: Complete Lighthouse → Advanced Metrics transition

- Lighthouse separated from FSH codebase and rebranded as "Fluidstack Advanced Metrics"
- Advanced Metrics packaged as Kubernetes Add-On with opt-in customer deployment
- Zero breaking changes for existing Lighthouse customers during transition

**Owner:** Platform Ops Lead

### KR3: Establish integration contract between compute and network observability

- Network metrics (gNMI from switches/routers) integrated into unified observability pipeline
- Cross-domain dashboards operational: correlate network health with compute/GPU metrics
- Shared alerting infrastructure routes network events to Network Ops, compute events to Cluster Ops

**Owner:** Victor Blake (NRE Lead), Platform Ops Lead

## O2: Deploy Fluidstack System Health (FSH) as standard internal operations tool

FSH provides internal monitoring, alerting, and automated remediation for all clusters

### KR1: FSH deployed on 100% of clusters (excluding Mistral, MBZ per software.md footnote)

- FSH available on all Stream, CB3, and existing production clusters
- Appropriately managed and scaled with zero pages related to FSH infrastructure itself
- Manageable costs with clear cost attribution per cluster

**Owner:** Cluster Ops Lead

### KR2: Reduce operator page volume by 40% through better FSH alerting

- Baseline established for current page volume (P0/P1/P2 breakdown)
- FSH alert tuning reduces spurious pages by 40% while maintaining 100% coverage of critical failures
- All supplier escalations automatically forwarded to relevant suppliers; all customer alerts forwarded to customer channel

**Owner:** Cluster Ops Lead, Platform Ops Lead

### KR3: FSH powers automated remediation integration

- FSH provides health signals to NVSentinel for automated remediation decisions
- Health check data flows into repair ticket routing (5-minute auto-route to on-call)
- Cluster decommissioning workflow integrated: zero spurious pages for decommissioned clusters within 24h

**Owner:** Cluster Ops Lead, Platform Ops Lead

## O3: Enable customer self-service observability through Advanced Metrics Add-On

Customers can opt-in to advanced monitoring/logging with writable dashboards and programmatic access

### KR1: Advanced Metrics Add-On available for customer opt-in

- Kubernetes Add-On System operational with Advanced Metrics as first add-on
- Customer toggle in console to enable/disable Advanced Metrics per cluster
- Customer Grafana with writable/editable dashboards deployed per cluster on opt-in

**Owner:** Platform Ops Lead

### KR2: Console integration shows basic metrics from FSH

- Console displays cluster health overview (GPU utilization, node status, basic alerts) sourced from FSH
- Real-time metrics updated every 30 seconds with <5 second latency from FSH
- UI/UX validated with ≥3 design partner customers

**Owner:** Platform Ops Lead, Console Team

### KR3: Programmatic access to observability data (Stretch)

- API endpoint operational for customers to consume FSH and Advanced Metrics programmatically
- Authentication/authorization model defined and implemented
- Documentation and example code published for common use cases (Prometheus-compatible query, webhook alerts)

**Owner:** Platform Ops Lead

## O4: Optimize observability cost and scalability for 2026 growth

Current Mimir costs (~$0.0375/host/h) must be reduced while scaling to support CB3 and future deployments

### KR1: Reduce Mimir hosting cost to <$0.025/host/h

- Identify cost drivers through infrastructure audit (storage, compute, retention policies)
- Implement optimizations: tiered storage, retention tuning, query optimization, right-sizing
- Achieve 33%+ cost reduction validated over 30-day period

**Owner:** Platform Ops Lead

### KR2: Third-party metrics and logging stack fully integrated

- Evaluation complete of external vendors (Datadog, Grafana Cloud, New Relic) vs self-hosted
- Decision documented with cost/benefit analysis
- If proceeding with third-party: integration operational with clear cost model and ROI

**Owner:** Platform Ops Lead

### KR3: Observability infrastructure load-tested for CB3 scale

- Load testing simulates 3-pod CB3 deployment with expected metric volume (estimated 10,000+ nodes, 80,000+ GPUs)
- Infrastructure scales horizontally without performance degradation
- Runbook documented for scaling observability infrastructure alongside cluster deployments

**Owner:** Platform Ops Lead, Victor Blake (NRE Lead)

### KR4: Network observability operational for Stream with handover to operations

- gNMI + Prometheus + Grafana stack deployed for 100% of Stream network devices
- Deployment validation dashboards live for real-time monitoring during Stream deployment
- Operations handover checklist completed with sign-off; alerting configured for critical network failures with documented escalation paths

**Owner:** Victor Blake (NRE Lead)

# Demand Management OKRs

## O1: Lay foundations for demand management

Enable customers to dynamically request and manage infrastructure capacity through APIs, validated in lab, with legal/contractual framework established

### KR1: BMS design for Stream, CB3 (and any BOM) defined by Jan 31

**Owner:** Sam Ourada

### KR2: BMS APIs defined and shared with customers by Feb 15

**Owner:** Sam Ourada

### KR3: Legal/contractual changes required for demand management defined and agreed upon by Feb 15

**Owner:** Sam Ourada

### KR4: Lab integration to BMS validated by Feb 28

**Owner:** Sam Ourada
