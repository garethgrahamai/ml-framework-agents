# AE-01 Agent Template Reference

## Quick Reference

This document maps all templates the AE-01 agent can generate, organized by implementation phase.

---

## Template Overview

| # | Template | Phase | Agent Mode | When to Use |
|---|----------|-------|------------|-------------|
| 1 | Handoff Review | Handoff | System Prompt | Receiving work from DS-01 |
| 2 | Architecture Design | Architecture | Architecture Mode | System design |
| 3 | Component Specification | Architecture | Architecture Mode | Detailed component design |
| 4 | Technology Selection | Architecture | Architecture Mode | Justifying tech choices |
| 5 | Implementation Plan | Implementation | Implementation Mode | Planning the build |
| 6 | Task Breakdown | Implementation | Implementation Mode | Sprint/task planning |
| 7 | Code Review Checklist | Implementation | Implementation Mode | Quality gates |
| 8 | Deployment Plan | Deployment | Deployment Mode | Planning rollouts |
| 9 | Rollback Procedure | Deployment | Deployment Mode | Failure recovery |
| 10 | A/B Test Specification | Deployment | Deployment Mode | Experiment design |
| 11 | Monitoring Specification | Operations | Operations Mode | What to monitor |
| 12 | Alerting Configuration | Operations | Operations Mode | Alert setup |
| 13 | Runbook | Operations | Operations Mode | Operational procedures |
| 14 | Incident Report | Operations | Operations Mode | Post-incident documentation |
| 15 | Retraining Plan | Lifecycle | System Prompt | Model refresh strategy |

---

## Templates by Agent Mode

### Architecture Mode
| Template | Purpose |
|----------|---------|
| Architecture Design | Overall system design |
| Component Specification | Detailed component specs |
| Technology Selection | Tech choice rationale |

### Implementation Mode
| Template | Purpose |
|----------|---------|
| Implementation Plan | Overall build plan |
| Task Breakdown | Sprint/task decomposition |
| Code Review Checklist | Quality standards |

### Deployment Mode
| Template | Purpose |
|----------|---------|
| Deployment Plan | Rollout strategy |
| Rollback Procedure | Recovery plan |
| A/B Test Specification | Experiment design |

### Operations Mode
| Template | Purpose |
|----------|---------|
| Monitoring Specification | Metrics and dashboards |
| Alerting Configuration | Alert rules |
| Runbook | Operational procedures |
| Incident Report | Post-incident docs |

---

## Templates by Phase

### Phase 1: Handoff
*Receiving work from DS-01*

| Template | Key Contents | Timing |
|----------|--------------|--------|
| Handoff Review | Verification of DS-01 artifacts, gap analysis | Start of engagement |

### Phase 2: Architecture
*Designing the ML system*

| Template | Key Contents | Timing |
|----------|--------------|--------|
| Architecture Design | Patterns, components, diagrams | After handoff review |
| Component Specification | Detailed specs per component | After architecture approval |
| Technology Selection | Tech choices with rationale | During architecture |

### Phase 3: Implementation
*Building the system*

| Template | Key Contents | Timing |
|----------|--------------|--------|
| Implementation Plan | Phases, timeline, resources | Before build starts |
| Task Breakdown | Tasks, dependencies, estimates | Each sprint/iteration |
| Code Review Checklist | Quality gates, standards | During development |

### Phase 4: Deployment
*Rolling out to production*

| Template | Key Contents | Timing |
|----------|--------------|--------|
| Deployment Plan | Strategy, steps, verification | Before deploy |
| Rollback Procedure | Triggers, steps, recovery | Before deploy |
| A/B Test Specification | Hypothesis, metrics, duration | If running experiment |

### Phase 5: Operations
*Running the system*

| Template | Key Contents | Timing |
|----------|--------------|--------|
| Monitoring Specification | Metrics, dashboards, SLOs | Before go-live |
| Alerting Configuration | Alert rules, thresholds, escalation | Before go-live |
| Runbook | Procedures, troubleshooting | Before go-live |
| Incident Report | Timeline, root cause, actions | After incidents |

### Phase 6: Lifecycle
*Managing over time*

| Template | Key Contents | Timing |
|----------|--------------|--------|
| Retraining Plan | Triggers, cadence, validation | Post-deployment |

---

## Template Dependencies

Recommended document flow:

```
DS-01 Handoff
     │
     ▼
Handoff Review
     │
     ▼
Architecture Design ◄──── Technology Selection
     │
     ▼
Component Specification
     │
     ▼
Implementation Plan
     │
     ▼
Task Breakdown (iterative)
     │
     ▼
Code Review Checklist (ongoing)
     │
     ▼
Deployment Plan ◄──── Rollback Procedure
     │
     ├──► A/B Test Specification (if testing)
     │
     ▼
Monitoring Specification
     │
     ▼
Alerting Configuration
     │
     ▼
Runbook
     │
     ▼
[Production]
     │
     ├──► Incident Report (as needed)
     │
     ▼
Retraining Plan
```

---

## Minimum Viable Implementation

For quick implementations, these 5 templates cover essentials:

| Template | Purpose |
|----------|---------|
| Handoff Review | Verify we have what we need |
| Architecture Design | Document the system design |
| Deployment Plan | Plan the rollout |
| Runbook | Enable operations |
| Monitoring Specification | Ensure observability |

---

## How to Request Templates

When using the AE-01 agent, request templates by name:

```
"Review the DS-01 handoff for UC-001"
"Create an Architecture Design"
"Generate the Deployment Plan"
"Write the Runbook"
"Document this incident"
```

The agent will use available context and note any gaps.
