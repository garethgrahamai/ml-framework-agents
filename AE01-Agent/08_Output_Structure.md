# AE-01 Output Structure

## Purpose

When AE-01 generates documents, they need a home. This defines the folder structure for each implementation project.

---

## Workspace Structure

For each implementation project, create this folder structure:

```
[UC-###_Project_Name]/
│
├── 00_Status.md                          # Current status and next steps
│
├── 01_Handoff/
│   ├── GoNoGo_Memo.md                    # From DS-01
│   ├── POC_Plan.md                       # From DS-01
│   ├── Data_Viability_Assessment.md      # From DS-01
│   ├── Baseline_Analysis.md              # From DS-01
│   ├── Risk_Register.md                  # From DS-01
│   └── Handoff_Review.md                 # AE-01 verification
│
├── 02_Architecture/
│   ├── Architecture_Design.md
│   ├── Component_Specifications/
│   │   ├── Data_Pipeline.md
│   │   ├── Feature_Store.md
│   │   ├── Model_Training.md
│   │   └── Serving_Infrastructure.md
│   └── Technology_Selection.md
│
├── 03_Implementation/
│   ├── Implementation_Plan.md
│   ├── Task_Breakdowns/
│   │   ├── Sprint_01.md
│   │   ├── Sprint_02.md
│   │   └── ...
│   └── Code_Review_Checklist.md
│
├── 04_Deployment/
│   ├── Deployment_Plan.md
│   ├── Rollback_Procedure.md
│   └── AB_Test_Specification.md
│
├── 05_Operations/
│   ├── Monitoring_Specification.md
│   ├── Alerting_Configuration.md
│   ├── Runbook.md
│   └── Incidents/
│       ├── INC_001_[Date]_[Title].md
│       └── ...
│
└── 06_Lifecycle/
    ├── Retraining_Plan.md
    ├── Version_History.md
    └── Sunset_Criteria.md
```

---

## Status File Template

Each workspace has a `00_Status.md` file tracking progress:

```markdown
# Implementation Status: [Project Name]

## Quick Info
| Field | Value |
|-------|-------|
| Use Case ID | UC-### |
| Name | [Name] |
| DS-01 Handoff Date | [Date] |
| AE-01 Operator | [Name] |
| Current Phase | [Phase] |
| Last Updated | [Date] |

## Current Status
**Phase:** [Handoff / Architecture / Implementation / Deployment / Operations / Maintenance]

**Status:** [In Progress / Blocked / On Hold / Complete]

**Next Action:** [What needs to happen next]

## Document Checklist

### Handoff (from DS-01)
- [ ] Go/No-Go Memo received
- [ ] POC Plan received
- [ ] Data Viability Assessment received
- [ ] Baseline Analysis received
- [ ] Risk Register received
- [ ] Handoff Review completed

### Architecture
- [ ] Architecture Design
- [ ] Component Specifications
- [ ] Technology Selection

### Implementation
- [ ] Implementation Plan
- [ ] Task Breakdowns (ongoing)
- [ ] Code Review Checklist

### Deployment
- [ ] Deployment Plan
- [ ] Rollback Procedure
- [ ] A/B Test Specification (if applicable)

### Operations
- [ ] Monitoring Specification
- [ ] Alerting Configuration
- [ ] Runbook

### Lifecycle
- [ ] Retraining Plan
- [ ] Version History
- [ ] Sunset Criteria

## Key Metrics
| Metric | Target | Current |
|--------|--------|---------|
| [Primary metric] | [Target] | [Value] |
| [Secondary metric] | [Target] | [Value] |

## Risks & Issues
| ID | Issue | Status | Owner |
|----|-------|--------|-------|
| [ID] | [Issue] | [Status] | [Name] |

## Decision Log
| Date | Decision | Rationale | Made By |
|------|----------|-----------|---------|
| [Date] | [Decision] | [Why] | [Who] |

## Notes
[Running notes, context, reminders]
```

---

## Workspace Location

All implementation workspaces live under a common parent:

```
AE01_Implementations/
├── UC-001_Customer_Churn_Prediction/
├── UC-002_Demand_Forecasting/
├── UC-003_Fraud_Detection/
└── _Templates/                    # Empty structure for new projects
    ├── 00_Status.md
    ├── 01_Handoff/
    ├── 02_Architecture/
    │   └── Component_Specifications/
    ├── 03_Implementation/
    │   └── Task_Breakdowns/
    ├── 04_Deployment/
    ├── 05_Operations/
    │   └── Incidents/
    └── 06_Lifecycle/
```

---

## Relationship to DS-01 Workspace

```
DS01_Assessments/                      AE01_Implementations/
├── UC-001_Customer_Churn/             ├── UC-001_Customer_Churn/
│   ├── 05_Risk_Decision/              │   ├── 01_Handoff/
│   │   └── Go_NoGo_Memo.md ──────────────► Go_NoGo_Memo.md (copied)
│   └── ...                            │   └── ...
```

**Use the same UC-### ID** to link assessment and implementation.

---

## Initialization Routine

When starting a new implementation, the agent should:

### Step 1: Get Use Case ID
Ask: "What's the Use Case ID from DS-01?" (e.g., UC-001)

### Step 2: Create Workspace
```
Create folder: AE01_Implementations/UC-[###]_[Name]/
Copy structure from: AE01_Implementations/_Templates/
```

### Step 3: Copy Handoff Artifacts
Copy from DS-01 workspace to `01_Handoff/`:
- Go_NoGo_Memo.md
- POC_Plan.md
- Data_Viability_Assessment.md
- Baseline_Analysis.md
- Risk_Register.md

### Step 4: Initialize Status
Create `00_Status.md` with:
- Use Case ID
- Name
- Handoff date
- Operator name
- Phase: "Handoff"

### Step 5: Confirm Location
Tell the operator:
```
Workspace created at: AE01_Implementations/UC-[###]_[Name]/
DS-01 artifacts copied to 01_Handoff/
Current phase: Handoff Review
```

---

## Document Naming Conventions

| Template | Filename |
|----------|----------|
| Handoff Review | `Handoff_Review.md` |
| Architecture Design | `Architecture_Design.md` |
| Component Spec | `[Component_Name].md` |
| Technology Selection | `Technology_Selection.md` |
| Implementation Plan | `Implementation_Plan.md` |
| Task Breakdown | `Sprint_[##].md` |
| Code Review Checklist | `Code_Review_Checklist.md` |
| Deployment Plan | `Deployment_Plan.md` |
| Rollback Procedure | `Rollback_Procedure.md` |
| A/B Test Specification | `AB_Test_Specification.md` |
| Monitoring Specification | `Monitoring_Specification.md` |
| Alerting Configuration | `Alerting_Configuration.md` |
| Runbook | `Runbook.md` |
| Incident Report | `INC_[###]_[Date]_[Title].md` |
| Retraining Plan | `Retraining_Plan.md` |
