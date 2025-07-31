---
description: Implement features, fixes, or complete projects through massive parallel development
agents: fullstack-developer, backend-developer, frontend-developer, git-specialist
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to implement?"

## Flow
```
developers... (parallel by module/file/component)
      ↓
Direct implementation → [git-specialist]
```

## Orchestration

### Phase 1: Implementation Planning

Orchestrator analyzes $ARGUMENTS and identifies:
- Independent modules/components/files
- Backend vs frontend work
- Potential conflicts to avoid
- Optimal parallelization strategy

### Phase 2: Parallel Implementation

**Option A - Multiple fullstack-developers** (for feature-based split):
- Each implements ONE complete feature
- No file conflicts between agents
- Example: auth, payments, notifications

**Option B - Specialized parallel development**:

Spawn multiple **backend-developer** agents:
- User service
- Auth middleware  
- Database models
- API endpoints
- Background jobs

Spawn multiple **frontend-developer** agents:
- Login components
- Dashboard views
- Form handlers
- State management
- UI utilities

Orchestrator ensures NO file conflicts between parallel agents.

### Phase 3: Version Control (if beneficial)

**git-specialist**:
- Review all changes
- Create logical commits
- Branch management if needed

## Usage

> /implement fix the login timeout bug
> /implement add dark mode toggle
> /implement create REST API for user management  
> /implement build complete chat application