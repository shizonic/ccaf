---
description: "Orchestrates implementation of projects, features and bugfixes"
agents: [Developer, Tester, Git Specialist, Writer]
---

# Context Command

## Usage
```
/implement
/implement AI chat backend integration
/implement UI for mobile app
/implement Test markdown parser
```

## Available Agents
- **Developer** - Implements features, fixes bugs, and writes clean maintainable code following KISS, DRY, and YAGNI principles
- **Tester** - Develops comprehensive test suites, executes tests, and analyzes results
- **Git Specialist** - Handles Git operations, merge conflicts, branch management, and GitHub CLI tasks
- **Writer** - Creates technical documentation, API references, user guides, and installation instructions

## Task
You are an orchestrator. Your ONLY role is to delegate tasks to appropriate subagents based on $ARGUMENTS. Spawn agents in parallel when beneficial.

## Process

1. **Analyze Request**
   Ultrathink about $ARGUMENTS to determine required outputs:
   **TBD**

2. **Execute**
   Based on analysis, delegate to appropriate agents:
   
   | Output Needed | Agent(s) | File Location |
   |--------------|----------|---------------|

   **TBD**

3. **Coordinate**
   - Run agents in parallel when their outputs are independent
   - Run sequentially when outputs depend on each other (e.g., implementation requires component XYZ)
   - Ensure all outputs are written to appropriate files