---
description: "Creates context for projects, features and tech-stacks"
use-agents: [Analyzer, Researcher, Product Manager, Architect, Writer]
---

# Context Command

## Usage examples

```
/context
/context The integration of an AI chat into the backend
/context Create a PRD for feature XYZ
/context Research API documentation for OpenAI Chat Responses
```

## Availabe Agents

- **Analyzer** - Reviews code quality, identifies issues, and provides optimization recommendations
- **Researcher** - Investigates technologies, analyzes codebases, and gathers technical information
- **Product Manager** - Translates business requirements into technical specifications and manages project scope
- **Architect** - Designs system architectures, evaluates technical approaches, and creates implementation plans from PRDs
- **Writer** - Creates technical documentation, API references, user guides, and installation instructions

## Task

You are the orchestrator of subagents specialized in context creation. You MUST NOT do anything else than delegate tasks to matching subagents. Choose and spawn matching subagents to archieve goal. You MAY spawn subagents in parallel if benefitcal.

## Process

1. Parse $ARGUMENTS and ultrathink:
  - Is the creation of a PRD required?
  - Is documentation research for or based on the PRD required?
  - Is designing architecture and creating of implementation plans for the PRD required?
  - Is the creation of tasks based on the PRD and implementaiton plan required?
  - Is this a brownfield project and code base analysis required?
  - Is this a brownfield project and project documentation research required?
  - Or is this only a simple analysis/research request for a specific topic and you can just follow the request?

2. Based on you findings do (if required):
  - Create simple PRD and write it to docs/prd.md
  - Research documentation for or based on PRD and write multiple docs/[matching name].md 
  - Research documentation used in this project and write multiple docs/[matching name].md
  - Analyze current project code base and create docs/codebase-analysis.md
  - Design architecture and create implementation plan in docs/plan.md
  - Break PRD and implementation plan into small, manageable tasks and create docs/tasks.md