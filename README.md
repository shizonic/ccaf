# Claude Code Agent Framework (CCAF)

A comprehensive collection of specialized AI agents and orchestration commands designed to enhance development workflows using Claude Code. The framework provides role-specific agents with focused expertise and a powerful context command for orchestrating multi-agent workflows.

## What It Does

CCAF provides role-specific AI agents that can be invoked for different development tasks, plus orchestration capabilities for complex workflows. Instead of using a generic AI assistant, you can call upon specialized agents with focused expertise and appropriate tool access, or use the `/context` command to coordinate multiple agents for comprehensive project analysis and planning.

## Available Agents

- **Developer** - Implements features, fixes bugs, and writes clean maintainable code following KISS, DRY, and YAGNI principles
- **Architect** - Designs system architectures, evaluates technical approaches, and creates implementation plans from PRDs
- **Tester** - Develops comprehensive test suites, executes tests, and analyzes results
- **Researcher** - Investigates technologies, analyzes codebases, and gathers technical information
- **Analyzer** - Reviews code quality, security vulnerabilities, performance bottlenecks, and architectural patterns
- **Product Manager** - Translates business requirements into technical specifications and manages project scope

## Key Features

- **Specialized Expertise** - Each agent has focused knowledge and appropriate tool access
- **Multi-Agent Orchestration** - Context command coordinates multiple agents for complex workflows
- **Intelligent Task Routing** - Agents automatically delegate to the most appropriate specialist
- **Consistent Quality** - Agents follow established principles and project patterns
- **Enhanced Productivity** - Right agent for the right task reduces context switching
- **Tool Integration** - Configured with MCP servers for web search, documentation, and development tools

## Commands

### /context Command

The `/context` command orchestrates multiple agents to create comprehensive project context including PRDs, documentation research, architecture design, and implementation planning.

**Usage Examples:**
```
/context
/context AI chat backend integration
/context Create PRD for feature XYZ
/context Research OpenAI Chat API documentation
```

**What it does:**
- Analyzes your request to determine required outputs and appropriate agents
- Coordinates multiple agents in parallel when beneficial, or sequentially when dependencies exist
- Creates comprehensive project documentation including:
  - Product Requirements Documents (PRDs)
  - Technology research and documentation
  - Codebase analysis for brownfield projects
  - System architecture and implementation plans
  - Task breakdowns for development work

**Available Agents for Context Command:**
- **Analyzer**: Reviews code quality, identifies issues, provides optimization recommendations
- **Researcher**: Investigates technologies, analyzes documentation, gathers technical information
- **Product Manager**: Creates PRDs, translates business requirements into technical specifications
- **Architect**: Designs system architectures, creates implementation plans from PRDs
- **Writer**: Creates technical documentation, API references, user guides

## Usage

### Individual Agents
Agents are configured for use with Claude Code's agent system. Simply invoke the appropriate agent based on your task:

- Need to implement a feature? Use the **Developer** agent
- Planning system architecture? Use the **Architect** agent  
- Need comprehensive code analysis? Use the **Analyzer** agent
- Creating tests? Use the **Tester** agent
- Researching technologies? Use the **Researcher** agent
- Managing project requirements? Use the **Product Manager** agent

### Multi-Agent Workflows
For complex tasks requiring multiple perspectives, use the `/context` command which will automatically coordinate the appropriate agents.

## Project Structure

```
.claude/
├── agents/          # Agent configuration files
│   ├── analyzer.md      # Code quality, security, and performance analysis
│   ├── architect.md     # System architecture and technical design
│   ├── developer.md     # Feature implementation and bug fixes
│   ├── product-manager.md # Requirements and project scope management
│   ├── researcher.md    # Technology investigation and codebase analysis
│   └── tester.md       # Test development and execution
├── commands/        # Custom command configurations
│   └── context.md      # Multi-agent orchestration command
├── settings.json    # Claude Code permissions and MCP server configuration
└── settings.local.json
.mcp.json           # MCP server definitions (context7, firecrawl, ref)
```

## Setup

1. Clone this repository to your development workspace
2. Ensure you have Claude Code installed and configured
3. The agents and commands will be automatically available in your Claude Code interface
   - Individual agents appear in the agent selector
   - The `/context` command can be invoked directly in any conversation

## Agent Capabilities

Each agent is configured with specific tools and expertise:

- **Analyzer**: Comprehensive code analysis including quality assessment, security scanning, performance evaluation, and architectural review
- **Architect**: System design from PRDs, technology stack selection, deployment strategy planning, and scalability design
- **Developer**: Feature implementation, bug fixes, code refactoring, and adherence to clean code principles
- **Product Manager**: Business requirement translation, scope management, and stakeholder communication
- **Researcher**: Technology investigation, API documentation analysis, and codebase exploration
- **Tester**: Test suite development, test execution, result analysis, and quality assurance

## MCP Integration

The framework includes preconfigured MCP servers:
- **Context7** - Enhanced context management and information retrieval
- **Firecrawl** - Web scraping and content extraction for research tasks
- **Ref** - Reference documentation and API lookup capabilities

Each agent has appropriate permissions and tool access configured for their specialized role, ensuring they can effectively perform their designated functions while maintaining security boundaries.