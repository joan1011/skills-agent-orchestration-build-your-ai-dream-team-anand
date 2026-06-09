# Agent team

Mona's Project Pulse dashboard is built using a specialized team of four custom AI agents, orchestrated through GitHub Copilot CLI in a Codespace environment.

## The Agent Team

### 1. Orchestrator
- **Model**: Claude Opus 4.7 (copilot)
- **Definition**: `.github/agents/orchestrator.agent.md`
- **Responsibility**: Coordinates the entire team by breaking down complex requests into tasks and delegating to specialist agents. Manages workflow phases, ensures file scopes don't conflict, and verifies the integrated result hangs together.

### 2. Planner
- **Model**: Claude Opus 4.7 (copilot)
- **Definition**: `.github/agents/planner.agent.md`
- **Responsibility**: Creates implementation plans by researching the codebase, documentation, dependencies, and edge cases. Produces detailed step-by-step plans with file assignments, dependency mapping, and validation expectations—without writing code.

### 3. Coder
- **Model**: GPT-5.5 (copilot)
- **Definition**: `.github/agents/coder.agent.md`
- **Responsibility**: Implements code-oriented tasks with clear structure, explicit errors, and testable behavior. Writes code, fixes bugs, and implements logic within assigned file scope. Also creates support configuration like `.vscode/launch.json` for runnable applications.

### 4. Designer
- **Model**: Gemini 3.1 Pro (copilot)
- **Definition**: `.github/agents/designer.agent.md`
- **Responsibility**: Handles UI/UX, accessibility, information architecture, interaction flow, and visual design. Ensures a polished, responsive dashboard with clear visual hierarchy, accessibility standards, and consistent product patterns.

## Orchestration Model

GitHub Copilot CLI running in a Codespace orchestrates all work through the Orchestrator agent. The Orchestrator breaks down user requests into phases, assigns file scopes to specialists to prevent conflicts, and runs work in parallel when possible while managing sequential dependencies. This ensures coordinated, high-quality output across planning, code implementation, and design.
