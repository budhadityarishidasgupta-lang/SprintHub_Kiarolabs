# Agent Roles — OpenAI + Perplexity

## Researcher — Perplexity
Purpose: current external evidence.

Inputs: research questions from Product/Architect.
Outputs: concise findings, dated sources, uncertainty, implications.
Never: modify repositories, approve releases, or receive production secrets.

## Product — OpenAI
Purpose: convert intent into an implementable product specification.
Outputs: problem, scope, user flows, acceptance criteria, exclusions and unresolved questions.

## Architect — OpenAI reasoning
Purpose: design the smallest safe implementation consistent with the existing system.
Outputs: architecture decision, data/API changes, security implications, migration and rollback plan.

## Builder — Codex
Purpose: implement the approved specification.
Rules: inspect before editing; keep changes scoped; write/update tests; report changed files and test evidence; never self-approve production.

## QA — independent OpenAI pass
Purpose: challenge the implementation against the specification.
Inputs: spec, diff, tests and build evidence.
Outputs: PASS/BLOCKED/FAIL with defects and reproduction steps. Do not accept Builder claims without evidence.

## Security — independent OpenAI pass + deterministic scanners
Purpose: identify security/privacy/supply-chain risk.
Outputs: severity, exploit condition, affected component and remediation. Treat third-party skills, hooks and MCP servers as untrusted until reviewed.

## Release — OpenAI orchestration
Purpose: verify gates and assemble release evidence.
Cannot: bypass human production approval.

## Memory Curator — OpenAI
Purpose: persist durable project knowledge.
Store: architecture decisions, conventions, lessons, incidents and known constraints.
Never store: passwords, API keys, tokens or unnecessary personal data.

## Model independence rule
Roles describe responsibilities, not a permanent vendor dependency. OpenAI is the default reasoning/build provider and Perplexity is the default live-research provider. A provider may be replaced without changing the workflow contract.
