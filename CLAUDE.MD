# CLAUDE.MD

## Repository Overview

This is a management information repository for Fluidstack's Engineering, Product, and Infrastructure organization. It contains:

- **OKRs**: Quarterly objectives and key results for organization-level and team-level goals
- **Team Information**: Structure, responsibilities, and details for each functional team
- **Organization**: Tracks strategic initiatives, deployment plans, and operational excellence metrics

## Repository Structure

```
.
├── okrs/                    # Quarterly OKRs organized by year/quarter
│   └── 2026/
│       └── q1/
│           ├── org_level.md       # Top-level org OKRs (5 key objectives)
│           ├── summary.md         # Summary/overview of Q1 goals
│           ├── customer_success.md
│           ├── infra.md
│           ├── procurement.md
│           └── software.md
└── teams/                   # Team structure and information
    ├── customer_success.md
    ├── infra.md
    ├── procurement.md
    ├── product.md
    ├── program.md
    └── software.md
```

## Key Context

### Organization Focus

Fluidstack is a GPU cloud infrastructure company transitioning from scrappy execution to scaled, repeatable operations. The organization is:

- Executing major deployments (Stream, CB3) with 500+ machines
- Building ClusterMAX Platinum for industry-leading operational excellence
- Validating TPU-based inference as a new business line
- Scaling team from current size with aggressive hiring (16-18 new members in Q1 2026)
- Operating across 10+ specialized teams

### Five Organizational Priorities (Q1 2026)

1. **Execute Stream/CB3 deployments** - Prove deployment engine for scale
2. **Build ClusterMAX Platinum foundation** - Industry-leading operational excellence
3. **Validate TPU-based inference business** - New product line and competitive advantage
4. **Improve customer experience and supplier quality** - Standards and processes for scale
5. **Build world-class engineering team and culture** - Capacity, retention, and AI adoption

### Teams

- **Cluster & Platform Ops**: Kubernetes, automation, auto-remediation
- **Inference**: TPU workloads, model optimization, new product line
- **Customer Engineering**: Customer deployments, support, quality
- **Infra Compute**: Hardware deployment, GPU/TPU operations
- **Networking**: Network infrastructure, connectivity
- **DCIM**: Data center infrastructure management
- **Infrastructure Deployment**: Deployment automation and tooling
- **Observability**: Monitoring, alerting, metrics
- **Procurement**: Vendor relationships, purchasing systems
- **Software**: Platform software and tooling
- **Product**: Product strategy and roadmap
- **Program**: Cross-functional coordination

## Working with This Repository

### When updating OKRs:

- Maintain the three-level hierarchy: organization → team → individual KRs
- Ensure team OKRs explicitly roll up to org-level objectives
- Keep objectives as H3 headings, KRs as bullet points
- Include "Why this matters" context for each objective
- Update both org_level.md and relevant team files

### When updating team information:

- Keep team structure files in sync with reality
- Document changes in responsibilities or team membership
- Track hiring progress against targets

### Formatting conventions:

- Organization OKRs: Objectives as H3, KRs as bullets
- Team OKRs: Same formatting pattern for consistency
- Use markdown for all documentation
- Include context and rationale, not just metrics

## Questions to Ask Me

When working on OKRs or team structure, consider asking:

- "Should I check if team OKRs still roll up correctly to org objectives?"
- "Do you want me to analyze progress toward Q1 goals?"
- "Should I identify any gaps between org objectives and team coverage?"
- "Do you need help drafting OKRs for the next quarter?"
- "Should I validate that all teams have documented OKRs?"

## Common Tasks

### Reviewing OKR alignment
Check that each team's OKRs explicitly state which org-level objectives they support

### Updating progress
Update KR metrics and status as milestones are achieved

### Quarterly planning
Draft new OKRs based on previous quarter learnings and upcoming priorities

### Gap analysis
Identify which org objectives lack sufficient team-level support

## Repository Maintenance

- Keep README.md in sync with structure changes
- Archive completed quarters as new ones begin
- Maintain consistent formatting across all OKR files
- Document significant pivots or strategy changes
