---
description: Complete development workflow from initial research through implementation to testing and documentation with maximum parallelization
agents: researcher, analyzer, product-manager, architect, fullstack-developer, backend-developer, frontend-developer, tester, writer, git-specialist
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to build from start to finish?"

## Flow
```
CONTEXT → PLAN → IMPLEMENT → VALIDATE → DOCUMENT
   ↓        ↓         ↓          ↓          ↓
Parallel  Parallel  Parallel  Parallel   Synthesis
```

## Orchestration

### PHASE 1: CONTEXT GATHERING

Spawn multiple **researcher** agents (by topic):
- Documentation research
- Best practices research  
- Security guidelines
- Performance patterns
Each writes `docs/research-[topic].md`

Spawn multiple **analyzer** agents (by area):
- Frontend analysis
- Backend analysis
- Database analysis
- Infrastructure review
Each writes `docs/analysis-[area].md`

### PHASE 2: PLANNING

Spawn multiple **product-manager** agents (by feature):
- Each creates PRD for assigned features
- Each writes `docs/prd-[feature].md`

Spawn multiple **architect** agents (by system):
- Frontend architecture
- Backend architecture
- Data architecture
- Security architecture
Each writes `docs/architecture-[system].md`

**writer** → `docs/master-plan.md`
- Synthesizes all plans
- Creates implementation roadmap

### PHASE 3: IMPLEMENTATION  

Orchestrator identifies non-conflicting work units:

Spawn multiple **backend-developer** agents:
- Service A, Service B, Service C...
- Each handles independent modules

Spawn multiple **frontend-developer** agents:
- Component A, Component B, Component C...
- Each handles independent UI parts

OR multiple **fullstack-developer** agents for feature-based splits

### PHASE 4: VALIDATION

Spawn multiple **tester** agents:
- Unit testing (per module)
- Integration testing
- E2E testing
- Performance testing
Each writes `docs/test-[type].md`

Spawn multiple **analyzer** agents:
- Security analysis
- Performance analysis
- Code quality checks
Each writes `docs/validation-[type].md`

### PHASE 5: FINAL DOCUMENTATION

Spawn multiple **writer** agents:
- User guide
- API documentation
- Deployment guide
- Developer documentation

**git-specialist** (if needed):
- Create comprehensive commits
- Generate final PR

## Usage

> /workflow implement JWT authentication
> /workflow create a blog platform
> /workflow add real-time notifications
> /workflow build complete SaaS application