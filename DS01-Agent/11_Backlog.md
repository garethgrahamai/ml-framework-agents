# DS-01 Agent Backlog

## Purpose

Track known gaps, incomplete items, and future enhancements for the DS-01 agent system.

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
| GAP-001 | Framework folder verification | TODO | Need to verify all referenced framework paths actually exist in ML-Decision-Enablement-Framework |
| GAP-002 | Template alignment check | TODO | Verify 21 agent templates match format of 09_DELIVERABLES_AND_TEMPLATES in framework |
| GAP-003 | AE-01 agent creation | TODO | Need equivalent agent system for ML-System-Implementation-Framework |
| GAP-004 | Handoff documentation | TODO | Detailed DS-01 → AE-01 handoff process and artifacts |

### Medium Priority

| ID | Item | Status | Notes |
|----|------|--------|-------|
| GAP-005 | Example conversations expansion | TODO | Only 4 examples, need more edge cases |
| GAP-006 | Error handling guidance | TODO | What agent does when stuck or user unresponsive |
| GAP-007 | Multi-session continuity | TODO | How agent resumes across sessions beyond status file |
| GAP-008 | Validation prompts | TODO | Prompts for agent to validate its own outputs |

### Low Priority

| ID | Item | Status | Notes |
|----|------|--------|-------|
| GAP-009 | Localization | TODO | Currently English-only |
| GAP-010 | Accessibility guidance | TODO | How to use with screen readers, etc. |
| GAP-011 | Performance benchmarks | TODO | Expected response times, token usage |

---

## Future Enhancements

### Planned Features

| ID | Feature | Priority | Notes |
|----|---------|----------|-------|
| ENH-001 | Confidence scoring | Medium | Agent provides confidence level with assessments |
| ENH-002 | Comparison mode | Low | Compare two use cases side-by-side |
| ENH-003 | Portfolio view | Low | Summarize status across multiple assessments |
| ENH-004 | Integration hooks | Medium | Webhooks/API patterns for integration |
| ENH-005 | Metrics dashboard prompt | Medium | Generate dashboard specs from assessment |

### Exploration Ideas

| ID | Idea | Status | Notes |
|----|------|--------|-------|
| EXP-001 | Fine-tuned model | Exploring | Would need training data from real assessments |
| EXP-002 | RAG integration | Exploring | Pull from framework docs dynamically |
| EXP-003 | Voice interface | Not started | Discovery sessions via voice |
| EXP-004 | Slack/Teams bot | Not started | Agent accessible via chat platforms |

---

## Incomplete Items

### Prompts

| File | What's Missing |
|------|----------------|
| `05_Example_Conversations.md` | Only 4 examples; need edge cases, failures, conditional scenarios |

### Documentation

| File | What's Missing |
|------|----------------|
| `07_Operator_Guide.md` | Troubleshooting section, FAQ |
| `08_Output_Structure.md` | Example of a completed workspace |
| `09_Framework_Reference.md` | Verified paths (need to check framework structure) |

### Integration

| Area | What's Missing |
|------|----------------|
| Framework sync | Process to keep agent aligned when framework updates |
| AE-01 handoff | Formal handoff checklist and protocol |
| Escalation back | Detailed escalation triggers and process |

---

## Technical Debt

| ID | Issue | Impact | Notes |
|----|-------|--------|-------|
| DEBT-001 | Template duplication | Medium | Templates exist in agent AND in framework 09_DELIVERABLES - single source of truth needed |
| DEBT-002 | Hardcoded paths | Low | Framework paths are hardcoded, could break if framework restructured |
| DEBT-003 | No test cases | Medium | No way to verify agent behaves correctly |

---

## Questions to Resolve

| ID | Question | Status |
|----|----------|--------|
| Q-001 | Should agent read framework docs at runtime or have them embedded? | Open |
| Q-002 | How to handle framework updates - manual sync or automated? | Open |
| Q-003 | Should there be a "lite" version of the agent with fewer templates? | Open |
| Q-004 | What's the minimum context window needed for full agent prompt? | Open |
| Q-005 | Should agent modes be separate prompts or one unified prompt with mode switching? | Open |

---

## Recently Completed

*Move items here when done, then transfer to Changelog*

| ID | Item | Completed | Notes |
|----|------|-----------|-------|
| - | Initial agent system | 2026-01-03 | v0.1.0 |
| - | 21 templates | 2026-01-03 | v0.2.0 |
| - | Operator guide | 2026-01-03 | v0.3.0 |
| - | Output structure | 2026-01-03 | v0.4.0 |
| - | Framework integration | 2026-01-03 | v0.5.0 |
| - | Changelog + Backlog | 2026-01-03 | v0.6.0 |

---

## Next Actions

Priority items for next work session:

1. [ ] Verify framework paths exist (GAP-001)
2. [ ] Check template alignment (GAP-002)
3. [ ] Expand example conversations (GAP-005)
4. [ ] Create AE-01 agent equivalent (GAP-003)
