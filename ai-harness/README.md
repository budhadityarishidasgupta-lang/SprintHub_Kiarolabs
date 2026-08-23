# Universal AI Engineering Harness

This directory is a provider-portable engineering harness for **multiple independent projects**. It is not KiaroLabs-specific. At the start of every engagement, the operator selects or creates a project profile that defines the target repository, environment, risk class, constraints, deployment rules and allowed tools.

The same base harness can support product development, automation, data agents, research tools, internal utilities and authorized security-testing projects. Project-specific rules live under `projects/`; universal rules live in the harness root.

## Default model stack

- **OpenAI / Codex** — implementation, refactoring, repository work, tests, code review and release preparation.
- **OpenAI reasoning model** — product/architecture decisions, specification review, QA reasoning, security reasoning and final synthesis.
- **Perplexity** — web-grounded research, current documentation, competitor/library research and external fact validation. Perplexity is a research provider, not the primary code executor.

## Mandatory project selection

Every run begins by resolving a `PROJECT_ID`. The selected project profile determines:

- repository/repositories in scope
- business or technical objective
- production vs sandbox boundaries
- deployment targets
- data sensitivity
- allowed and prohibited actions
- required validation gates
- project-specific memory and decisions

If no project is selected, the harness must remain in planning/read-only mode and must not modify a repository or environment.

## Standard workflow

Project Select -> Research -> Specify -> Clarify -> Plan -> Implement -> Test -> Independent Review -> Security Gate -> Sandbox/UAT -> Release Gate -> Remember

No production deployment is automatic. Any third-party skill, hook, MCP server or executable must be reviewed before adoption.

## Eight capabilities captured

1. ECC agent-harness patterns
2. GitHub Spec Kit / spec-driven development
3. gstack specialist-role patterns
4. Vercel agent-skills / reusable skills
5. awesome-mcp-servers / connector discovery
6. Dify / visual workflow patterns
7. OpenAI Codex / primary coding executor
8. UI/UX skill and review patterns

See `PROJECT_REGISTRY.md`, `PROJECT_PROFILE_TEMPLATE.md`, `UPSTREAM_REGISTRY.md`, `MODEL_ROUTING.md`, `AGENTS.md`, and `WORKFLOW.md`.
