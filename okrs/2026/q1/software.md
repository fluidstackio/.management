# Marketplace/Software Objectives and Key Results (OKRs) Q1 2026

# Cluster & Platform Ops

### O1: Deployments are standardized and fast to deploy by everyone on the team

- **KR1:** Deployments progress at a minimum of 1000 GPUs/hr

  **Owner:** TBD

- **KR2:** Migrate all clusters[^1] to new ClusterOps stack, including regional management clusters (Goal 100%, currently at 19%)

  **Owner:** TBD

- **KR3:** SLURM on k8s as the default SLURM deployment, zero "bare metal" SLURM deployments (including POCs)

  *Note: This KR is enforced via Supplier Quality & Standardization requirements (see Customer Engineering O5) which establish technical requirements and deployment tooling enforcement.*

  **Owner:** TBD

- **KR4:** Clusters are decommissioned within 24h and there are zero spurious pages for decommissioned clusters

  **Owner:** TBD

### O2: Clusters are reliable and alerts are routed properly

- **KR1:** Reduce page volume by 40% via better alerting from FS System Health

  **Owner:** TBD

- **KR2:** Fluidstack System Health (FSH) is available on all clusters, is appropriately managed and scaled, with zero pages and manageable costs; Lighthouse is separated from FSH and broken into its own product

  **Owner:** TBD

- **KR3:** All supplier escalations are automatically forwarded to relevant suppliers; all customer alerts forwarded to customer channel

  **Owner:** TBD

- **KR4:** Observability stack improvements delivered

  *Note: Observability strategy and implementation is coordinated with the Observability Team (see infra.md Observability Team OKRs). Key dependencies:*
  - *FSH deployment and cost optimization (Observability Team O2, O4)*
  - *Customer-facing Advanced Metrics (Observability Team O3)*
  - *Network/compute observability integration (Observability Team O1)*

  **Owner:** TBD

- **KR5:** Auto-remediation reduces MTTR to <15min (software) / <4hrs (hardware)

  - Deploy comprehensive DCGM health checks (passive + active) across all clusters
  - Implement automated drain → diagnose → repair → reintegrate pipeline
  - Target: 85% of failures resolved without human intervention
  - ClusterMAX Platinum requirement: MTTR <15min for software failures, <4hrs for hardware failures

  **Owner:** TBD

### O3: Build ClusterMAX Platinum foundation

Build automated operations and security depth to achieve ClusterMAX Platinum tier by mid-2026. Q1 focuses on establishing foundational capabilities that will be completed and validated for Platinum certification in Q2/Q3.

- **KR1:** Auto-Remediation - Reduce MTTR to <15min (software) / <4hrs (hardware)

  *See O2 KR5 for detailed implementation. ClusterMAX Platinum requires MTTR <15min for software failures, <4hrs for hardware failures with 85% automation.*

  **Owner:** TBD

- **KR2:** Security Hardening - Achieve industry-leading security posture

  *See O5 KR1 for NVIDIA embargo program and <24hr CVE patching SLA. See O5 KR3 for InfiniBand 7-key security implementation (ClusterMAX Platinum requirement).*

  **Owner:** Jason Kichen

- **KR3:** Auth & Access - Deploy production-grade SSO for SLURM + K8s

  - Integrate Google Workspace/Okta for unified authentication
  - API-driven user provisioning with RBAC enforcement
  - Single login → SLURM access + kubeconfig + Grafana dashboards

  **Owner:** TBD

- **KR4:** Performance & DX - Match CoreWeave's developer experience benchmarks

  - Deploy NGC mirrors: <15s container pulls (currently 45-60s)
  - Pre-configured SLURM job templates + topology-aware scheduling
  - Public metrics dashboard showing uptime, MTTR, and MFU performance

  **Owner:** TBD

### O4: Fluidstack managed Kubernetes is reliable and fully featured (including SLURM on K8s)

- **KR1:** All K8s clusters migrated to management clusters

  - Customer clusters do not contain Fluidstack control-plane components
  - Management cluster architecture operational and scaled appropriately
  - Aggregate region information at the hub layer for unified control plane

  **Owner:** TBD

- **KR2:** NVSentinel running on all K8s clusters

  - CRD for reboots and tickets operational for all clusters
  - Customer toggle to enable/disable from console
  - Customer can edit/amend config for remediation
  - Reduce alert burden through remediation via NVSentinel installation on 90% of clusters, installed by default with opt-out

  **Owner:** TBD

- **KR3:** Kubernetes Add-On System operational

  - Users can opt-in to Fluidstack Advanced Metrics (ex-Lighthouse) with customer Grafana and writable/editable dashboards
  - Static (non-CRD) configurations supported
  - Users can opt-out of NVSentinel
  - Users can configure NVSentinel

  **Owner:** TBD

- **KR4:** SLURM on k8s fully featured and production-ready

  - SLURM on k8s integrated with Kubernetes Add-On System architecture
  - Feature parity with bare metal SLURM for production workloads
  - Documentation and runbooks for SLURM on k8s operations

  **Owner:** TBD

- **KR5:** Can deploy Kubernetes on TPU v7 and schedule a workload on a 2x2x2 slice

  **Owner:** TBD

### O5: Security & Compliance Foundation

Establish security fundamentals for production infrastructure including vulnerability management, incident response, access controls, and compliance with vendor security programs

- **KR1:** Vulnerability scanning and remediation program operational for bare metal and Kubernetes (HIGHEST PRIORITY)

  **Vulnerability Scanning and Remediation:**
  - Vulnerability scanning tooling selected and deployed (e.g., Trivy, Anchore, Qualys, or equivalent for both bare metal and containers)
  - Automated daily scans operational for: OS packages (bare metal), container images, Kubernetes configurations, SLURM components
  - Vulnerability reporting dashboard operational with severity classification (Critical/High/Medium/Low) and SLA-based remediation tracking
  - Process documented: scan → triage → remediation → verification cycle with clear ownership and SLAs (e.g., Critical: 7 days, High: 30 days)
  - ≥90% of Critical vulnerabilities remediated within SLA by end of Q1

  **NVIDIA Embargo Program:**
  - Fluidstack enrolled in NVIDIA Product Security Incident Response Team (PSIRT) program
  - Secure communication channel established for embargo notifications (dedicated email, PGP keys if required)
  - Internal process documented: embargo notification → impact assessment → patch testing → deployment coordination
  - <24hr CVE patching SLA for Critical vulnerabilities (ClusterMAX Platinum requirement)
  - ≥2 Platform Ops team members trained on embargo handling procedures

  **Owner:** Jason Kichen

- **KR2:** Comprehensive security incident response capability established

  **Emergency Update Response:**
  - Documented incident response playbook for critical security updates (firmware, OS, network devices) with severity classification and response timelines
  - Tested emergency update procedure on ≥1 non-production cluster (simulated critical CVE)
  - Runbook includes: impact assessment, customer communication template, rollback procedures, post-mortem process
  - Plan approved by Platform Ops Lead, Cluster Ops Lead, and Networking Lead

  **Security Incident Response Team:**
  - Security incident response team identified with clear roles (Incident Commander, Communications Lead, Technical Lead)
  - Incident severity classification defined (P0-P3) with escalation paths and response SLAs
  - Customer communication templates created for security incidents (initial notification, updates, post-incident report)
  - Security incident tracking integrated into Jira with appropriate confidentiality controls
  - At least 1 tabletop exercise completed with security incident response team

  **Owner:** Jason Kichen

- **KR3:** Infrastructure hardening and production access controls implemented

  **OS, Kubernetes, and SLURM Hardening:**
  - Hardening standards documented following CIS benchmarks (or equivalent): OS (Ubuntu/RHEL), Kubernetes, SLURM
  - Key hardening measures implemented: disable unnecessary services, secure SSH config, RBAC policies (k8s), network policies, secrets management
  - Automated hardening validation added to deployment pipeline (fails deployment if standards not met)
  - ≥80% of clusters meet hardening standards by end of Q1 (100% of new deployments)

  **InfiniBand Security (ClusterMAX Platinum requirement):**
  - Implement full 7-key InfiniBand security: Management (M), Partition (P), Subnet Administrator (SA), Virtual Subnet (VS), Communication (C), Node-to-Node (N2N), Application Management (AM)
  - Security keys rotated on documented schedule
  - Validation testing for all 7 key types operational

  **Tailscale and Teleport Access Controls:**
  - Audit completed: identify all users with Tailscale/Teleport access, classify by role and required access level (prod/dev/staging)
  - ACLs implemented: restrict prod access to only users requiring it (principle of least privilege), separate dev/staging/prod networks
  - Access request/approval workflow documented and operational for production access
  - ≥95% reduction in users with unnecessary prod access, zero standing prod access for non-ops roles
  - Quarterly access review process established (first review completed in Q1)

  **Owner:** Jason Kichen

## Stretch Goals

- Console shows basic metrics from FS System Health
- Expose a way for customers to consume our FSH and Advanced metrics programmatically

# Mike Ops

### O1: Hire and retain the best talent

- **KR1:** Add +4 SRE and achieve 50/50 time zone balance between west coast/London

  **Owner:** TBD

- **KR2:** "Repatriate" all team members lost to the infra team

  **Owner:** TBD

### O2: Align sales org around product roadmap

- **KR1:** go/top40 customers are aligned to a product

  **Owner:** TBD


# Inference

### O1: Build technical foundation and team for TPU-based inference

- **KR1:** Hire and onboard 4-6 inference engineers (2-3 kernel team, 2-3 serving team) with relevant TPU/JAX/XLA or k8s scheduling expertise

  **Owner:** TBD

- **KR2:** Benchmark ≥2 reasoning models (600B+ params) on v7 hardware, achieving competitive tok/sec vs GPU baselines

  **Owner:** TBD

- **KR3:** Demonstrate successful deployment of customer-provided model (e.g., Cursor, Perplexity) with <10% performance degradation vs reference implementation

  **Owner:** TBD

- **KR4:** Prototype disaggregated prefill/decode architecture operational with basic routing/load balancing

  **Owner:** TBD

### O2: Validate business model with design partners

- **KR1:** Identify and secure LOIs from 3-5 tier-1 inference customers willing to commit to token minimums on TPU

  **Owner:** TBD

- **KR2:** Define $/token pricing model with target 50%+ margin validated against v7 economics

  **Owner:** TBD

- **KR3:** Secure commitment for 1-2 v7 pods with delivery timeline aligned to mid-2026 launch

  **Owner:** TBD

### O3: Maintain strategic positioning

- **KR1:** Zero TPU capacity sold to Fireworks/Baseten/Together or other inference competitors

  **Owner:** TBD

- **KR2:** Multi-tenant k8s architecture validated for inference workloads (dependency: Platform Ops O2)

  **Owner:** TBD

- **KR3:** Inference capability communicated to select customers and investors (documented conversations with ≥10 targets)

  **Owner:** TBD

---

## Footnotes

[^1]: Except Mistral, MBZ
