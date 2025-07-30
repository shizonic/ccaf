---
description: "Orchestrates context creation for projects, features, and tech stacks"
agents: [Analyzer, Researcher]
---

# Context Command

## Usage
```
/context
/context Analyse AI chat backend integration
/context Research OpenAI Chat API documentation
```

## Available Agents
- **Analyzer**: Reviews code quality, identifies issues, provides optimization recommendations
- **Researcher**: Investigates technologies, analyzes documentation, gathers technical information
- **Product Manager**: Creates PRDs, translates business requirements into technical specifications
- **Architect**: Designs system architectures, creates implementation plans from PRDs
- **Writer**: Creates technical documentation, API references, user guides

## Task
You are an orchestrator. Your ONLY role is to delegate tasks to appropriate subagents based on $ARGUMENTS. Spawn agents in parallel when beneficial.

## Process

1. **Analyze Request**
   Ultrathink about $ARGUMENTS to determine required outputs:
   - PRD creation needed?
   - Documentation research needed?
   - Architecture/implementation plan needed?
   - Task breakdown needed?
   - Codebase analysis needed? (brownfield projects)
   - Simple topic research only?

2. **Execute**
   Based on analysis, delegate to appropriate agents:
   
   | Output Needed | Agent(s) | File Location |
   |--------------|----------|---------------|
   | PRD | Product Manager | `docs/prd.md` |
   | Documentation Research | Researcher | `docs/[topic].md` |
   | Codebase Analysis | Analyzer | `docs/codebase-analysis.md` |
   | Architecture & Implementation | Architect | `docs/plan.md` |
   | Task Breakdown | Product Manager + Architect | `docs/tasks.md` |
   | Topic Research | Researcher | `docs/[topic].md` |

3. **Coordinate**
   - Run agents in parallel when their outputs are independent
   - Run sequentially when outputs depend on each other (e.g., implementation plan requires PRD)
   - Ensure all outputs are written to appropriate files