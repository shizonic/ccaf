---
description: Create and execute comprehensive tests and analyze code quality through massive parallelization
agents: tester, analyzer, git-specialist
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to validate?"

## Flow
```
testers... │ analyzers... → [git]
     ↓           ↓           
Direct reports  Direct reports
```

## Orchestration

### Phase 1: Parallel Validation

Orchestrator identifies all testable and analyzable aspects:

Spawn multiple **tester** agents:
- Unit tests (per module)
- Integration tests (per feature)  
- E2E tests (per user flow)
- Performance tests
- Security tests
Each writes `docs/test-[type]-[module].md`

Spawn multiple **analyzer** agents:
- Code quality (per service)
- Security scan (OWASP checks)
- Performance analysis
- Architecture compliance
- Dependency audit
Each writes `docs/analysis-[aspect]-[area].md`

### Phase 2: Version Control (if applicable)

**git-specialist**:
- Create PR if changes exist
- Summarize validation results

## Usage

> /validate user authentication system
> /validate shopping cart feature
> /validate API endpoint changes
> /validate entire application refactor