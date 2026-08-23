# Standard Engineering Workflow

## 0. Intake
Capture goal, user outcome, constraints, environment and explicit production restrictions.

## 1. Research
Perplexity researches only the external facts that can materially affect the design. Prefer primary/official sources. Store conclusions and links in the feature research note.

## 2. Specify
OpenAI creates the feature specification: problem, scope, non-goals, user stories, acceptance criteria, data/privacy requirements and definition of done.

## 3. Clarify
Resolve material ambiguity. Do not invent business rules where an unresolved choice can alter data, security, cost or user experience.

## 4. Architect
OpenAI reasoning creates the technical plan, interfaces, DB changes, dependencies, migration, test strategy and rollback.

## 5. Build
Codex implements the bounded task. Builder must not broaden scope or deploy production implicitly.

## 6. Test
Run deterministic tests first. Add integration/e2e tests when appropriate. Capture evidence rather than relying on agent assertions.

## 7. Independent review
A separate OpenAI review checks the diff against the specification and acceptance criteria.

## 8. Security gate
Check secrets, auth/authz, data exposure, injection, dependencies, hooks/MCPs, unsafe shell/network behavior and configuration drift.

## 9. Sandbox/UAT
Deploy only to the designated non-production environment. Run smoke tests and user acceptance tests.

## 10. Release gate
Require explicit production approval, known rollback path and migration readiness.

## 11. Remember
Update durable project context: architecture decisions, known issues, lessons learned and reusable skills/rules.

## Definition of done
A feature is not done because code exists. It is done when acceptance criteria pass, deterministic tests pass, independent review is clear, security gate is clear, UAT is accepted, documentation is updated and rollback is understood.
