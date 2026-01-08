# Engineering Organization OKRs - Q1 2026

## Overview

These organization-level OKRs represent the highest-priority outcomes for the entire Engineering, Product, and Infrastructure organization in Q1 2026. All team-level OKRs (Cluster & Platform Ops, Inference, Customer Engineering, Infra Compute, Networking, DCIM, Infrastructure Deployment, Observability, Procurement) roll up into these five objectives.

Q1 2026 is a critical quarter where Fluidstack transitions from scrappy execution to scaled, repeatable operations. Success requires tight coordination across 10+ teams, aggressive hiring (16-18 new team members), and rapid automation development.

---

## O1: Execute Stream/CB3 deployments successfully and prove deployment engine for 2026+ scale

**Why this matters:** Stream/CB3 are the proving ground for repeatable, scaled operations. Success here validates processes, tooling, and team capacity for future growth.

### KR1: Stream sub-pod deployed successfully with 576 machines operational and <5% failure rate requiring manual intervention

### KR2: CB3 deployment readiness validated: runbooks tested, tooling load-tested for 2x capacity

### KR3: Lab 2.0 environment operational by Mar 31 with 1 rack V7, 1 Deschutes CDU, VAST cluster (site selected Jan 31, migration plan Feb 15, equipment delivered Mar 15)

### KR4: Procurement systems and partnerships operational: Zip integration complete (vendor onboarding <7 days, PO/invoice tracking by Feb 15), Atlas procurement integrated (<24hr latency), sell-through relationships established (Dell/SMC, Arista, Commscope by Feb 15), off-site integration program operational (WWT/Computacenter/Hyve by Feb 28)

**Roll-up from:** Infra Compute O1/O2, Networking O1/O2, DCIM O1/O2/O3, Infrastructure Deployment O1, Procurement O1/O2, Cluster & Platform Ops O1

---

## O2: Build ClusterMAX Platinum foundation and industry-leading operational excellence

**Why this matters:** ClusterMAX Platinum differentiates Fluidstack in the market. Q1 establishes the foundation (auto-remediation, security, DX) for mid-2026 certification.

### KR1: Auto-remediation operational: MTTR <15min (software) / <4hrs (hardware) with ≥85% automated failure resolution

### KR2: Security posture measurably improved: ≥90% Critical CVEs remediated within SLA, incident response capability tested (tabletop exercise), ≥80% clusters hardened to CIS benchmarks

### KR3: Customer experience improvements delivered: management cluster migration complete, NVSentinel on 90% of clusters, Kubernetes Add-On System operational, TPU v7 workload scheduling validated

### KR4: Observability foundation established: FSH on 100% of clusters reducing page volume by 40%, unified observability architecture documented, Mimir costs reduced to <$0.025/host/h

### KR5: Deployment velocity demonstrates scalability: GPU deployment rate ≥1000 GPUs/hr, sub-pod deployment time ≤10 days rack-ready to workload-ready

**Roll-up from:** Cluster & Platform Ops O2/O3/O4/O5, Observability Team O1/O2/O3/O4, Infra Compute O1

---

## O3: Validate TPU-based inference business and maintain strategic positioning

**Why this matters:** Inference on TPU represents a new product line and strategic competitive advantage. Q1 proves technical and commercial viability.

### KR1: Technical capability demonstrated: ≥2 reasoning models benchmarked on v7 hardware with competitive performance, customer deployment (Cursor/Perplexity) with <10% degradation

### KR2: Business model validated: LOIs from 3-5 tier-1 customers, $/token pricing defined with 50%+ margin, commitment for 1-2 v7 pods secured

### KR3: Core inference architecture validated (testing, not production): K8s on TPUs operational, disaggregated prefill/decode prototype functional, KV cache architecture tested

**Roll-up from:** Inference O1/O2/O3

---

## O4: Improve customer experience and supplier quality standards

**Why this matters:** As Fluidstack scales, consistent customer experience and supplier quality are essential for retention and growth. Q1 establishes scalable processes.

### KR1: Supplier quality standardized: Technical Requirements published and acknowledged by all active suppliers, 100% new deployments on managed k8s/SLURM on k8s (zero bare metal exceptions)

### KR2: Supplier quality dashboard operational: real-time metrics (uptime, incident response, deployment success, FSH coverage) with automated data collection, integrated into presales process

### KR3: Customer Engineering operational excellence: P0-only paging implemented, 100% clusters trackable in Jira, PoC process with Discovery Agreements operational

### KR4: go/top40 customers aligned to product roadmap with clear delivery commitments and predictable execution

**Roll-up from:** Customer Engineering O1/O2/O3/O4/O5

---

## O5: Build world-class engineering team and culture

**Why this matters:** 2026+ scale requires team capacity, retention, continuous learning, and leveraging AI to increase productivity. Q1 builds the foundation.

### KR1: Hiring executing at target velocity: 100% of hiring targets met (16-18 hires across Procurement +4, Infra +4, Networking +2, Software +4-6), interview to offer latency <2 weeks

### KR2: Team retention strong: <10% voluntary attrition across engineering organization

### KR3: Professional development and growth: 100% of team members complete ≥1 professional development activity (conference attendance, certification like CKA, training course)

### KR4: AI tooling adopted and created: ≥3 custom AI tools/agents built and operational (e.g., deployment assistant, troubleshooting copilot, runbook generator), existing AI tools (Copilot, Claude, etc.) adopted across engineering workflows

**Roll-up from:** All team hiring KRs, Customer Engineering O3 (CKA certification)

---

## Priority Framework

If forced to rank these objectives:

**P0 (Must succeed):** O1 - Stream/CB3 execution
- Everything else depends on proving we can deploy at scale

**P1 (Critical for differentiation):** O2 - ClusterMAX Platinum foundation
- This is what makes Fluidstack industry-leading vs commodity

**P2 (Strategic bet):** O3 - Inference validation
- New revenue stream, but failure is survivable in Q1

**P2 (Essential for scale):** O4 - Customer experience and supplier quality
- Enables retention and consistent quality as we grow

**P1 (Enabler for all):** O5 - Team and culture
- Without the right team, nothing else succeeds

---

## Success Criteria

At the end of Q1 2026, success looks like:
- Stream sub-pod operational with lessons learned captured for CB3
- ClusterMAX Platinum roadmap on track with foundational capabilities proven
- Inference business model validated with customer commitments
- Supplier quality measurably improving with automated tracking
- Team capacity built with strong retention and continuous learning culture
