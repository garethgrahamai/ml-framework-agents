# AE-01 Agent Backlog

## Purpose

Track known gaps, incomplete items, and future enhancements for the AE-01 agent system.

---

## Status Key

| Status | Meaning |
|--------|---------|
| `TODO` | Not started |
| `IN PROGRESS` | Currently being worked on |
| `BLOCKED` | Waiting on something |
| `DONE` | Completed (move to changelog) |

---

## Known Gaps

### High Priority

| ID | Item | Status | Notes |
|----|------|--------|-------|
| GAP-001 | Framework folder verification | TODO | Verify referenced paths exist in ML-System-Implementation-Framework |
| GAP-002 | Template content expansion | TODO | Templates are outlined but need full field definitions |
| GAP-003 | DS-01 handoff process | TODO | Need formal handoff checklist and validation |
| GAP-004 | Example conversations | TODO | No example conversations yet (unlike DS-01) |

### Medium Priority

| ID | Item | Status | Notes |
|----|------|--------|-------|
| GAP-005 | Escalation back to DS-01 | TODO | Detailed escalation triggers and process |
| GAP-006 | Error handling guidance | TODO | What agent does when stuck |
| GAP-007 | Multi-session continuity | TODO | How agent resumes across sessions |
| GAP-008 | Technology-specific guidance | TODO | Framework is tech-agnostic, may need concrete examples |

### Low Priority

| ID | Item | Status | Notes |
|----|------|--------|-------|
| GAP-009 | Integration examples | TODO | Real-world tool integrations (Airflow, MLflow, etc.) |
| GAP-010 | Cost estimation guidance | TODO | How to estimate infrastructure costs |
| GAP-011 | Team sizing guidance | TODO | How to size implementation teams |

---

## Future Enhancements

### Planned Features

| ID | Feature | Priority | Notes |
|----|---------|----------|-------|
| ENH-001 | Code generation mode | Medium | Generate boilerplate code for common patterns |
| ENH-002 | Cost calculator | Low | Estimate infrastructure costs |
| ENH-003 | Timeline generator | Medium | Auto-generate timelines from task breakdown |
| ENH-004 | Architecture diagram generator | Medium | Mermaid/PlantUML diagram generation |
| ENH-005 | Incident pattern matching | Low | Suggest solutions based on past incidents |

### Exploration Ideas

| ID | Idea | Status | Notes |
|----|------|--------|-------|
| EXP-001 | Integration with MLOps tools | Exploring | Direct integration with MLflow, Airflow, etc. |
| EXP-002 | Automated deployment scripts | Not started | Generate deployment scripts from plans |
| EXP-003 | Monitoring dashboard templates | Exploring | Grafana/Datadog dashboard JSON |
| EXP-004 | Runbook automation | Not started | Runbook steps as executable scripts |

---

## Incomplete Items

### Mode Prompts

| File | What's Missing |
|------|----------------|
| `02_Architecture_Mode_Prompt.md` | More architecture patterns, cloud-specific guidance |
| `03_Implementation_Mode_Prompt.md` | Testing strategy details, CI/CD guidance |
| `04_Deployment_Mode_Prompt.md` | Cloud-specific deployment patterns |
| `05_Operations_Mode_Prompt.md` | Tool-specific monitoring setup |

### Documentation

| File | What's Missing |
|------|----------------|
| (None yet) | Example conversations needed |
| `07_Operator_Guide.md` | Troubleshooting section, FAQ |
| `08_Output_Structure.md` | Example of a completed workspace |

### Integration

| Area | What's Missing |
|------|----------------|
| DS-01 handoff | Formal handoff validation checklist |
| Escalation | Detailed escalation criteria and process |
| Framework sync | Process to keep agent aligned when framework updates |

---

## Technical Debt

| ID | Issue | Impact | Notes |
|----|-------|--------|-------|
| DEBT-001 | No template expansion | Medium | Templates are outlines, not full documents |
| DEBT-002 | Hardcoded paths | Low | Framework paths are hardcoded |
| DEBT-003 | No test cases | Medium | No way to verify agent behaves correctly |
| DEBT-004 | Missing example conversations | High | Hard to understand expected behavior |

---

## Questions to Resolve

| ID | Question | Status |
|----|----------|--------|
| Q-001 | How much implementation detail should agent provide vs. deferring to framework? | Open |
| Q-002 | Should agent recommend specific tools or stay technology-agnostic? | Open |
| Q-003 | How to handle multi-model systems (ensemble, pipeline)? | Open |
| Q-004 | What level of code generation is appropriate? | Open |
| Q-005 | How to version agent alongside framework updates? | Open |

---

## Dependencies on DS-01

| Dependency | Status | Notes |
|------------|--------|-------|
| Handoff artifact format | Aligned | Using same document templates |
| Use Case ID scheme | Aligned | UC-### format shared |
| Escalation path | Documented | In both agent systems |
| Workspace structure | Compatible | Separate but linked folders |

---

## Recently Completed

*Move items here when done, then transfer to Changelog*

| ID | Item | Completed | Notes |
|----|------|-----------|-------|
| - | Initial agent system | 2026-01-03 | v0.1.0 |

---

## Next Actions

Priority items for next work session:

1. [ ] Create example conversations (GAP-004)
2. [ ] Verify framework paths exist (GAP-001)
3. [ ] Define formal DS-01 handoff checklist (GAP-003)
4. [ ] Expand template content (GAP-002)
