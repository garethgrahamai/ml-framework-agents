# DS-01 Operator Guide

## Purpose

This guide tells you **which agent to run**, **when to run it**, and **who needs to be in the room**.

You (the operator) orchestrate the DS-01 agent through the viability assessment process.

---

## Quick Reference

| Stage | Agent Mode | Who's Present | Duration | Output |
|-------|------------|---------------|----------|--------|
| Triage | Red Flag Scanner | Operator alone | 10 min | Quick risk assessment |
| Intake | Assessment Generator | Operator alone | 15 min | Use Case Submission |
| Discovery | Discovery Mode | Operator + Business Stakeholder | 30-60 min | Discovery Session Summary |
| Stakeholder Interviews | Discovery Mode | Operator + Individual Stakeholder | 30 min each | Interview Summary |
| Data Assessment | Assessment Generator | Operator + Data Owner (optional) | 30-60 min | Data Viability Assessment |
| Baseline Definition | Assessment Generator | Operator + Domain Expert | 30 min | Baseline Analysis |
| Risk Consolidation | Red Flag Scanner | Operator alone | 20 min | Risk Register |
| Decision Gate | Assessment Generator | Operator alone (then present to stakeholders) | 30 min | Go/No-Go Memo |
| Planning | Assessment Generator | Operator + Technical Lead | 30 min | POC Plan |

---

## Detailed Workflow

### Stage 1: Triage

**When:** A new ML idea or request arrives

**Purpose:** Quick check for obvious blockers before investing time

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Red Flag Scanner |
| **Operator** | Data Scientist, Analyst, or PM |
| **Who's Present** | Operator alone |
| **Input Needed** | Brief description of the idea (even a paragraph works) |
| **Duration** | 10 minutes |
| **Output** | Risk assessment with severity ratings |

**What to do:**
1. Paste the use case description into Red Flag Scanner
2. Review the flags identified
3. If HARD STOPS found → Stop, communicate to requestor
4. If no hard stops → Proceed to Intake

**Decision Point:**
- HARD STOPS present → Decline with explanation
- HIGH severity flags → Proceed with caution, note concerns
- Low/Medium only → Proceed normally

---

### Stage 2: Intake

**When:** Idea passes triage, needs formal documentation

**Purpose:** Create structured record of the request

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Assessment Generator |
| **Operator** | Data Scientist or Analyst |
| **Who's Present** | Operator alone (may need to contact requestor for gaps) |
| **Input Needed** | Original request, any context gathered |
| **Duration** | 15 minutes |
| **Output** | Use Case Submission document |

**What to do:**
1. Request "Generate a Use Case Submission"
2. Provide context from the original request
3. Fill any gaps marked [TBD] by contacting requestor
4. Get sponsor confirmation

**Decision Point:**
- Sponsor confirmed → Proceed to Discovery
- No sponsor → Cannot proceed, need business ownership

---

### Stage 3: Discovery Session

**When:** Use case has sponsor, ready for deep dive

**Purpose:** Extract the decision, understand constraints, identify risks

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Discovery Mode |
| **Operator** | Data Scientist (facilitating) |
| **Who's Present** | Operator + Business Stakeholder(s) |
| **Input Needed** | Use Case Submission, stakeholder availability |
| **Duration** | 30-60 minutes |
| **Output** | Discovery Session Summary |

**Who to invite:**
- Primary business stakeholder (required)
- Subject matter expert (recommended)
- Data owner (optional, helpful)

**What to do:**
1. Schedule meeting with stakeholders
2. Open Discovery Mode agent
3. Let agent guide the questioning
4. Capture responses in real-time
5. After session: generate Discovery Session Summary

**Key questions the agent will cover:**
1. What decision will this improve?
2. Who makes this decision today?
3. What happens when it's wrong?
4. What data exists?
5. How do you know outcomes?
6. What's changed recently?

**Decision Point:**
- Clear decision identified → Continue assessment
- No clear decision → More discovery needed or stop

---

### Stage 4: Stakeholder Interviews (If Needed)

**When:** Multiple stakeholders with different perspectives, or need deeper context

**Purpose:** Capture individual viewpoints, identify alignment/misalignment

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Discovery Mode |
| **Operator** | Data Scientist or Analyst |
| **Who's Present** | Operator + ONE stakeholder at a time |
| **Input Needed** | Discovery Session Summary, specific questions |
| **Duration** | 30 minutes per interview |
| **Output** | Stakeholder Interview Summary (one per person) |

**Who to interview:**
- Decision makers
- End users of the prediction
- Data owners
- Domain experts
- Anyone with different success definition

**What to do:**
1. Review Discovery Session Summary for gaps
2. Prepare focused questions for each stakeholder
3. Run interview using Discovery Mode
4. Generate Interview Summary after each

**Decision Point:**
- Stakeholders aligned → Proceed
- Stakeholders misaligned → Escalate, get alignment before continuing

---

### Stage 5: Data Assessment

**When:** Discovery complete, decision is clear

**Purpose:** Evaluate whether data can support the ML use case

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Assessment Generator |
| **Operator** | Data Scientist |
| **Who's Present** | Operator alone, consult Data Owner as needed |
| **Input Needed** | Discovery findings, access to data catalog/systems |
| **Duration** | 30-60 minutes (may span days if data exploration needed) |
| **Output** | Data Inventory, Data Quality Assessment, Data Viability Assessment |

**What to do:**
1. Generate Data Inventory (catalog what exists)
2. Profile actual data if possible
3. Generate Data Quality Assessment
4. Generate Data Viability Assessment (verdict)
5. If labels are complex, generate Label/Target Analysis

**Who to consult:**
- Data engineers (for access, pipelines)
- Data owners (for quality, history)
- Business users (for field meanings)

**Decision Point:**
- Data viable → Continue to baseline
- Data not viable → Stop or identify remediation path
- Conditionally viable → Document conditions, get sign-off

---

### Stage 6: Baseline Definition

**When:** Data assessment complete and viable

**Purpose:** Establish what non-ML approaches can achieve

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Assessment Generator |
| **Operator** | Data Scientist |
| **Who's Present** | Operator + Domain Expert |
| **Input Needed** | Discovery findings, current process knowledge |
| **Duration** | 30 minutes |
| **Output** | Baseline Analysis |

**Who to consult:**
- Experienced practitioners who do this today
- Business analysts who know current rules
- Anyone who can articulate "how we decide this now"

**What to do:**
1. Interview domain expert about current approach
2. Identify simple rules that might work
3. Generate Baseline Analysis
4. Define the bar ML must beat

**Decision Point:**
- Baseline leaves room for ML improvement → Continue
- Baseline already very good → Question if ML adds enough value

---

### Stage 7: Risk Consolidation

**When:** Data and baseline assessments complete

**Purpose:** Compile all identified risks into formal register

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Red Flag Scanner |
| **Operator** | Data Scientist |
| **Who's Present** | Operator alone |
| **Input Needed** | All prior findings, discovery notes, data assessment |
| **Duration** | 20 minutes |
| **Output** | Risk Register |

**What to do:**
1. Compile all findings from prior stages
2. Run through Red Flag Scanner with full context
3. Generate formal Risk Register
4. Assign owners and mitigations

---

### Stage 8: Decision Gate

**When:** All assessments complete

**Purpose:** Make and document the Go/No-Go recommendation

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Assessment Generator |
| **Operator** | Data Scientist |
| **Who's Present** | Operator alone (drafting), then stakeholders (presenting) |
| **Input Needed** | All prior documents |
| **Duration** | 30 minutes to draft, meeting to present |
| **Output** | Go/No-Go Memo |

**What to do:**
1. Review all findings
2. Generate Go/No-Go Memo
3. Schedule decision meeting
4. Present to stakeholders
5. Get sign-off

**Who needs to approve:**
- Business sponsor (required)
- Technical lead (required)
- Executive sponsor (for large initiatives)

**Decision Point:**
- GO → Proceed to Planning
- NO-GO → Document learnings, close
- CONDITIONAL → Document conditions, get commitment

---

### Stage 9: Planning (If GO)

**When:** Go decision made

**Purpose:** Plan the proof of concept

| Aspect | Detail |
|--------|--------|
| **Agent Mode** | Assessment Generator |
| **Operator** | Data Scientist + Technical Lead |
| **Who's Present** | Operator + Technical Lead + Business Owner |
| **Input Needed** | All prior documents, resource availability |
| **Duration** | 30-60 minutes |
| **Output** | POC Plan, Success Criteria Definition |

**What to do:**
1. Generate POC Plan
2. Generate Success Criteria Definition
3. Review with stakeholders
4. Get sign-off
5. Hand off to implementation team (AE-01)

---

## Handoff to AE-01

After DS-01 delivers a GO with POC Plan, the handoff to AE-01 (Implementation) includes:

**Documents to transfer:**
- Go/No-Go Memo
- POC Plan
- Success Criteria Definition
- Data Viability Assessment
- Baseline Analysis
- Risk Register

**Key information to communicate:**
- What decision ML will improve
- What baseline to beat
- Known data constraints
- Accepted risks
- Success criteria and thresholds

---

## Summary: The Operator's Checklist

| # | Stage | Mode | Who | Got It? |
|---|-------|------|-----|---------|
| 1 | Triage | Red Flag Scanner | Alone | ☐ |
| 2 | Intake | Assessment Generator | Alone | ☐ |
| 3 | Discovery | Discovery Mode | + Business Stakeholder | ☐ |
| 4 | Interviews | Discovery Mode | + Individual Stakeholders | ☐ |
| 5 | Data Assessment | Assessment Generator | + Data Owner (consult) | ☐ |
| 6 | Baseline | Assessment Generator | + Domain Expert | ☐ |
| 7 | Risk Consolidation | Red Flag Scanner | Alone | ☐ |
| 8 | Decision Gate | Assessment Generator | Alone → Present to all | ☐ |
| 9 | Planning | Assessment Generator | + Tech Lead + Business | ☐ |
