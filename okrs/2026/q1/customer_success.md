# Customer Engineering OKRs - Q1 2026

### O1: Reduce on-call toil

- **KR1:** Implement paging only for critical P0 system down or cluster wide degradation alerts

  **Owner:** TBD

- **KR2:** Implement Jira work tracking for P1 and below issues to be triaged during working hours

  **Owner:** TBD

### O2: Build sustainable process for tracking cluster lifecycle in Jira

- **KR1:** 100% of active clusters are trackable in Jira MRKT board with associated Customer, supplier, and contractual details

  **Owner:** TBD

### O3: Level up team to be able to address all inbound customer issues for managed k8s clusters

- **KR1:** 100% of Customer Engineers CKA Certified

  **Owner:** TBD

### O4: Implement PoC Process

- **KR1:** 100% of presales engagements have associated Discovery Agreement in place

  **Owner:** TBD

### O5: Supplier Quality & Standardization

Standardize supplier offerings and establish quality requirements to ensure consistent customer experience across all suppliers

**Note:** This objective was previously joint with Cluster Ops but is now fully owned by Customer Engineering following the Cluster Ops and Platform Ops integration. Customer Engineering has full accountability for supplier quality and standardization.

- **KR1:** Define and publish Supplier Technical Requirements document

  - Document mandatory technical capabilities: managed k8s or SLURM on k8s (zero bare metal exceptions)
  - Specify infrastructure requirements: network topology, storage, monitoring/observability access, incident response SLAs
  - Define handover checklist: what Fluidstack needs from suppliers at cluster turnup (credentials, monitoring endpoints, escalation paths)
  - Approval from Cluster Ops and Customer Engineering leadership

  **Owner:** Customer Engineering Lead

- **KR2:** Establish Supplier Quality Dashboard

  - Real-time dashboard showing per-supplier metrics: uptime %, incident response time, deployment success rate, FSH coverage, ticket resolution time
  - Automated data collection from Jira, FSH, deployment tooling (no manual updates)
  - Red/Yellow/Green status indicators for each supplier against SLA thresholds
  - Dashboard accessible to Sales, Customer Engineering, and leadership

  **Owner:** Customer Engineering Lead

- **KR3:** Migrate all suppliers to standardized offerings by end of Q1

  - 100% of new deployments use managed k8s or SLURM on k8s (enforcement via deployment tooling)
  - Existing bare metal SLURM clusters identified with migration plan by Feb 15
  - All active suppliers acknowledged Supplier Technical Requirements (signed attestation or contract amendment)

  **Owner:** Customer Engineering Lead

- **KR4:** Supplier scorecard integrated into presales process

  - PoC/Discovery Agreement template includes supplier quality check (reference to dashboard)
  - Sales team trained on supplier quality metrics and how to communicate to customers
  - 100% of Q1 presales engagements reference supplier quality in customer-facing materials

  **Owner:** Customer Engineering Lead, Sales Ops
