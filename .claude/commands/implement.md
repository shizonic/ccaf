---
description: Implement features, fixes, or complete projects with adaptive development approach and optional version control
agents: fullstack-developer, backend-developer, frontend-developer, git-specialist
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to implement?"

## Flow
```
Simple: fullstack-developer → [git-specialist]
Complex: backend-developer │ frontend-developer → [git-specialist]
```

## Orchestration

### Phase 1: Implementation Strategy

Orchestrator MUST analyze $ARGUMENTS to determine:
- Scope requires full-stack OR specialized development
- Existing code patterns to follow
- Git commits beneficial or not

### Phase 2A: Solo Implementation (if unified work)

**fullstack-developer**:
- Implement $ARGUMENTS following existing patterns
- MUST use KISS, DRY, YAGNI principles
- NEVER add unrequested features
- Prefer editing existing files over creating new ones

### Phase 2B: Parallel Implementation (if separable)

**backend-developer** │ **frontend-developer** (parallel):

Backend:
- APIs, database, business logic for $ARGUMENTS
- Security, performance, error handling
- Follow existing backend patterns

Frontend:  
- UI components, state management for $ARGUMENTS
- Accessibility, responsive design
- Follow existing frontend patterns

Orchestrator MUST coordinate both outputs for consistency.

### Phase 3: Version Control (optional)

IF git commits would help organization:

**git-specialist**:
- Create semantic commits for changes
- MUST NOT include "Co-Authored-By: Claude"
- One commit per logical change
- Clear commit messages

Skip if changes are exploratory or temporary.

## Usage

> /implement fix the login timeout bug
> /implement add dark mode toggle
> /implement create REST API for user management  
> /implement build complete chat application