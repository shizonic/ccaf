# Claude Code Agent Framework (CCAF)

Specialized AI agents for development workflows in Claude Code. Get the right expertise for each task with focused agents and multi-agent orchestration.

## Agents

- **Analyzer**: Reviews code quality, identifies security vulnerabilities, and provides performance optimization recommendations
- **Researcher**: Investigates technologies and frameworks, providing comprehensive reports on technical components and best practices
- **Product Manager**: Transforms feature ideas into structured PRDs and breaks down complex projects into actionable tasks
- **Architect**: Designs scalable system architectures and translates business requirements into technical solutions
- **Frontend Developer**: Builds responsive UI components, optimizes frontend performance, and creates accessible user interfaces
- **Backend Developer**: Designs APIs, implements secure authentication, optimizes database operations, and builds scalable server architectures
- **Fullstack Developer**: Implements complete features across frontend and backend, handles database operations, and develops APIs with practical solutions
- **Git Specialist**: Manages version control workflows, resolves merge conflicts, and ensures proper commit standards
- **Tester**: Creates comprehensive test suites, executes tests, and provides detailed analysis of results
- **Writer**: Creates clear documentation including API references, user guides, and technical specifications

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