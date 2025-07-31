---
description: Transform ideas into comprehensive PRDs, technical architectures, and actionable development tasks through massive parallelization
agents: product-manager, architect, analyzer, writer
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to plan?"

## Flow
```
product-managers... │ architects... │ analyzers...
         ↓                ↓               ↓
   Direct writes    Direct writes   Direct writes
                         ↓
                    [writer synthesis]
```

## Orchestration

### Phase 1: Task Decomposition

Orchestrator splits $ARGUMENTS into parallel planning tasks:

**For product-managers** (by feature/module):
- User authentication
- Payment processing  
- Admin dashboard
- API endpoints
- Mobile features

**For architects** (by system area):
- Frontend architecture
- Backend services
- Database design
- Infrastructure
- Security architecture
- Integration patterns

**For analyzers** (feasibility checks):
- Technical constraints
- Performance implications
- Security considerations
- Existing code compatibility

### Phase 2: Parallel Planning

Spawn multiple **product-manager** agents:
- Each handles ONE feature area
- Each writes `docs/prd-[feature].md`

Spawn multiple **architect** agents:
- Each designs ONE system area
- Each writes `docs/architecture-[area].md`

Spawn multiple **analyzer** agents:
- Each validates ONE aspect
- Each writes `docs/feasibility-[aspect].md`

### Phase 3: Synthesis

**writer** → `docs/implementation-plan.md`
- Reads all PRDs, architectures, analyses
- Creates unified implementation plan
- Prioritizes tasks and dependencies
- Ultrathink for complex integration decisions

## Usage

> /plan add user authentication to our app
> /plan real-time collaborative editing feature
> /plan complete SaaS billing system
> /plan migrate monolith to microservices