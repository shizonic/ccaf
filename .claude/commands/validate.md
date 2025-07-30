---
description: Create and execute comprehensive tests, analyze code quality, and generate complete documentation
agents: tester, analyzer, writer, git-specialist
---

## Task: $ARGUMENTS

IF $ARGUMENTS is empty: "What would you like to validate and document?"

## Flow
```
tester │ analyzer → orchestrator → writer │ writer │ writer → [git]
   ↓        ↓           ↓             ↓       ↓       ↓
Tests   Analysis   Synthesize    3 parallel docs
```

## Orchestration

### Phase 1: Parallel Validation (tester │ analyzer)

**tester**:
- Create comprehensive tests for $ARGUMENTS
- Unit, integration, edge cases
- Execute all tests and capture results
- MUST NOT fix failing tests
- Report coverage metrics

**analyzer**:
- Review code quality for $ARGUMENTS  
- Security vulnerabilities (OWASP)
- Performance bottlenecks
- Architecture compliance
- Technical debt assessment

### Phase 2: Documentation

Orchestrator synthesizes test + analysis results, then spawns 3 parallel writers:

**writer 1** → `docs/test-report.md`
- Test execution summary
- Pass/fail breakdown
- Coverage analysis
- Failed test details (no fixes)

**writer 2** → `docs/quality-analysis.md`
- Code quality findings
- Security assessment  
- Performance review
- Improvement recommendations

**writer 3** → `docs/user-guide.md`
- How to use $ARGUMENTS
- API documentation if applicable
- Configuration options
- Troubleshooting guide

### Phase 3: Final PR (optional)

IF project uses PRs:

**git-specialist**:
- Create PR with all changes
- Include test and quality summaries
- Reference documentation

## Usage

> /validate user authentication system
> /validate shopping cart feature
> /validate API endpoint changes
> /validate entire application refactor