# AE-01 Operator Guide

## Purpose

This guide tells you **which agent mode to run**, **when to run it**, and **who needs to be in the room**.

You (the operator) orchestrate the AE-01 agent through the implementation process.

---

## Quick Reference

| Stage | Agent Mode | Who's Present | Duration | Output |
|-------|------------|---------------|----------|--------|
| Handoff | System Prompt | Operator + DS-01 handoff | 30 min | Handoff Review |
| Architecture | Architecture Mode | Operator + Tech Lead | 1-2 hours | Architecture Design |
| Planning | Implementation Mode | Operator + Team | 1 hour | Implementation Plan |
| Sprint Work | Implementation Mode | Operator + Developers | Ongoing | Task Breakdowns |
| Pre-Deploy | Deployment Mode | Operator + DevOps | 1 hour | Deployment Plan |
| Go-Live | Deployment Mode | Operator + On-call | During deploy | Verification |
| Ops Setup | Operations Mode | Operator + SRE | 1-2 hours | Runbook, Monitoring |
| Incidents | Operations Mode | Operator + On-call | As needed | Incident Reports |

---

## Detailed Workflow

### Stage 1: Handoff Review

**When:** DS-01 delivers a GO decision

**Purpose:** Verify you have everything needed to implement

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Full AE-01 (System Prompt) |
| **Operator** | ML Engineer or Tech Lead |
| **Who's Present** | Operator, optionally DS-01 contact |
| **Input Needed** | DS-01 deliverables (Go/No-Go, POC Plan, etc.) |
| **Duration** | 30 minutes |
| **Output** | Handoff Review document |

**What to do:**
1. Gather all DS-01 artifacts
2. Review with AE-01 agent
3. Identify any gaps or concerns
4. If gaps: go back to DS-01
5. If complete: proceed to Architecture

**Decision Point:**
- All artifacts present and clear → Proceed
- Missing critical info → Request from DS-01
- Viability concerns discovered → Escalate to DS-01

---

### Stage 2: Architecture Design

**When:** Handoff complete, ready to design

**Purpose:** Create the technical architecture

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Architecture Mode |
| **Operator** | ML Engineer or Architect |
| **Who's Present** | Operator + Tech Lead + Infrastructure contact |
| **Input Needed** | Handoff artifacts, system constraints |
| **Duration** | 1-2 hours (may span sessions) |
| **Output** | Architecture Design, Component Specs |

**What to do:**
1. Define requirements (latency, scale, etc.)
2. Explore architecture patterns with agent
3. Make technology selections
4. Document the design
5. Get stakeholder review

**Who to consult:**
- Infrastructure/DevOps (for platform constraints)
- Security (for compliance requirements)
- Data Engineering (for pipeline integration)

**Decision Point:**
- Architecture approved → Proceed to Planning
- Concerns raised → Iterate on design

---

### Stage 3: Implementation Planning

**When:** Architecture approved

**Purpose:** Break down the work into actionable tasks

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Implementation Mode |
| **Operator** | Tech Lead or Project Manager |
| **Who's Present** | Operator + Development Team |
| **Input Needed** | Architecture docs, team capacity |
| **Duration** | 1 hour |
| **Output** | Implementation Plan, initial Task Breakdown |

**What to do:**
1. Review architecture with team
2. Break down into phases
3. Estimate effort
4. Assign ownership
5. Identify dependencies

**Decision Point:**
- Plan is feasible → Begin implementation
- Timeline unrealistic → Renegotiate scope or resources

---

### Stage 4: Sprint/Development Work

**When:** During active development

**Purpose:** Guide ongoing implementation

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Implementation Mode |
| **Operator** | Tech Lead |
| **Who's Present** | Operator + relevant developers |
| **Input Needed** | Current progress, blockers |
| **Duration** | Ongoing (sprint ceremonies) |
| **Output** | Updated Task Breakdowns, Code Review guidance |

**What to do:**
1. Update task status
2. Refine upcoming work
3. Address blockers with agent assistance
4. Ensure quality gates are met

---

### Stage 5: Pre-Deployment

**When:** Implementation complete, ready to deploy

**Purpose:** Plan the production rollout

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Deployment Mode |
| **Operator** | Tech Lead or DevOps Lead |
| **Who's Present** | Operator + DevOps + On-call |
| **Input Needed** | Completed system, deployment constraints |
| **Duration** | 1 hour |
| **Output** | Deployment Plan, Rollback Procedure |

**What to do:**
1. Verify all pre-deployment checks
2. Choose deployment strategy
3. Define rollback triggers
4. Set up monitoring for deploy
5. Notify stakeholders

**Decision Point:**
- All checks pass → Proceed to deploy
- Gaps identified → Fix before deploying

---

### Stage 6: Go-Live

**When:** During actual deployment

**Purpose:** Execute and verify deployment

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Deployment Mode |
| **Operator** | Deploying engineer |
| **Who's Present** | Operator + On-call + Stakeholders on standby |
| **Input Needed** | Deployment Plan |
| **Duration** | Deployment window |
| **Output** | Deployment verification |

**What to do:**
1. Execute deployment steps
2. Monitor metrics at each stage
3. Verify success criteria
4. Rollback if triggers hit
5. Communicate status

---

### Stage 7: Operations Setup

**When:** After successful deployment

**Purpose:** Establish operational readiness

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Operations Mode |
| **Operator** | SRE or ML Engineer |
| **Who's Present** | Operator + SRE/DevOps |
| **Input Needed** | Running system, SLO requirements |
| **Duration** | 1-2 hours |
| **Output** | Monitoring Spec, Alerting Config, Runbook |

**What to do:**
1. Configure monitoring
2. Set up alerting
3. Create/update runbook
4. Train on-call team
5. Handoff to operations

---

### Stage 8: Incident Response

**When:** Incidents occur

**Purpose:** Resolve issues and document learnings

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Operations Mode |
| **Operator** | On-call engineer |
| **Who's Present** | Incident responders |
| **Input Needed** | Symptoms, logs, metrics |
| **Duration** | As needed |
| **Output** | Incident Report, action items |

**What to do:**
1. Triage and mitigate
2. Investigate root cause
3. Document timeline
4. Create action items
5. Conduct retrospective

---

## Handoff from DS-01

When receiving work from DS-01, ensure you have:

| Document | Required | Purpose |
|----------|----------|---------|
| Go/No-Go Memo | Yes | Confirms viability |
| POC Plan or Success Criteria | Yes | Defines targets |
| Data Viability Assessment | Yes | Data constraints |
| Baseline Analysis | Yes | Bar to beat |
| Risk Register | Yes | Known risks |
| Decision Definition | Helpful | Business context |

**If missing documents:** Request from DS-01 before proceeding.

---

## Escalation to DS-01

Escalate back to DS-01 if you discover:

| Issue | Action |
|-------|--------|
| Data quality worse than assessed | Escalate - may affect viability |
| Baseline unbeatable | Escalate - core viability question |
| New regulatory concerns | Escalate - may be a hard stop |
| Labels unreliable | Escalate - fundamental data issue |

---

## Summary: The Operator's Checklist

| # | Stage | Mode | Who | Got It? |
|---|-------|------|-----|---------|
| 1 | Handoff | System Prompt | + DS-01 contact | ☐ |
| 2 | Architecture | Architecture Mode | + Tech Lead | ☐ |
| 3 | Planning | Implementation Mode | + Team | ☐ |
| 4 | Development | Implementation Mode | + Developers | ☐ |
| 5 | Pre-Deploy | Deployment Mode | + DevOps | ☐ |
| 6 | Go-Live | Deployment Mode | + On-call | ☐ |
| 7 | Ops Setup | Operations Mode | + SRE | ☐ |
| 8 | Incidents | Operations Mode | + Responders | ☐ |
