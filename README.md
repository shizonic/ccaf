# Claude Code Agent Framework (CCAF)

Multi-agent orchestration framework for specialized AI development workflows.

## Commands

### Research & Planning
- `/context` - Research technologies, analyze existing code, understand codebases
  - **When**: Exploring unfamiliar tech, investigating bugs, or learning project structure
- `/plan` - Transform ideas into PRDs and technical architectures
  - **When**: Starting new features, defining requirements, or designing system architecture

### Development & Quality
- `/implement` - Develop features with automatic agent selection based on task complexity
  - **When**: Building features, fixing bugs, or coding solutions after planning
- `/validate` - Create comprehensive tests and perform code quality analysis
  - **When**: Testing new features, ensuring code quality, or debugging issues

### Complete Workflows
- `/workflow` - End-to-end development cycle: research → plan → implement → validate
  - **When**: Full feature development from concept to tested implementation

## Quick Decision Guide

**Starting fresh?** → `/workflow` (complete cycle)  
**Need to understand something?** → `/context` (research first)  
**Have requirements ready?** → `/implement` (jump to coding)  
**Code needs testing?** → `/validate` (quality assurance)

## Usage Examples

```bash
/context JWT authentication best practices
/plan user authentication system  
/implement JWT auth middleware
/validate authentication system
/workflow add real-time notifications
```

## Agent Capabilities

### Development Specialists
- **fullstack-developer** - Complete web applications, APIs, database integration
- **backend-developer** - Server-side logic, APIs, database design, performance optimization
- **frontend-developer** - UI components, responsive design, client-side optimization
- **git-specialist** - Version control, branch management, merge conflict resolution

### Planning & Analysis
- **product-manager** - Feature requirements, PRDs, task breakdown, project planning
- **architect** - Technical system design, scalability planning, technology decisions
- **analyzer** - Code quality assessment, security audits, performance analysis
- **researcher** - Technology investigation, best practices, framework documentation

### Quality & Documentation
- **tester** - Automated testing, test strategy, quality assurance workflows
- **writer** - Technical documentation, API docs, user guides, specifications

**Framework automatically selects optimal agents based on your task complexity and requirements.**