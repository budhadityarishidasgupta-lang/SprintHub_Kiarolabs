# Universal Agent Contract

This harness is model-portable, defaults to OpenAI + Perplexity, and serves multiple projects.

## Project binding rule

Before any write, execution, deployment or state-changing action, resolve the active `PROJECT_ID` and read its project profile. Never carry project-specific assumptions, credentials, deployment targets, memory or permissions from one project into another.

If the project is missing or ambiguous, remain read-only until it is resolved.

## Global rules

1. Read the selected project profile, approved specification and relevant project context before acting.
2. Treat project boundaries as hard isolation boundaries.
3. Do not treat another agent's assertion as proof; verify important claims.
4. Prefer deterministic tools/tests over LLM judgement when possible.
5. Do not expose or commit secrets.
6. Do not add third-party skills, hooks, MCP servers or dependencies without the supply-chain gate.
7. Do not change production infrastructure or production data unless the selected project/task explicitly authorizes it.
8. Sandbox/UAT precedes production unless the project profile explicitly defines a different safe workflow.
9. Keep context lean: retrieve relevant durable memory rather than replaying entire histories.
10. Record material architecture decisions and lessons under the active project after accepted work.
11. Stop and surface a blocker when ambiguity can materially change security, data integrity, authorization or architecture.
12. Security-testing projects must define explicit authorized targets and scope. Never infer authorization from technical reachability.

## Handoff contract

Each agent hands off: PROJECT_ID; objective; inputs used; work performed; evidence; unresolved risks; files/artifacts changed; recommended next gate.

## Independence rule

The implementation agent cannot be the sole approver of its own work. QA/security/release evaluation must be a separate pass with fresh instructions and evidence.
