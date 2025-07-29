# Claude Code Agent Framework (CCAF)

Specialized AI agents for development workflows in Claude Code. Get the right expertise for each task with focused agents and multi-agent orchestration.

## Agents

- **Developer** - Feature implementation, bug fixes, clean code
- **Architect** - System design, technical planning
- **Tester** - Test development and execution
- **Researcher** - Technology investigation, codebase analysis
- **Analyzer** - Code quality, security, performance review
- **Product Manager** - Requirements to technical specs
- **Git Specialist** - Git operations, version control, commit formatting
- **Writer** - Documentation creation, technical writing

## Commands

### /context
Orchestrates multiple agents for complex workflows.

```
/context
/context AI chat backend integration
/context Create PRD for feature XYZ
```

Creates PRDs, research docs, architecture plans, and implementation breakdowns by coordinating the right agents automatically.

## Usage

**Individual Agents**: Select the appropriate agent in Claude Code based on your task.

**Complex Tasks**: Use `/context` command for multi-agent coordination.

## Setup

1. Clone to your workspace
2. Ensure Claude Code is installed
3. Agents and commands are automatically available

## Structure

```
.claude/
├── agents/          # Agent configurations
├── commands/        # /context command
└── settings.json    # Permissions and MCP config
.mcp.json           # MCP servers (context7, firecrawl, ref)
```