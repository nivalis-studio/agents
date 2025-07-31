# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains fully-developed AI sub-agent definitions for Claude Code at Nivalis Studio. These agents provide specialized expertise across technology domains, development roles, and project orchestration patterns.

## Architecture & Workflow

**Organization**: Hierarchical specialist structure with orchestration layers
**Workflow**: CTO → Tech Leads → Specialists + Maintainers
**Implementation Status**: All agents are fully developed with comprehensive capabilities, tools, and delegation patterns

## Repository Structure

```
agents/
├── orchestrators/ - Project setup and work dispatch
│   ├── team-configurator.md    - Project setup, environment config
│   └── tech-orchestrator.md    - Multi-domain coordination, strategic decisions
├── tech-leads/ - Domain leadership and architecture
│   ├── frontend-lead.md        - Frontend architecture, design systems
│   ├── backend-lead.md         - Backend architecture, scalability
│   └── mobile-lead.md          - Mobile strategy, cross-platform
├── devs/ - Technology specialists
│   ├── nextjs-expert.md        - Next.js 14+, App Router, RSC
│   ├── typescript-expert.md    - TypeScript, type systems
│   ├── tailwind-expert.md      - Tailwind CSS, design systems
│   ├── expo-expert.md          - Expo, React Native
│   ├── rust-expert.md          - Rust systems programming
│   ├── go-expert.md            - Go backend development
│   ├── algo-expert.md          - Algorithms, data structures
│   ├── database-expert.md      - Database design, optimization
│   ├── bun-expert.md           - Bun runtime, tooling
│   ├── deployment-expert.md    - Deployment strategies, DevOps
│   ├── infrastructure-expert.md - Infrastructure, cloud services
│   └── performance-expert.md   - Performance optimization, monitoring
└── maintainers/ - Code quality and maintenance
    ├── code-archaeologist.md   - Legacy analysis, codebase exploration
    ├── code-reviewer.md        - Code quality, best practices
    ├── code-tester.md          - Testing strategy, quality assurance
    ├── code-fixer.md           - Bug fixing, refactoring, technical debt
    ├── code-refactoring-expert.md - Advanced refactoring patterns
    ├── code-documenter.md      - Documentation generation, maintenance
    └── api-documenter.md       - API documentation, OpenAPI specs
```

## Agent Structure & Capabilities

### Agent File Format

Each agent is a markdown file with comprehensive YAML frontmatter:

```yaml
---
name: agent-name
description: When and how to use this agent with specific examples
color: visual-identifier
model: inherit
---
```

### Standard Agent Components

- **Trigger Conditions**: Automatic and explicit activation criteria
- **Core Capabilities**: Detailed specialization areas and expertise
- **Tool Usage Patterns**: How the agent uses Claude Code tools
- **Delegation Patterns**: Coordination, handoff, and collaboration rules
- **Quality Standards**: Success criteria and best practices

### Technology Coverage

- **Frontend**: Next.js 14+, React Server Components, TypeScript, Tailwind CSS, component libraries (@medusajs/ui, shadcn/ui)
- **Backend**: Node.js, PostgreSQL, Prisma, Go, Rust, API design, server-side architecture
- **Mobile**: Expo, React Native, cross-platform development, native integration
- **Infrastructure**: Database design, algorithms, performance optimization, deployment, cloud services
- **Quality**: Code review, testing, linting, legacy system analysis, refactoring, documentation

## Workflow Orchestration

### Recommended Usage Pattern

1. **Start with Orchestrators**: Use `tech-orchestrator` for complex projects requiring coordination
2. **Project Setup**: Use `team-configurator` for new projects and environment setup
3. **Domain Leadership**: Tech leads coordinate domain-specific architecture decisions
4. **Specialist Implementation**: Technology experts handle specific implementation tasks
5. **Quality Assurance**: Maintainer agents ensure code quality and system health

### Direct Specialist Access

- Simple tasks can directly access specialist agents without orchestration
- Each agent has clear delegation patterns for seamless handoffs
- Agents automatically coordinate with related specialists when needed

## Key Operational Notes

### No Build Process

- Pure documentation-based agent definitions
- No compilation, dependencies, or build steps required
- Git-based version control for agent evolution

### Quality Standards

- All agents follow @nivalis/eslint-config standards when applicable
- Code fixer agent specializes in eslint and prettier rule enforcement
- Comprehensive testing through code-tester agent integration
- Focus on performance optimization with specific Core Web Vitals targets
- Security-first approach with vulnerability assessment and remediation

### Agent Coordination

- **Horizontal**: Specialists collaborate with peers (e.g., nextjs-expert ↔ typescript-expert)
- **Vertical**: Tech leads coordinate with specialists in their domain
- **Cross-Domain**: Orchestrators manage multi-domain projects and strategic decisions
- **Component Library Strategy**: nextjs-expert prioritizes @medusajs/ui, falls back to shadcn/ui, delegates styling to tailwind-expert
- **Auto-Delegation**: Agents automatically hand off to specialists when encountering domain-specific requirements

## Common Development Workflows

### Starting New Projects

1. Use `tech-orchestrator` for complex multi-domain projects
2. Use `team-configurator` for project setup and environment configuration
3. Delegate to appropriate tech leads based on project domain

### Feature Development

1. **Frontend Features**: frontend-lead → nextjs-expert/tailwind-expert coordination
2. **Backend Features**: backend-lead → relevant technology specialists (go-expert, database-expert)
3. **Full-Stack Features**: tech-orchestrator coordinates both domains

### Code Quality & Maintenance

1. **Code Review**: Use code-reviewer for systematic quality assessment
2. **Bug Fixing**: Use code-fixer for root cause analysis and safe fixes
3. **Legacy Analysis**: Use code-archaeologist for understanding complex codebases
4. **Testing**: Use code-tester for comprehensive testing strategy

### Performance & Infrastructure

1. **Performance Issues**: performance-expert for optimization and monitoring
2. **Deployment**: deployment-expert for CI/CD and deployment strategies
3. **Infrastructure**: infrastructure-expert for cloud services and scaling
