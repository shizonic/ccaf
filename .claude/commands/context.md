---
description: Gather comprehensive context about a project, feature, or technology through parallel research and analysis
agents: researcher, analyzer, writer
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to gather context about?"

## Flow
```
researcher │ analyzer → orchestrator → writer │ writer │ writer
     ↓          ↓            ↓             ↓       ↓       ↓
 External   Internal     Synthesize    3 parallel docs
```

## Orchestration

### Phase 1: Parallel Research (researcher │ analyzer)

**researcher**: 
- Research $ARGUMENTS externally
- Find official docs, APIs, best practices
- MUST use MCP tools (context7, firecrawl, ref) when available
- Focus on latest versions and standards

**analyzer**:
- Analyze existing codebase for $ARGUMENTS
- Identify current implementations, patterns, dependencies
- Map project structure and architecture
- Note technical debt or improvements needed

### Phase 2: Synthesis & Documentation

Orchestrator MUST:
1. Combine researcher findings + analyzer insights
2. Identify gaps and overlaps
3. Create unified context understanding

Then spawn 3 parallel writers with synthesized context:

**writer 1** → `docs/context-overview.md`
- Executive summary of $ARGUMENTS
- Key findings from research + analysis
- Current state vs best practices

**writer 2** → `docs/tech-stack-analysis.md`  
- Technologies, frameworks, dependencies
- Version information and compatibility
- Integration points and constraints

**writer 3** → `docs/implementation-guide.md`
- API references and code examples
- Architecture patterns applicable
- Next steps and recommendations

MUST NOT assume greenfield - adapt to existing code when present.

## Usage

> /context how to implement JWT authentication
> /context React Server Components  
> /context our entire e-commerce platform
> /context migrating from REST to GraphQL