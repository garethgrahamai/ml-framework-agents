# DS-01 Agent Template Reference

## Quick Reference

This document maps all templates the DS-01 agent can generate, organized by assessment phase.

---

## Template Overview

| # | Template | Phase | Agent Mode | When to Use |
|---|----------|-------|------------|-------------|
| 1 | Use Case Submission | Initiation | Assessment Generator | New use case intake |
| 2 | Project Charter | Initiation | Assessment Generator | Formalizing approved initiatives |
| 3 | Stakeholder Map | Initiation | Assessment Generator | Identifying key players |
| 4 | Discovery Session Summary | Discovery | Discovery Mode | After running discovery session |
| 5 | Stakeholder Interview Summary | Discovery | Discovery Mode | After each stakeholder interview |
| 6 | Decision Definition | Discovery | Assessment Generator | Formalizing the decision to improve |
| 7 | Data Inventory | Data Assessment | Assessment Generator | Cataloging available data |
| 8 | Data Quality Assessment | Data Assessment | Assessment Generator | Evaluating data fitness |
| 9 | Data Viability Assessment | Data Assessment | Assessment Generator | Overall data readiness verdict |
| 10 | Label/Target Analysis | Data Assessment | Assessment Generator | Deep dive on outcome variable |
| 11 | Baseline Analysis | Baseline & Formulation | Assessment Generator | Establishing non-ML benchmarks |
| 12 | ML Problem Formulation | Baseline & Formulation | Assessment Generator | Translating business to ML task |
| 13 | Algorithm Selection Rationale | Baseline & Formulation | Assessment Generator | Justifying algorithm choice |
| 14 | Risk Register | Risk & Decision | Red Flag Scanner | Documenting all identified risks |
| 15 | Go/No-Go Memo | Risk & Decision | Assessment Generator | Final viability recommendation |
| 16 | POC Plan | Planning | Assessment Generator | Planning proof of concept |
| 17 | Success Criteria Definition | Planning | Assessment Generator | Defining measurable success |
| 18 | Model Evaluation Report | Post-Implementation | Assessment Generator | Documenting model performance |
| 19 | Production Readiness Checklist | Post-Implementation | Assessment Generator | Pre-deployment verification |
| 20 | Runbook | Post-Implementation | Assessment Generator | Operational documentation |
| 21 | Post-Implementation Review | Post-Implementation | Assessment Generator | Retrospective analysis |

---

## Templates by Agent Mode

### Discovery Mode
Primary output from running discovery sessions.

| Template | Purpose |
|----------|---------|
| Discovery Session Summary | Captures findings from structured discovery |
| Stakeholder Interview Summary | Documents individual stakeholder perspectives |

### Red Flag Scanner Mode
Primary output from risk analysis.

| Template | Purpose |
|----------|---------|
| Risk Register | Comprehensive risk documentation with mitigations |

### Assessment Generator Mode
Generates formal assessment documents from collected information.

| Template | Purpose |
|----------|---------|
| All 21 templates | Any document can be requested by name |

---

## Templates by Phase

### Phase 1: Initiation
*Starting a new ML assessment*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| Use Case Submission | Business problem, initial value estimate, sponsor | Day 0 - Intake |
| Project Charter | Scope, objectives, stakeholders, timeline | After initial approval |
| Stakeholder Map | Influence/interest matrix, engagement strategy | Before discovery begins |

### Phase 2: Discovery
*Understanding the decision and context*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| Discovery Session Summary | Decision, data landscape, red flags, initial impression | After discovery session |
| Stakeholder Interview Summary | Individual insights, concerns, success definitions | After each interview |
| Decision Definition | Decision statement, error costs, actionability test | After discovery complete |

### Phase 3: Data Assessment
*Evaluating data viability*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| Data Inventory | Sources, access status, key fields, gaps | During data exploration |
| Data Quality Assessment | Completeness, accuracy, timeliness scores | After data profiling |
| Data Viability Assessment | Overall readiness score, risks, recommendation | Data gate decision |
| Label/Target Analysis | Target definition, quality scores, proxy analysis | When labels are complex |

### Phase 4: Baseline & Formulation
*Establishing benchmarks and ML approach*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| Baseline Analysis | Current state, rule-based options, ML target | Before ML development |
| ML Problem Formulation | Task type, input/output spec, evaluation design | Before modeling begins |
| Algorithm Selection Rationale | Candidates evaluated, selection criteria, decision | Before POC |

### Phase 5: Risk & Decision
*Final viability assessment*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| Risk Register | All risks by category, severity, mitigation plans | Ongoing, finalized at gate |
| Go/No-Go Memo | Recommendation, key findings, conditions | Viability gate decision |

### Phase 6: Planning (If Viable)
*Planning the proof of concept*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| POC Plan | Hypothesis, scope, data plan, timeline, resources | After Go decision |
| Success Criteria Definition | Must-have/should-have criteria, measurement plan | Before POC begins |

### Phase 7: Post-Implementation
*After model is built*

| Template | Key Contents | Typical Timing |
|----------|--------------|----------------|
| Model Evaluation Report | Performance metrics, fairness analysis, recommendation | After POC/training |
| Production Readiness Checklist | Deployment prerequisites, blockers | Before go-live |
| Runbook | Operations guide, playbooks, contacts | At deployment |
| Post-Implementation Review | Actual vs expected, lessons learned, ROI | 30/90 days post-launch |

---

## How to Request Templates

When using the DS-01 agent, request templates by name:

```
"Generate a Use Case Submission for [context]"
"Create the Decision Definition based on our discovery"
"Draft a Data Viability Assessment"
"Write the Go/No-Go Memo"
"Prepare a POC Plan"
"Create the Runbook for this system"
```

The agent will:
1. Use available context from the conversation
2. Fill in what it can from discovery/analysis
3. Mark gaps as `[TBD]` for follow-up
4. Provide rationale for assessments

---

## Template Dependencies

Some templates build on others. Recommended order:

```
Use Case Submission
       │
       ▼
Project Charter ◄──── Stakeholder Map
       │
       ▼
Discovery Session Summary
       │
       ├──► Decision Definition
       │
       ▼
Data Inventory
       │
       ▼
Data Quality Assessment
       │
       ▼
Data Viability Assessment ◄──── Label/Target Analysis
       │
       ▼
Baseline Analysis
       │
       ▼
Risk Register ──────────────────┐
       │                        │
       ▼                        ▼
ML Problem Formulation    Go/No-Go Memo
       │                        │
       ▼                        │
Algorithm Selection             │
       │                        │
       ▼◄───────────────────────┘
POC Plan ◄──── Success Criteria Definition
       │
       ▼
Model Evaluation Report
       │
       ▼
Production Readiness Checklist
       │
       ▼
Runbook
       │
       ▼
Post-Implementation Review
```

---

## Minimum Viable Assessment

For quick assessments, these 5 templates cover the essentials:

| Template | Purpose |
|----------|---------|
| Discovery Session Summary | Understand the problem |
| Decision Definition | Clarify what ML would improve |
| Data Viability Assessment | Can we build this? |
| Baseline Analysis | What's the bar to beat? |
| Go/No-Go Memo | Final recommendation |

---

## Full Assessment

For comprehensive assessments, use all 21 templates following the phase sequence.
