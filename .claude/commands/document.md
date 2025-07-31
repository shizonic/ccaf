---
description: Create polished final documentation by synthesizing all existing work into comprehensive guides for different audiences
agents: analyzer, writer
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What type of documentation would you like to create? (e.g., user guide, API docs, deployment guide, complete documentation suite)"

## Flow
```
analyzer → writers... (parallel)
    ↓         ↓
Read docs/*  Create final guides
```

## Orchestration

### Phase 1: Analysis

**analyzer**:
- Read all files in `docs/` directory
- Identify documentation gaps
- Determine which final documents are needed based on $ARGUMENTS
- Create outline for each document type

### Phase 2: Parallel Documentation Creation

Orchestrator spawns multiple **writer** agents based on analyzer findings and $ARGUMENTS:

**Potential parallel writers** (spawn only relevant ones):

**writer 1** → `docs/final/user-guide.md`
- End-user documentation
- Getting started guide
- Feature explanations
- Troubleshooting

**writer 2** → `docs/final/api-reference.md`
- Complete API documentation
- Endpoints, parameters, responses
- Authentication details
- Code examples

**writer 3** → `docs/final/developer-guide.md`
- Architecture overview
- Development setup
- Contributing guidelines
- Technical decisions

**writer 4** → `docs/final/deployment-guide.md`
- Infrastructure requirements
- Environment configuration
- Deployment steps
- Monitoring setup

**writer 5** → `docs/final/README.md`
- Project overview
- Quick start
- Key features
- Links to other docs

Each writer receives:
- Relevant sections from analyzer's findings
- Specific document type to create
- Target audience for their document

Writers MUST create self-contained, polished documents.

## Usage

> /document create complete documentation suite
> /document user and API documentation only
> /document deployment and operations guides
> /document README and quick start guide