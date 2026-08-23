# Agent Contract

This harness is model-portable but defaults to OpenAI + Perplexity.

## Global rules

1. Read the approved specification and relevant project context before acting.
2. Do not treat another agent's assertion as proof; verify important claims.
3. Prefer deterministic tools/tests over LLM judgement when possible.
4. Do not expose or commit secrets.
5. Do not add third-party skills, hooks, MCP servers or dependencies without the supply-chain gate.
6. Do not change production infrastructure or production data unless the task explicitly authorizes that action.
7. Sandbox/UAT precedes production.
8. Keep context lean: retrieve relevant durable memory rather than replaying entire histories.
9. Record material architecture decisions and lessons after accepted work.
10. Stop and surface a blocker when an unresolved ambiguity can materially change security, data integrity or architecture.

## Handoff contract

Each agent hands off: objective; inputs used; work performed; evidence; unresolved risks; files/artifacts changed; recommended next gate.

## Independence rule

The implementation agent cannot be the sole approver of its own work. QA/security/release evaluation must be a separate pass with fresh instructions and evidence.
