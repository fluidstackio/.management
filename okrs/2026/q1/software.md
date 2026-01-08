# Marketplace/Software Objectives and Key Results (OKRs) Q1 2026

# Cluster Ops

## O1: Deployments are standardized and fast to deploy by everyone on the team

### KR1: Deployments progress at a minimum of 1000 GPUs/hr

### KR2: Migrate all clusters[^1] to new ClusterOps stack, including regional management clusters (Goal 100%, currently at 19%)

### KR3: SLURM on k8s as the default SLURM deployment, zero "bare metal" SLURM deployments (including POCs)

*Note: This KR is enforced via the joint Supplier Quality & Standardization objective (O4 below) which establishes technical requirements and deployment tooling enforcement.*

### KR4: Clusters are decommissioned within 24h and there are zero spurious pages for decommissioned clusters

## O2: Clusters are reliable and alerts are routed properly

### KR1: Reduce page volume by xx% via better alerting from FS System Health

### KR2: Fluidstack System Health (FSH) is available on all clusters, is appropriately managed and scaled, with zero pages and manageable costs; Lighthouse is separated from FSH and broken into its own product

### KR3: All supplier escalations are automatically forwarded to relevant suppliers; all customer alerts forwarded to customer channel

## O3: (joint) Company wide mono-repo

### KR1: Merge ClusterOps, Atlas and Lighthouse Repos

## O4: (joint with Customer Engineering) Supplier Quality & Standardization

Standardize supplier offerings and establish quality requirements to ensure consistent customer experience across all suppliers

### KR1: Define and publish Supplier Technical Requirements document

- Document mandatory technical capabilities: managed k8s or SLURM on k8s (zero bare metal exceptions)
- Specify infrastructure requirements: network topology, storage, monitoring/observability access, incident response SLAs
- Define handover checklist: what Fluidstack needs from suppliers at cluster turnup (credentials, monitoring endpoints, escalation paths)
- Approval from Cluster Ops and Customer Engineering leadership

**Owner:** Cluster Ops Lead, Customer Engineering Lead

### KR2: Establish Supplier Quality Dashboard

- Real-time dashboard showing per-supplier metrics: uptime %, incident response time, deployment success rate, FSH coverage, ticket resolution time
- Automated data collection from Jira, FSH, deployment tooling (no manual updates)
- Red/Yellow/Green status indicators for each supplier against SLA thresholds
- Dashboard accessible to Sales, Customer Engineering, and leadership

**Owner:** Cluster Ops Lead, Customer Engineering Lead

### KR3: Migrate all suppliers to standardized offerings by end of Q1

- 100% of new deployments use managed k8s or SLURM on k8s (enforcement via deployment tooling)
- Existing bare metal SLURM clusters identified with migration plan by Feb 15
- All active suppliers acknowledged Supplier Technical Requirements (signed attestation or contract amendment)

**Owner:** Cluster Ops Lead, Customer Engineering Lead

### KR4: Supplier scorecard integrated into presales process

- PoC/Discovery Agreement template includes supplier quality check (reference to dashboard)
- Sales team trained on supplier quality metrics and how to communicate to customers
- 100% of Q1 presales engagements reference supplier quality in customer-facing materials

**Owner:** Customer Engineering Lead, Sales Ops

# Mike Ops

## O1: Hire and retain the best talent

### KR1: Add +4 SRE and achieve 50/50 time zone balance between west coast/London

### KR2: "Repatriate" all team members lost to the infra team

## O2: Align sales org around product roadmap

### KR1: go/top40 customers are aligned to a product


# Platform Ops

## O1: Customer experience meets or exceeds ClusterMAX™ Gold

### KR1: Aggregate region information at the hub layer

## O2: Migrated all existing K8s clusters to management clusters

### KR1: Customer clusters do not contain Fluidstack control-plane components

## O3: NVSentinel running on all K8s clusters

### KR1: CRD for reboots and tickets for all

### KR2: Customer toggle to enable/disable from console

### KR3: Customer can edit/amend config for remediation

### KR4: Reduce alert burden through remediation via NVSentinel installation on yy% of clusters, and is installed by default with an opt out

## O4: Improved observability stack

### KR1: Use third party metrics and logging fully integrated

### KR2: Alerting working as per expected

### KR3: Reduce cost of hosting Mimir (currently ~0.0375$/host/h)

## O5: Kubernetes Add-On System

### KR1: Users can opt-in to Fluidstack Advanced Metrics (ex-Lighthouse)

#### KR1.1: Customer grafana with writable/editable dashboards

#### KR1.2: Static (non-CRD) configurations

### KR2: Users can opt-out of NVSentinel

### KR3: Users can configure NVSentinel

## O6: (joint) Company wide mono-repo

### KR1: Merge ClusterOps, Atlas and Lighthouse Repos

## O7: Security & Compliance Foundation

Establish security fundamentals for production infrastructure including incident response, vulnerability management, access controls, and compliance with vendor security programs

### KR1: Emergency firmware/OS/networking update incident response plan operational

- Documented incident response playbook for critical security updates (firmware, OS, network devices) with severity classification and response timelines
- Tested emergency update procedure on ≥1 non-production cluster (simulated critical CVE)
- Runbook includes: impact assessment, customer communication template, rollback procedures, post-mortem process
- Plan approved by Platform Ops Lead, Cluster Ops Lead, and Networking Lead

**Owner:** Jason Kichen

### KR2: NVIDIA embargo program compliance established

- Fluidstack enrolled in NVIDIA Product Security Incident Response Team (PSIRT) program
- Secure communication channel established for embargo notifications (dedicated email, PGP keys if required)
- Internal process documented: embargo notification → impact assessment → patch testing → deployment coordination
- ≥2 Platform Ops team members trained on embargo handling procedures

**Owner:** Jason Kichen

### KR3: OS, Kubernetes, and SLURM hardening standards implemented

- Hardening standards documented following CIS benchmarks (or equivalent): OS (Ubuntu/RHEL), Kubernetes, SLURM
- Key hardening measures implemented: disable unnecessary services, secure SSH config, RBAC policies (k8s), network policies, secrets management
- Automated hardening validation added to deployment pipeline (fails deployment if standards not met)
- ≥80% of clusters meet hardening standards by end of Q1 (100% of new deployments)

**Owner:** Jason Kichen

### KR4: Vulnerability scanning plan operational for bare metal and Kubernetes

- Vulnerability scanning tooling selected and deployed (e.g., Trivy, Anchore, Qualys, or equivalent for both bare metal and containers)
- Automated daily scans operational for: OS packages (bare metal), container images, Kubernetes configurations, SLURM components
- Vulnerability reporting dashboard operational with severity classification (Critical/High/Medium/Low) and SLA-based remediation tracking
- Process documented: scan → triage → remediation → verification cycle with clear ownership and SLAs (e.g., Critical: 7 days, High: 30 days)

**Owner:** Jason Kichen

### KR5: Tailscale and Teleport access controls hardened

- Audit completed: identify all users with Tailscale/Teleport access, classify by role and required access level (prod/dev/staging)
- ACLs implemented: restrict prod access to only users requiring it (principle of least privilege), separate dev/staging/prod networks
- Access request/approval workflow documented and operational for production access
- ≥95% reduction in users with unnecessary prod access, zero standing prod access for non-ops roles
- Quarterly access review process established (first review completed in Q1)

**Owner:** Jason Kichen

### KR6: Security incident response team and communication plan established

- Security incident response team identified with clear roles (Incident Commander, Communications Lead, Technical Lead)
- Incident severity classification defined (P0-P3) with escalation paths and response SLAs
- Customer communication templates created for security incidents (initial notification, updates, post-incident report)
- Security incident tracking integrated into Jira with appropriate confidentiality controls

**Owner:** Jason Kichen

## Stretch OXs (Depends on ClusterOps)

- Console shows basic metrics from FS System Health
- Expose a way for customers to consume our FSH and Advanced metrics programmatically

# Inference

## O1: Build technical foundation and team for TPU-based inference

### KR1: Hire and onboard 4-6 inference engineers (2-3 kernel team, 2-3 serving team) with relevant TPU/JAX/XLA or k8s scheduling expertise

### KR2: Benchmark ≥2 reasoning models (600B+ params) on v7 hardware, achieving competitive tok/sec vs GPU baselines

### KR3: Demonstrate successful deployment of customer-provided model (e.g., Cursor, Perplexity) with <10% performance degradation vs reference implementation

### KR4: Prototype disaggregated prefill/decode architecture operational with basic routing/load balancing

## O2: Validate business model with design partners

### KR1: Identify and secure LOIs from 3-5 tier-1 inference customers willing to commit to token minimums on TPU

### KR2: Define $/token pricing model with target 50%+ margin validated against v7 economics

### KR3: Secure commitment for 1-2 v7 pods with delivery timeline aligned to mid-2026 launch

## O3: Maintain strategic positioning

### KR1: Zero TPU capacity sold to Fireworks/Baseten/Together or other inference competitors

### KR2: Multi-tenant k8s architecture validated for inference workloads (dependency: Platform Ops O2)

### KR3: Inference capability communicated to select customers and investors (documented conversations with ≥10 targets)

---

## Footnotes

[^1]: Except Mistral, MBZ
