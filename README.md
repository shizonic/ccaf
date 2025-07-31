# Claude Code Agent Framework (CCAF)

A sophisticated multi-agent framework for automating software development workflows through specialized AI agents and parallel orchestration.

## Overview

CCAF provides 6 slash commands that orchestrate 10 specialized agents to handle complete software development lifecycles - from research and planning to implementation and documentation.

## Quick Start

1. **Prerequisites**: Claude Code CLI with MCP server support
2. **Configuration**: Copy `.mcp.json.example` to `.mcp.json` and add your API keys
3. **Usage**: Run any command with `/command [arguments]`

```bash
/context JWT authentication best practices
/plan add user authentication system  
/implement user login functionality
/validate authentication system
/document create API documentation
/workflow complete auth implementation
```

## Commands

### Core Development Commands
- **`/context`** - Research technologies, analyze codebases, gather requirements
- **`/plan`** - Create PRDs, technical architectures, and implementation plans  
- **`/implement`** - Build features, fix bugs, develop complete projects
- **`/validate`** - Generate tests, analyze code quality, verify implementations
- **`/document`** - Create API docs, user guides, technical specifications

### Meta Commands
- **`/workflow`** - Execute complete development lifecycle (all commands above)

## Architecture

### Specialized Agents
- **researcher** - Technology research and external documentation
- **analyzer** - Code quality, security, performance, architecture analysis
- **product-manager** - Feature requirements and business logic planning
- **architect** - System design and technical architecture
- **fullstack-developer** - Complete feature implementation
- **backend-developer** - Server-side development and APIs
- **frontend-developer** - UI/UX implementation and client-side logic
- **tester** - Test creation, execution, and quality assurance
- **writer** - Technical documentation and guides
- **git-specialist** - Version control and repository management

### Key Features
- **Massive Parallelization** - Multiple agents work simultaneously on independent tasks
- **Conflict Prevention** - Orchestrator ensures no file conflicts between parallel agents  
- **Direct Output** - Each agent writes to specific files in `docs/` directory
- **Specialization** - Each agent focuses on their domain expertise
- **Integration** - Commands work independently or as part of larger workflows

## MCP Integrations

- **context7** - Up-to-date library documentation and code examples
- **firecrawl** - Advanced web scraping and research capabilities  
- **ref** - Documentation search and reference materials

## File Structure

```
.claude/
├── commands/          # Slash command definitions
├── agents/            # Specialized agent configurations  
└── settings.json      # Permission and MCP server settings
.mcp.json              # MCP server configuration
```

## Output Structure

All agent outputs are organized in the `docs/` directory:
- `docs/research-[topic].md` - Research findings
- `docs/analysis-[area].md` - Code and architecture analysis
- `docs/prd-[feature].md` - Product requirements
- `docs/architecture-[system].md` - Technical designs
- `docs/test-[type].md` - Test reports and coverage
- `docs/final/[document].md` - Polished documentation

## Development Principles

- **KISS** - Keep implementations simple and focused
- **YAGNI** - Build only what's explicitly requested
- **DRY** - Follow existing project patterns and conventions
- **Quality First** - Emphasis on clean, maintainable, secure code
- **Parallel Execution** - Maximize efficiency through concurrent agent work

## Examples

```bash
# Research Phase
/context "analyze our authentication system and industry best practices"

# Planning Phase  
/plan "add OAuth 2.0 social login with Google and GitHub"

# Implementation Phase
/implement "create user registration API with email verification"

# Quality Assurance
/validate "comprehensive testing for auth system"

# Documentation
/document "create complete API documentation"

# Complete Workflow
/workflow "implement JWT-based authentication system"
```

## Configuration

### API Keys Required
- **Firecrawl API** - For web research and scraping
- **Ref API** - For documentation search

### Permissions
The framework requires specific bash permissions for Git operations, file management, and MCP server access. See `.claude/settings.json` for details.

---

**Note**: CCAF emphasizes defensive security practices and refuses to create potentially malicious code. All agents focus on production-ready, secure implementations following industry best practices.