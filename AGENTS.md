# WeatherCheck — AI Agent Instructions

## 1. Project Context

WeatherCheck is a full-stack weather application that allows users to search for locations and view current weather conditions and short-term forecasts.

### Technology Stack

- Frontend: React
- Backend: Node.js with Express
- Containerization: Docker and Docker Compose
- Weather Data: External weather API

### Project Documentation

- `docs/project-definition.md` — Project purpose and scope.
- `docs/requirements.md` — Functional and technical requirements.

Consult the project documentation when implementing features or making technical decisions. Follow the established project scope and requirements.

## 2. Development Guidelines

- Follow the established project architecture and requirements.
- Keep changes focused on the assigned task and its acceptance criteria.
- Prefer simple, maintainable solutions over unnecessary complexity.
- Follow existing coding conventions and project structure.
- Avoid creating unnecessary files, directories, or documentation.
- Store automated tests in dedicated `tests/` directories within their respective frontend and backend projects.
- Do not introduce new dependencies unless they are justified and approved.
- Do not implement additional features beyond the assigned task without approval.
- Never hardcode or expose API keys, credentials, or other sensitive information. Use environment variables for secrets.

## 3. Testing & Validation

- Verify that implemented changes satisfy the assigned task's acceptance criteria.
- Run relevant automated tests when available.
- Test new or modified functionality when practical.
- Create or update automated tests when appropriate to verify new or modified functionality.
- Report test results, failures, and any tests that could not be performed.
- Provide a summary of changes, modified files, and unresolved issues.
- Do not claim that functionality works unless it has been verified.
- Address errors introduced by changes before considering the task complete.

## 4. Agent Autonomy & Approval

- Explain the proposed approach before making significant implementation changes.
- Ask for clarification when requirements are ambiguous rather than making significant assumptions.
- Make routine code changes within the assigned task's scope without requiring approval for every modification.
- Request approval before making major architectural or design decisions.
- Request approval before installing new dependencies or introducing additional technologies.
- Do not delete existing files or make destructive changes without approval.
- Do not commit or push changes to Git without explicit approval.
- Leave final code review and task completion decisions to the developer.