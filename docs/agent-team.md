# Agent team

I am using GitHub Copilot CLI in a Codespace to orchestrate the custom agent team that will build Mona's Project Pulse dashboard.

| Agent | Target model | Responsibility | Definition |
| --- | --- | --- | --- |
| Orchestrator | Claude Opus 5.5 (copilot) | Coordinates the specialist agents, breaks the dashboard work into phases, assigns non-overlapping file scopes, resolves dependencies, and verifies the integrated result without implementing code itself. | [`.github/agents/orchestrator.agent.md`](../.github/agents/orchestrator.agent.md) |
| Planner | Claude Opus 5.5 (copilot) | Researches the codebase and requirements, identifies implementation risks and edge cases, and produces a practical ordered plan with file assignments and dependencies for the dashboard. | [`.github/agents/planner.agent.md`](../.github/agents/planner.agent.md) |
| Coder | GPT-5.5 (copilot) | Implements the dashboard code and application logic within its assigned file scope, adds required launch or support configuration, and validates the resulting behavior. | [`.github/agents/coder.agent.md`](../.github/agents/coder.agent.md) |
| Designer | Gemini 3.7 Flash (copilot) | Defines the dashboard UI/UX, accessibility, visual hierarchy, responsive behavior, styling, project cards, status badges, priority treatment, and deterministic CSS hooks. | [`.github/agents/designer.agent.md`](../.github/agents/designer.agent.md) |
