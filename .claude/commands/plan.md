---
description: Transform ideas into comprehensive PRDs, technical architectures, and actionable development tasks
agents: product-manager, architect, analyzer, writer
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to plan?"

## Flow
```
product-manager → architect → analyzer → writer │ writer │ writer
       ↓              ↓           ↓          ↓       ↓       ↓
      PRD         Technical    Validate   3 planning docs
```

## Orchestration

### Phase 1: Requirements (product-manager)

Create comprehensive PRD for $ARGUMENTS:
- Problem statement and user needs
- Functional/non-functional requirements  
- User stories with acceptance criteria
- Break into 1-3 day development tasks
- MUST handle edge cases and error scenarios

### Phase 2: Architecture (architect)

Receive PRD from orchestrator, then:
- Design technical architecture for $ARGUMENTS
- Create component diagrams (Mermaid)
- Define APIs, data models, integrations
- Choose appropriate patterns and technologies
- Consider existing codebase constraints

### Phase 3: Validation (analyzer)

Receive PRD + architecture from orchestrator:
- Validate technical feasibility
- Identify risks and dependencies
- Check alignment with existing systems
- Note security and performance concerns

### Phase 4: Documentation

Orchestrator synthesizes all inputs, then spawns 3 parallel writers:

**writer 1** → `docs/prd.md`
- Complete product requirements document
- User stories and acceptance criteria

**writer 2** → `docs/architecture.md`
- Technical design with diagrams
- Component specifications and APIs

**writer 3** → `docs/implementation-tasks.md`
- Prioritized task breakdown
- Dependencies and timelines
- Clear action items for developers

Ultrathink for complex architectural decisions.

## Usage

> /plan add user authentication to our app
> /plan real-time collaborative editing feature
> /plan complete SaaS billing system
> /plan migrate monolith to microservices