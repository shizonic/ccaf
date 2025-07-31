---
description: Gather comprehensive context about a project, feature, or technology through massive parallel research and analysis
agents: researcher, analyzer, writer
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to gather context about?"

## Flow
```
researchers... │ analyzers... → [writer]
      ↓              ↓             ↓
Direct writes   Direct writes   Synthesis
```

## Orchestration

### Phase 1: Task Decomposition

Orchestrator analyzes $ARGUMENTS and creates parallel subtasks:

**For researchers** (examples based on complexity):
- Official documentation
- API references  
- Best practices
- Security considerations
- Performance patterns
- Community solutions
- Alternative approaches

**For analyzers** (based on codebase):
- Frontend components
- Backend services
- Database layer
- Test coverage
- Configuration
- Dependencies
- Architecture patterns

### Phase 2: Parallel Execution

Spawn multiple **researcher** agents:
- Each researches ONE specific aspect
- Each writes directly to `docs/research-[aspect].md`

Spawn multiple **analyzer** agents:
- Each analyzes ONE codebase area
- Each writes directly to `docs/analysis-[area].md`

### Phase 3: Optional Synthesis

IF $ARGUMENTS requires unified overview:

**writer** → `docs/context-synthesis.md`
- Reads all research and analysis files
- Creates executive summary
- Identifies key patterns and recommendations

## Usage

> /context how to implement JWT authentication
> /context React Server Components  
> /context our entire e-commerce platform
> /context migrating from REST to GraphQL