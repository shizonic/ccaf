---
description: Complete development workflow from initial research through implementation to testing and documentation
agents: researcher, analyzer, product-manager, architect, fullstack-developer, backend-developer, frontend-developer, tester, writer, git-specialist
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to build from start to finish?"

## Flow
```
CONTEXT → PLAN → IMPLEMENT → VALIDATE
   ↓        ↓         ↓          ↓
Research  Design    Build    Test+Doc
```

## Orchestration

### PHASE 1: CONTEXT GATHERING

**researcher** │ **analyzer** (parallel):
- Researcher: External docs, APIs, best practices for $ARGUMENTS
- Analyzer: Existing codebase analysis, patterns, constraints

Orchestrator synthesizes findings and writes `docs/context-summary.md`

### PHASE 2: PLANNING

**product-manager** (receives context):
- Create PRD with user stories
- Break into 1-3 day tasks
- Define acceptance criteria

**architect** (receives PRD):
- Technical architecture design
- Component diagrams (Mermaid)
- API contracts and data models
- Ultrathink for complex decisions

Orchestrator writes `docs/project-plan.md` with combined outputs

### PHASE 3: IMPLEMENTATION  

Orchestrator determines approach based on $ARGUMENTS complexity:

**Option A - Unified**: 
- **fullstack-developer** implements everything

**Option B - Parallel**:
- **backend-developer** │ **frontend-developer** work simultaneously
- Orchestrator ensures API contracts align

All developers MUST follow KISS, DRY, YAGNI principles

### PHASE 4: VALIDATION & DOCUMENTATION

**tester** │ **analyzer** (parallel):
- Tester: Create/run comprehensive tests (MUST NOT fix failures)
- Analyzer: Code quality, security, performance review

Then spawn 3 parallel **writer** agents:
- `docs/test-report.md` - Test results and coverage
- `docs/technical-docs.md` - Architecture and API docs  
- `docs/user-guide.md` - Usage instructions

### PHASE 5: FINALIZATION

**git-specialist** (if version control needed):
- Semantic commits for all changes
- Create PR with summaries
- Link to documentation

## Usage

> /workflow implement JWT authentication
> /workflow create a blog platform
> /workflow add real-time notifications
> /workflow build complete SaaS application