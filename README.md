# Claude Code Agent Framework (CCAF)

A collection of specialized AI agents designed to enhance development workflows using Claude Code. Each agent is configured with specific expertise and tools to handle different aspects of software development.

## What It Does

CCAF provides role-specific AI agents that can be invoked for different development tasks. Instead of using a generic AI assistant, you can call upon specialized agents with focused expertise and appropriate tool access.

## Available Agents

- **Developer** - Implements features, fixes bugs, and writes clean maintainable code following KISS, DRY, and YAGNI principles
- **Architect** - Designs system architectures, evaluates technical approaches, and creates implementation plans from PRDs
- **Writer** - Creates technical documentation, API references, user guides, and installation instructions
- **Tester** - Develops comprehensive test suites, executes tests, and analyzes results
- **Git Specialist** - Handles Git operations, merge conflicts, branch management, and GitHub CLI tasks
- **Researcher** - Investigates technologies, analyzes codebases, and gathers technical information
- **Analyzer** - Reviews code quality, identifies issues, and provides optimization recommendations
- **Product Manager** - Translates business requirements into technical specifications and manages project scope

## Key Features

- **Specialized Expertise** - Each agent has focused knowledge and appropriate tool access
- **Consistent Quality** - Agents follow established principles and project patterns
- **Enhanced Productivity** - Right agent for the right task reduces context switching
- **Tool Integration** - Configured with MCP servers for web search, documentation, and development tools

## Usage

Agents are configured for use with Claude Code's agent system. Simply invoke the appropriate agent based on your task:

- Need to implement a feature? Use the **Developer** agent
- Planning system architecture? Use the **Architect** agent  
- Writing documentation? Use the **Writer** agent
- Creating tests? Use the **Tester** agent

## Project Structure

```
.claude/
├── agents/          # Agent configuration files
│   ├── developer.md
│   ├── architect.md
│   ├── writer.md
│   ├── tester.md
│   ├── git-specialist.md
│   ├── researcher.md
│   ├── analyzer.md
│   └── product-manager.md
├── settings.json    # Claude Code permissions and MCP server configuration
└── settings.local.json
.mcp.json           # MCP server definitions (context7, firecrawl, ref)
```

## Setup

1. Clone this repository to your development workspace
2. Ensure you have Claude Code installed and configured
3. The agents will be automatically available in your Claude Code agent selector

## MCP Integration

The framework includes preconfigured MCP servers:
- **Context7** - Enhanced context management
- **Firecrawl** - Web scraping and content extraction  
- **Ref** - Reference documentation and API lookup

Each agent has appropriate permissions and tool access configured for their specialized role.