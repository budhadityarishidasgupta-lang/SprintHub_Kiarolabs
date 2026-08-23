# Model Routing — OpenAI + Perplexity

Claude is not required by this harness.

## Roles

### Research Agent — Perplexity
Use for current external evidence: official documentation discovery, package/framework changes, market/competitor research, implementation alternatives, known issues and current best practices. Output must include sources and an evidence summary. Research output is advisory and must not directly modify production code.

### Product & Specification Agent — OpenAI
Turn the request plus research into scope, user stories, constraints, acceptance criteria, non-goals and measurable definition of done. Resolve ambiguity before implementation when it materially affects architecture or safety.

### Architecture Agent — OpenAI reasoning
Choose the smallest sustainable architecture. Record interfaces, data changes, security/privacy constraints, migration and rollback plan. Prefer existing project patterns over new dependencies.

### Build Agent — OpenAI Codex
Read the approved spec and architecture. Implement only approved scope, create/update tests, preserve existing behavior, and report changed files and assumptions. Never silently deploy production.

### QA Agent — OpenAI (independent pass)
Evaluate acceptance criteria, regressions, edge cases, data integrity and failure paths. Treat builder claims as untrusted until verified.

### Security Agent — OpenAI reasoning + deterministic scanners where available
Review auth/authz, secrets, dependency/supply-chain risk, injection, unsafe execution, privacy/data exposure and deployment configuration. Third-party agent skills/hooks/MCPs require explicit review.

### Release Agent — OpenAI
Require tests/QA/security gates, migration and rollback readiness. Deploy to sandbox/UAT first. Production remains a separate explicit gate.

### Memory Agent — OpenAI
After an accepted change, persist durable architecture decisions, incidents, lessons and known constraints. Do not dump full chat history into context.

## Routing principle

Use Perplexity to answer **what is currently true outside the repository**. Use OpenAI to answer **what should we do and why**. Use Codex to answer **make the approved repository change**. Use an independent OpenAI pass to answer **did it actually work and is it safe**.

## Fallback

If Perplexity is unavailable, use a web-grounded research provider. If Codex is unavailable, another OpenAI coding-capable agent may implement the same approved spec. The workflow is provider-portable; roles and gates are more important than model brand.
