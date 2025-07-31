# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains AI sub-agent definitions for Claude Code at Nivalis Studio. The agents are currently minimal stubs that need to be developed into full specialist agents with capabilities, tools, and workflows.

## Current State

**Architecture**: Flat specialist structure with optional orchestration
**Implementation Status**: All agents are minimal YAML stubs (name-only)
**Files**: 11 agent definition files (.md format with YAML frontmatter)

## Repository Structure

```
agents/
├── Technology Experts
│   ├── nextjs-expert.md
│   ├── typescript-expert.md
│   ├── tailwind-expert.md
│   ├── rust-expert.md
│   ├── go-expert.md
│   └── expo-expert.md
├── Code Quality Specialists  
│   ├── code-archaeologist.md
│   ├── code-reviewer.md
│   └── performance-optimizer.md
└── Optional Orchestrators
    ├── tech-lead-orchestrator.md
    └── team-configurator.md
```

## Agent Development Patterns

### Current Structure
Each agent file contains minimal YAML frontmatter:
```yaml
---
name: agent-name
---
```

### Required Development
Each agent needs:
- **Description**: When to use this agent and specialization area
- **Tools**: List of Claude Code tools (Read, Write, Edit, Bash, etc.)
- **Trigger Conditions**: Specific, measurable activation criteria
- **Core Capabilities**: What the agent excels at
- **Delegation Patterns**: When to hand off to other specialists

### Intended Technology Coverage
- **Frontend**: Next.js 14+, React Server Components, TypeScript, Tailwind CSS
- **Backend**: Node.js, PostgreSQL, Prisma, RESTful APIs, GraphQL  
- **Mobile**: Expo, React Native, TypeScript
- **Systems**: Rust, Go, performance optimization
- **Quality**: Code review, architectural analysis, codebase exploration

## Development Workflow

### Agent Implementation
1. **Expand Stubs**: Add full YAML frontmatter with description, tools, capabilities
2. **Define Triggers**: Specify measurable conditions for agent activation
3. **Add Content**: Include detailed capabilities, workflows, and best practices
4. **Test Integration**: Verify agents work with Claude Code sub-agent system

### Repository Maintenance
- **No Build Process**: Pure documentation-based agents, no compilation needed
- **No Dependencies**: Markdown files with YAML frontmatter only
- **Version Control**: Git-based, commit agent updates as they're developed

## Design Philosophy

**Specialist-First**: Direct access to focused experts rather than hierarchical workflows
**Context-Driven**: Agents activate based on detected patterns and explicit needs
**Optional Orchestration**: Complex multi-domain work can use orchestrator agents
**Quality Gates**: Code review recommended but not mandated through rigid workflows

## Key Implementation Notes

- Agents are currently non-functional stubs requiring development
- No mandatory workflow hierarchies - use appropriate agent for the task
- Orchestrator agents (`tech-lead-orchestrator`, `team-configurator`) are optional tools
- Each agent should be self-contained with clear delegation patterns
- Focus on Claude Code sub-agent best practices: clear responsibilities and automatic delegation