# ML Framework Agents

> AI agents that operationalise ML viability assessment and implementation. Turn methodology into guided workflow.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework](https://img.shields.io/badge/type-agentic--ai-purple.svg)]()

---

## Overview

This repo contains two AI agent systems that operationalise the ML Decision and Implementation frameworks. These agents act as AI-powered assistants that guide users through the complete ML project lifecycle.

| Agent | Role | Framework | Phase |
|-------|------|-----------|-------|
| **DS-01** | ML Viability Architect | ML Viability Framework | Pre-investment assessment |
| **AE-01** | ML Implementation Engineer | ML Implementation Framework | Post-viability build |

---

## The Problem

Methodologies are only useful if people follow them. Most framework documentation:
- Gets read once and forgotten
- Requires expertise to apply correctly
- Doesn't adapt to specific contexts
- Has no memory of project state

These agents solve that by embedding the methodology into an AI assistant that:
- Guides users through each step
- Asks the right questions at the right time
- Maintains state across sessions
- Produces structured outputs

---

## The Two-Agent Model

```
                    ML PROJECT LIFECYCLE

┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   IDEA ──► DS-01 ──► GO/NO-GO ──► AE-01 ──► PRODUCTION         │
│            │                       │                            │
│            ▼                       ▼                            │
│      Is this viable?         Build & deploy                     │
│                                                                 │
│            │                       │                            │
│            └───── ESCALATION ◄─────┘                            │
│                  (if issues found)                              │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**DS-01** assesses whether an ML use case is viable before investment. It asks the hard questions, identifies red flags, and delivers a clear GO / NO-GO / CONDITIONAL recommendation.

**AE-01** takes over after a GO decision. It designs architecture, plans implementation, guides deployment, and establishes operations.

If AE-01 discovers viability issues during implementation, it escalates back to DS-01.

---

## Agent Architecture

### File-Based Memory System

Since AI agents don't have persistent memory across sessions, we use a **file-based memory system** that gives each agent:

| Memory Type | Files | Purpose |
|-------------|-------|---------|
| **Identity** | `00_Overview.md`, `01_System_Prompt.md` | Who am I? What do I do? |
| **Knowledge** | `09_Framework_Reference.md` | What methodology do I follow? |
| **Capabilities** | Template Reference, Mode Prompts | What can I produce? |
| **Process** | `07_Operator_Guide.md` | How do I work? With whom? |
| **State** | `08_Output_Structure.md`, workspace Status files | Where are we? |
| **History** | `10_Changelog.md` | What changed? |
| **Future** | `11_Backlog.md` | What's incomplete? What's next? |

At the start of each session, the agent reads its memory files to understand:
- Its identity and role
- The current state of work
- What needs to happen next

After each session, the agent updates status files to persist progress.

---

## Folder Structure

```
ml-framework-agents/
│
├── README.md                    
│
├── DS01-Agent/                  ← Viability Assessment Agent
│   ├── 00_Overview.md           Status + file index
│   ├── 01_System_Prompt.md      Core agent prompt
│   ├── 02_Discovery_Mode_Prompt.md
│   ├── 03_Red_Flag_Scanner_Prompt.md
│   ├── 04_Assessment_Generator_Prompt.md
│   ├── 05_Example_Conversations.md
│   ├── 06_Template_Reference.md
│   ├── 07_Operator_Guide.md
│   ├── 08_Output_Structure.md
│   ├── 09_Framework_Reference.md
│   ├── 10_Changelog.md
│   └── 11_Backlog.md
│
└── AE01-Agent/                  ← Implementation Agent
    ├── 00_Overview.md           Status + file index
    ├── 01_System_Prompt.md      Core agent prompt
    ├── 02_Architecture_Mode_Prompt.md
    ├── 03_Implementation_Mode_Prompt.md
    ├── 04_Deployment_Mode_Prompt.md
    ├── 05_Operations_Mode_Prompt.md
    ├── 06_Template_Reference.md
    ├── 07_Operator_Guide.md
    ├── 08_Output_Structure.md
    ├── 09_Framework_Reference.md
    ├── 10_Changelog.md
    └── 11_Backlog.md
```

---

## Agent Capabilities

### DS-01: Viability Architect

| Mode | Purpose | Key Outputs |
|------|---------|-------------|
| **Discovery Mode** | Run stakeholder sessions | Discovery Summary, Interview Notes |
| **Red Flag Scanner** | Analyse for risks | Risk Register, Warning Flags |
| **Assessment Generator** | Produce documents | Go/No-Go Memo, Viability Assessment |

**Primary outputs:** Use Case Submission, Decision Definition, Data Viability Assessment, Baseline Analysis, Go/No-Go Recommendation

### AE-01: Implementation Engineer

| Mode | Purpose | Key Outputs |
|------|---------|-------------|
| **Architecture Mode** | Design systems | Architecture Design, Component Specs |
| **Implementation Mode** | Plan builds | Implementation Plan, Task Breakdowns |
| **Deployment Mode** | Plan rollouts | Deployment Plan, Rollback Procedures |
| **Operations Mode** | Establish ops | Runbooks, Monitoring Specs |

**Primary outputs:** System Architecture, Deployment Plan, Runbook, Monitoring Specification

---

## Output Workspaces

Each agent generates documents into structured workspaces:

```
DS01_Assessments/                    AE01_Implementations/
├── UC-001_Customer_Churn/           ├── UC-001_Customer_Churn/
│   ├── 00_Status.md                 │   ├── 00_Status.md
│   ├── 01_Initiation/               │   ├── 01_Handoff/
│   ├── 02_Discovery/                │   ├── 02_Architecture/
│   ├── 03_Data_Assessment/          │   ├── 03_Implementation/
│   ├── 04_Baseline_Formulation/     │   ├── 04_Deployment/
│   ├── 05_Risk_Decision/            │   ├── 05_Operations/
│   ├── 06_Planning/                 │   └── 06_Lifecycle/
│   └── 07_Post_Implementation/      │
```

Both agents use the same **UC-###** identifier to link related work across the lifecycle.

---

## How to Use

### Option 1: Full Agent Mode
Copy the `01_System_Prompt.md` content into Claude, ChatGPT, or another LLM to get the complete agent experience with all capabilities.

### Option 2: Specialised Modes
Use individual mode prompts (Discovery, Red Flag Scanner, Architecture, etc.) for focused tasks without loading the full agent.

### Option 3: Agentic Workflow
Chain the agents together: DS-01 assessment → handoff document → AE-01 implementation.

### Operator Guides
See `07_Operator_Guide.md` in each agent folder for:
- Which mode to run for each task
- When to run it in the project lifecycle
- Who needs to be present (stakeholders, SMEs)

---

## Key Design Decisions

| Decision | Rationale |
|----------|-----------|
| **File-based memory** | Agents read/write files to persist state across sessions without external infrastructure |
| **Specialised modes** | Each agent has focused modes for different tasks—avoids prompt overload |
| **Structured outputs** | Documents go to defined folder locations for consistency and traceability |
| **Framework alignment** | Agents reference source frameworks, don't duplicate content |
| **Operator orchestration** | Humans decide when to run which mode—AI assists, doesn't replace judgment |
| **Clear handoffs** | DS-01 → AE-01 transition is documented and verified before proceeding |

---

## Human-AI Collaboration Model

These agents are designed for **human-in-the-loop** operation:

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   OPERATOR (Human)              AGENT (AI)                      │
│                                                                 │
│   • Decides which mode          • Asks structured questions     │
│   • Provides context            • Identifies red flags          │
│   • Validates outputs           • Generates documents           │
│   • Makes go/no-go calls        • Maintains state               │
│   • Owns the decision           • Suggests next steps           │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

The agent guides and produces; the human decides and approves.

---

## Source Frameworks

These agents operationalise two companion methodology frameworks:

| Framework | Purpose | Repo |
|-----------|---------|------|
| ML Viability Framework | Pre-investment assessment methodology | [ml-viability-framework](https://github.com/garethgrahamai/ml-viability-framework) |
| ML Implementation Framework | Production lifecycle methodology | [ml-implementation-framework](https://github.com/garethgrahamai/ml-implementation-framework) |

The agents reference these frameworks for deeper guidance and maintain alignment with their principles.

---

## What This Demonstrates

| Skill | Evidence |
|-------|----------|
| **Agentic AI design** | Multi-agent system with handoffs and escalation |
| **Prompt engineering** | System prompts, mode prompts, structured outputs |
| **State management** | File-based memory for LLM persistence |
| **Human-AI collaboration** | Operator orchestration model |
| **Systems thinking** | End-to-end lifecycle coverage |
| **Methodology design** | Turning frameworks into executable workflows |

---

## Status

This project is in active development. Core agent architecture and prompts are functional; template coverage is ongoing.

---

## Related Projects

- [AI Governance POC](https://github.com/garethgrahamai/ai-governance-poc) - Working RAG implementation with enterprise controls
- [ML Viability Framework](https://github.com/garethgrahamai/ml-viability-framework) - DS-01 source methodology
- [ML Implementation Framework](https://github.com/garethgrahamai/ml-implementation-framework) - AE-01 source methodology

---

## License

MIT License - see [LICENSE](LICENSE) for details.

---

## Author

**Gareth Graham**  
AI Strategy & Enablement | Enterprise Governance

[LinkedIn](https://linkedin.com/in/garethgrahamai) | [GitHub](https://github.com/garethgrahamai)

