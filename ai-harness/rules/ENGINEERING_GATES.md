# Engineering Gates

These gates apply to every project using this harness.

## Gate 0 — Intake
Do not code from a vague request. Create or update a feature specification first.

## Gate 1 — Research
Use Perplexity when the decision depends on current external facts, libraries, APIs, market information or documentation. Store conclusions and source links, not raw research dumps.

## Gate 2 — Architecture
OpenAI reasoning reviews scope, existing architecture, data model, API impact, security, cost and rollback. Prefer the smallest reversible change.

## Gate 3 — Implementation
Codex implements only the approved scope. It must inspect the existing repository before changing code and preserve unrelated behavior.

## Gate 4 — Deterministic verification
Run available unit, integration, lint, type, build and migration checks. Model opinion is not a substitute for executable tests.

## Gate 5 — Independent review
A separate OpenAI review pass checks the diff and evidence. The implementation pass cannot approve itself.

## Gate 6 — Security
Check authentication, authorization, secrets, input validation, dependency changes, data exposure, prompt injection surfaces, MCP/tool permissions and destructive operations.

## Gate 7 — Sandbox/UAT
Deploy to a non-production target first. Run acceptance criteria and regression scenarios. Record evidence and unresolved defects.

## Gate 8 — Human production approval
Production release requires explicit human approval. Never infer approval from silence or successful sandbox tests.

## Gate 9 — Release and rollback
Release only the reviewed commit. Verify health after deployment. If release criteria fail, execute the documented rollback.

## Gate 10 — Memory
Persist architecture decisions, incidents, useful patterns and lessons. Do not persist secrets, credentials or unnecessary personal data.
