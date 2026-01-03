# DS-01 Output Structure

## Purpose

When DS-01 generates documents, they need a home. This defines the folder structure for each use case assessment.

---

## Workspace Structure

For each use case, create this folder structure:

```
[UC-###_Use_Case_Name]/
│
├── 00_Status.md                          # Current status and next steps
│
├── 01_Initiation/
│   ├── Use_Case_Submission.md
│   ├── Project_Charter.md
│   └── Stakeholder_Map.md
│
├── 02_Discovery/
│   ├── Discovery_Session_Summary.md
│   ├── Decision_Definition.md
│   └── Interviews/
│       ├── Interview_[Stakeholder1].md
│       └── Interview_[Stakeholder2].md
│
├── 03_Data_Assessment/
│   ├── Data_Inventory.md
│   ├── Data_Quality_Assessment.md
│   ├── Data_Viability_Assessment.md
│   └── Label_Target_Analysis.md
│
├── 04_Baseline_Formulation/
│   ├── Baseline_Analysis.md
│   ├── ML_Problem_Formulation.md
│   └── Algorithm_Selection_Rationale.md
│
├── 05_Risk_Decision/
│   ├── Risk_Register.md
│   └── Go_NoGo_Memo.md
│
├── 06_Planning/
│   ├── POC_Plan.md
│   └── Success_Criteria_Definition.md
│
└── 07_Post_Implementation/
    ├── Model_Evaluation_Report.md
    ├── Production_Readiness_Checklist.md
    ├── Runbook.md
    └── Post_Implementation_Review.md
```

---

## Status File Template

Each workspace has a `00_Status.md` file tracking progress:

```markdown
# Assessment Status: [Use Case Name]

## Quick Info
| Field | Value |
|-------|-------|
| Use Case ID | UC-### |
| Name | [Name] |
| Sponsor | [Name] |
| DS-01 Operator | [Name] |
| Created | [Date] |
| Last Updated | [Date] |

## Current Status
**Stage:** [Triage / Intake / Discovery / Data Assessment / Baseline / Risk / Decision / Planning / Complete]

**Status:** [In Progress / Blocked / On Hold / Complete]

**Next Action:** [What needs to happen next]

## Document Checklist

### Initiation
- [ ] Use Case Submission
- [ ] Project Charter
- [ ] Stakeholder Map

### Discovery
- [ ] Discovery Session Summary
- [ ] Decision Definition
- [ ] Stakeholder Interviews (list names)

### Data Assessment
- [ ] Data Inventory
- [ ] Data Quality Assessment
- [ ] Data Viability Assessment
- [ ] Label/Target Analysis

### Baseline & Formulation
- [ ] Baseline Analysis
- [ ] ML Problem Formulation
- [ ] Algorithm Selection Rationale

### Risk & Decision
- [ ] Risk Register
- [ ] Go/No-Go Memo

### Planning
- [ ] POC Plan
- [ ] Success Criteria Definition

### Post-Implementation
- [ ] Model Evaluation Report
- [ ] Production Readiness Checklist
- [ ] Runbook
- [ ] Post-Implementation Review

## Decision Log
| Date | Decision | Rationale | Made By |
|------|----------|-----------|---------|
| [Date] | [Decision] | [Why] | [Who] |

## Notes
[Running notes, context, reminders]
```

---

## Workspace Location

All use case workspaces live under a common parent:

```
DS01_Assessments/
├── UC-001_Customer_Churn_Prediction/
├── UC-002_Demand_Forecasting/
├── UC-003_Fraud_Detection/
└── _Templates/                    # Empty structure for new assessments
    ├── 00_Status.md
    ├── 01_Initiation/
    ├── 02_Discovery/
    │   └── Interviews/
    ├── 03_Data_Assessment/
    ├── 04_Baseline_Formulation/
    ├── 05_Risk_Decision/
    ├── 06_Planning/
    └── 07_Post_Implementation/
```

---

## Initialization Routine

When starting a new assessment, the agent should:

### Step 1: Create Workspace
```
Create folder: DS01_Assessments/UC-[###]_[Name]/
Copy structure from: DS01_Assessments/_Templates/
```

### Step 2: Initialize Status
Create `00_Status.md` with:
- Use Case ID
- Name
- Sponsor (if known)
- Operator name
- Today's date
- Stage: "Triage"

### Step 3: Confirm Location
Tell the operator:
```
Workspace created at: DS01_Assessments/UC-[###]_[Name]/
All documents will be saved to this location.
Current stage: Triage
```

---

## Document Naming Conventions

| Template | Filename |
|----------|----------|
| Use Case Submission | `Use_Case_Submission.md` |
| Project Charter | `Project_Charter.md` |
| Stakeholder Map | `Stakeholder_Map.md` |
| Discovery Session Summary | `Discovery_Session_Summary.md` |
| Stakeholder Interview | `Interview_[Name].md` |
| Decision Definition | `Decision_Definition.md` |
| Data Inventory | `Data_Inventory.md` |
| Data Quality Assessment | `Data_Quality_Assessment.md` |
| Data Viability Assessment | `Data_Viability_Assessment.md` |
| Label/Target Analysis | `Label_Target_Analysis.md` |
| Baseline Analysis | `Baseline_Analysis.md` |
| ML Problem Formulation | `ML_Problem_Formulation.md` |
| Algorithm Selection Rationale | `Algorithm_Selection_Rationale.md` |
| Risk Register | `Risk_Register.md` |
| Go/No-Go Memo | `Go_NoGo_Memo.md` |
| POC Plan | `POC_Plan.md` |
| Success Criteria Definition | `Success_Criteria_Definition.md` |
| Model Evaluation Report | `Model_Evaluation_Report.md` |
| Production Readiness Checklist | `Production_Readiness_Checklist.md` |
| Runbook | `Runbook.md` |
| Post-Implementation Review | `Post_Implementation_Review.md` |

---

## Agent Startup Prompt Addition

Add this to the system prompt for workspace awareness:

```
## Workspace Management

At the start of each session, you must:

1. **Identify the workspace**: Ask which use case you're working on, or if this is new
2. **For new use cases**:
   - Generate a Use Case ID (UC-###)
   - Create the workspace folder structure
   - Initialize the status file
   - Confirm the workspace location to the operator
3. **For existing use cases**:
   - Read the 00_Status.md file
   - Confirm current stage and next action
   - Ask what the operator wants to do this session
4. **When generating documents**:
   - Save to the correct subfolder
   - Update the status file checklist
   - Note the file location in your response

Workspace root: DS01_Assessments/
```
