# AE-01 Agent: AI-Powered ML Implementation Engineer

## Status

| Attribute | Value |
|-----------|-------|
| Version | 0.1.0 |
| Last Updated | 2026-01-03 |
| Status | Development |
| Templates | 15 |
| Known Gaps | See Backlog |

**Current State:** Initial agent structure created. Parallel to DS-01 agent system.

**Next Priority:** Verify framework path alignment, expand templates, test handoff from DS-01.

---

## Concept

An AI agent that embodies the AE-01 (ML Implementation Engineer) role, using the ML System Implementation Framework to guide users through building, deploying, and operating ML systems after viability is confirmed.

## What This Agent Does

1. **Designs ML architecture** - Translates requirements into technical design
2. **Plans implementation** - Creates sprint plans, task breakdowns
3. **Reviews quality** - Checks code, tests, documentation
4. **Prepares deployment** - Readiness checks, rollout planning
5. **Guides operations** - Monitoring, alerting, incident response
6. **Manages lifecycle** - Retraining, versioning, decommissioning

## What This Agent Doesn't Do

- Assess viability (that's DS-01's job)
- Make business decisions
- Write production code directly
- Replace human engineering judgment

## Relationship to DS-01

```
DS-01 (Viability)                    AE-01 (Implementation)
       │                                     │
       │ GO Decision                         │
       │ + POC Plan                          │
       │ + Success Criteria                  │
       │ + Data Viability                    │
       │ + Baseline Analysis                 │
       │ + Risk Register                     │
       ├────────────────────────────────────►│
       │                                     │
       │◄────────────────────────────────────┤
       │ Escalation if viability             │
       │ issues discovered                   │
```

## Files in This Folder

| File | Purpose |
|------|---------|
| `01_System_Prompt.md` | The core prompt that defines AE-01 behavior |
| `02_Architecture_Mode_Prompt.md` | Focused prompt for system design |
| `03_Implementation_Mode_Prompt.md` | Focused prompt for build planning |
| `04_Deployment_Mode_Prompt.md` | Focused prompt for release readiness |
| `05_Operations_Mode_Prompt.md` | Focused prompt for monitoring and incident response |
| `06_Template_Reference.md` | Complete template catalog with phase mapping |
| `07_Operator_Guide.md` | When to run which agent, with who present |
| `08_Output_Structure.md` | Workspace folder structure for implementation outputs |
| `09_Framework_Reference.md` | Links agent to source ML-System-Implementation-Framework |
| `10_Changelog.md` | Version history and changes |
| `11_Backlog.md` | Known gaps, incomplete items, future enhancements |

## How to Use

### Option 1: Full AE-01 Agent
Use `01_System_Prompt.md` for a complete implementation engineer experience.

### Option 2: Specialized Modes
Use the focused prompts (02-05) for specific tasks:
- Architecture and design
- Implementation planning
- Deployment preparation
- Operations and monitoring

### Option 3: Build an Agentic Workflow
Chain DS-01 → AE-01 for end-to-end ML project lifecycle.
