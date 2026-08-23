# Kiaro AI Engineering Harness

This directory is the curated engineering harness for future KiaroLabs builds. It deliberately does **not** blindly vendor or execute third-party repositories. External projects are tracked as upstream references and patterns are adopted only after license/security review.

## Default model stack

- **OpenAI / Codex** — implementation, refactoring, repository work, tests, code review, release preparation.
- **OpenAI reasoning model** — product/architecture decisions, specification review, QA reasoning, security reasoning and final synthesis.
- **Perplexity** — web-grounded research, current documentation, competitor/library research and external fact validation. Perplexity is a research provider, not the primary code executor.

## Mandatory workflow

Research -> Specify -> Clarify -> Plan -> Implement -> Test -> Independent Review -> Security Gate -> Sandbox/UAT -> Release Gate -> Remember

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

See `UPSTREAM_REGISTRY.md`, `MODEL_ROUTING.md`, and `WORKFLOW.md`.
