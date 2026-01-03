# DS-01 Agent: AI-Powered Viability Assessment

## Status

| Attribute | Value |
|-----------|-------|
| Version | 0.6.0 |
| Last Updated | 2026-01-03 |
| Status | Development |
| Templates | 21 |
| Known Gaps | 11 (see Backlog) |

**Current State:** Functional agent with comprehensive templates, operator guide, output structure, and framework integration. Ready for testing.

**Next Priority:** Verify framework path alignment, expand example conversations, create AE-01 equivalent.

---

## Concept

An AI agent that embodies the DS-01 (ML Viability Architect) role, using the ML Decision Enablement Framework to guide users through structured viability assessments.

## What This Agent Does

1. **Runs discovery sessions** - Asks probing questions to extract constraints
2. **Identifies red flags** - Spots patterns that indicate viability concerns
3. **Applies expert judgment** - Recognizes composite data, delayed feedback, leakage risks
4. **Guides assessment** - Walks through data viability, baselines, risk
5. **Produces recommendations** - Drafts Go/No-Go memos with rationale

## What This Agent Doesn't Do

- Replace human judgment on final decisions
- Build models
- Access actual data systems
- Navigate organizational politics

## Files in This Folder

| File | Purpose |
|------|---------|
| `01_System_Prompt.md` | The core prompt that defines DS-01 behavior |
| `02_Discovery_Mode_Prompt.md` | Focused prompt for running discovery sessions |
| `03_Red_Flag_Scanner_Prompt.md` | Focused prompt for analyzing use cases for risks |
| `04_Assessment_Generator_Prompt.md` | Comprehensive prompt for generating all 21 assessment documents |
| `05_Example_Conversations.md` | Sample interactions showing expected behavior |
| `06_Template_Reference.md` | Complete template catalog with mapping to phases and modes |
| `07_Operator_Guide.md` | When to run which agent, with who present |
| `08_Output_Structure.md` | Workspace folder structure for assessment outputs |
| `09_Framework_Reference.md` | Links agent to source ML-Decision-Enablement-Framework |
| `10_Changelog.md` | Version history and changes |
| `11_Backlog.md` | Known gaps, incomplete items, future enhancements |

## How to Use

### Option 1: Full DS-01 Agent
Use `01_System_Prompt.md` for a complete viability architect experience.

### Option 2: Specialized Modes
Use the focused prompts (02-04) for specific tasks:
- Discovery session facilitation
- Red flag analysis
- Document generation

### Option 3: Build an Agentic Workflow
Chain the specialized prompts together in a multi-step workflow.
