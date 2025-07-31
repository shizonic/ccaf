# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Architecture Overview

This is the Claude Code Agent Framework (CCAF) - a multi-agent orchestration system that automates software development workflows through specialized AI agents and massive parallelization.

### Core Components

- **6 Slash Commands**: `/context`, `/plan`, `/implement`, `/validate`, `/document`, `/workflow`
- **10 Specialized Agents**: researcher, analyzer, product-manager, architect, fullstack-developer, backend-developer, frontend-developer, tester, writer, git-specialist
- **3 MCP Servers**: context7 (library docs), firecrawl (web scraping), ref (documentation search)

### Command Orchestration Pattern

All commands follow a 3-phase pattern:
1. **Task Decomposition**: Analyze requirements and create parallel subtasks
2. **Parallel Execution**: Spawn multiple specialized agents working simultaneously
3. **Direct Output**: Each agent writes to dedicated files in `docs/` directory

**Critical**: Agents never conflict on file writes. Each writes to specific paths like `docs/research-[topic].md`, `docs/analysis-[area].md`, etc.

## Agent Constraints and Capabilities

### Strict Agent Boundaries
- **tester**: NEVER fixes failing tests or modifies code - analysis and reporting only
- **git-specialist**: MUST use semantic commit format (`<type>(<scope>): <subject>`) and NEVER includes author signatures
- **researcher**: Has access to all MCP servers for external research
- **analyzer**: Focuses on 4 domains: code quality, security, performance, architecture
- **All developers**: Follow KISS, YAGNI, DRY principles and existing project patterns

### Specialized Toolsets
- **researcher**: context7, firecrawl, ref MCP servers + WebSearch
- **git-specialist**: All git operations, GitHub CLI, semantic commits
- **All agents**: Standard file operations, bash commands per permissions

## File Organization

### Configuration Structure
```
.claude/
├── commands/          # 6 slash command definitions with orchestration logic
├── agents/           # 10 agent specifications with constraints and capabilities
└── settings.json     # Base permissions and MCP server enablement
.mcp.json            # MCP server configuration with API keys
```

### Output Structure
```
docs/
├── research-[topic].md      # External research findings
├── analysis-[area].md       # Code/architecture analysis
├── prd-[feature].md         # Product requirements
├── architecture-[system].md # Technical designs
├── test-[type].md          # Test reports and coverage
└── final/[document].md     # Polished documentation
```

## Development Workflows

### Primary Command Patterns

**Research Phase**: `/context [query]` spawns researcher + analyzer for comprehensive investigation
**Planning Phase**: `/plan [feature]` spawns product-manager + architect for requirements and design
**Implementation Phase**: `/implement [task]` spawns developers in parallel by module/component
**Quality Phase**: `/validate [scope]` spawns tester + analyzer for comprehensive testing
**Documentation Phase**: `/document [type]` spawns writer + analyzer for polished docs
**Complete Workflow**: `/workflow [project]` executes all phases with maximum parallelization

### Parallelization Strategy

Commands decompose work to avoid conflicts:
- **By Module**: Different agents work on separate components
- **By Layer**: Frontend/backend/database agents work simultaneously  
- **By Feature**: Each agent implements complete independent features
- **By Domain**: Research/analysis/implementation happen in parallel

## MCP Server Integration

### Required API Keys
- **Firecrawl**: `FIRECRAWL_API_KEY` in `.mcp.json` for web scraping
- **Ref**: `REF_API_KEY` in `.mcp.json` for documentation search
- **Context7**: No API key required

### Research Capabilities
- **context7**: Version-specific library documentation and code examples
- **firecrawl**: Advanced web scraping with AI-powered content extraction
- **ref**: Public and private documentation search and indexing

## Security and Permissions

### Permission Model
- **Bash Commands**: Limited to specific operations (ls, find, mkdir, git, rg, gh, rm)
- **MCP Servers**: Full access to enabled servers (context7, firecrawl, ref)
- **WebFetch**: Restricted to trusted documentation domains
- **File Operations**: Standard read/write/edit permissions

### Security Principles
- All agents refuse to create potentially malicious code
- API keys stored in `.mcp.json` (should be environment variables in production)  
- Explicit constraints prevent agent overreach and hallucination
- Defensive coding practices enforced across all implementations

## Key Development Patterns

### Agent Specialization
Each agent has a single domain of expertise and cannot cross boundaries. When spawning agents, the orchestrator ensures no file conflicts and assigns independent work units.

### Workflow Composition  
Commands can be used independently or composed. The `/workflow` command demonstrates full lifecycle automation by executing all other commands in sequence.

### Quality-First Implementation
All developer agents emphasize production-ready code following existing project conventions rather than imposing new patterns. Security, performance, and maintainability are primary concerns.

### Massive Parallelization
The framework's core strength is running multiple specialized agents simultaneously on independent tasks, dramatically accelerating complex development workflows while maintaining quality and avoiding conflicts.