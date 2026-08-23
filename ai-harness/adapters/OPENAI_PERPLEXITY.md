# OpenAI + Perplexity Adapter

This adapter maps provider-neutral harness roles to the preferred runtime.

## OpenAI
Use OpenAI reasoning for Product, Architect, QA, Security, Release and Memory roles. Use Codex for repository implementation work.

Codex handoff should contain structured artifacts rather than full chat history:
1. feature spec
2. architecture plan
3. relevant `.ai-context` files
4. repository + branch
5. acceptance criteria
6. allowed/forbidden changes
7. required tests

## Perplexity
Use Perplexity as an external research service for questions requiring current web evidence. A research request should include:
- precise question
- freshness requirement
- preferred primary/official sources
- output: findings, citations, uncertainty and engineering implication

Research results are advisory evidence. They cannot authorize repository writes or production changes.

## Secrets
Expected runtime secrets, when APIs are used, should be supplied by the deployment platform's secret manager/environment configuration and never committed to Git:
- `OPENAI_API_KEY`
- `PERPLEXITY_API_KEY`

## Cost/context controls
- Repository facts: inspect GitHub first; do not call Perplexity.
- Current external facts: Perplexity.
- Implementation: Codex.
- Independent review: separate OpenAI context/pass.
- Persist concise artifacts so later runs retrieve relevant context instead of replaying conversations.

## Fallback
If Perplexity is unavailable, pause freshness-dependent research or use another explicitly approved web-research provider. If OpenAI/Codex is unavailable, do not silently switch provider for write operations; record the blocked state or use an explicitly approved adapter.
