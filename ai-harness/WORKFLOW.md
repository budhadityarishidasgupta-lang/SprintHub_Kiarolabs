# Universal Engineering Workflow

## -1. Project select
Resolve `PROJECT_ID` from the project registry. Load the project profile, repositories, environments, constraints, authorization boundaries and project memory. If no project is resolved, stay read-only.

## 0. Intake
Capture goal, user outcome, constraints, environment, risk class and explicit production restrictions for the selected project.

## 1. Research
Perplexity researches only external facts that can materially affect the design. Prefer primary/official sources. Store conclusions and links in the active project's feature research note.

## 2. Specify
OpenAI creates the feature specification: problem, scope, non-goals, user stories, acceptance criteria, data/privacy requirements and definition of done.

## 3. Clarify
Resolve material ambiguity. Do not invent business rules where an unresolved choice can alter data, security, cost or user experience.

## 4. Architect
OpenAI reasoning creates the technical plan, interfaces, DB changes, dependencies, migration, test strategy and rollback within project boundaries.

## 5. Build
Codex implements the bounded task only in repositories authorized by the project profile. Builder must not broaden scope or deploy production implicitly.

## 6. Test
Run deterministic tests first. Add integration/e2e tests when appropriate. Capture evidence rather than relying on agent assertions.

## 7. Independent review
A separate OpenAI review checks the diff against the specification, acceptance criteria and project profile.

## 8. Security gate
Check secrets, auth/authz, data exposure, injection, dependencies, hooks/MCPs, unsafe shell/network behavior, authorization boundaries and configuration drift.

## 9. Sandbox/UAT
Use the designated non-production environment when one exists. Run smoke tests and user acceptance tests. For authorized security-testing projects, operate only against targets explicitly listed in the project profile.

## 10. Release gate
Require explicit production approval, known rollback path and migration readiness. Never infer approval from prior projects.

## 11. Remember
Update only the active project's durable context: architecture decisions, known issues, incidents, lessons learned and reusable candidates. Promote a lesson to universal harness memory only after confirming it is project-agnostic.

## Definition of done
A task is not done because code exists. It is done when project-specific acceptance criteria pass, deterministic tests pass, independent review is clear, security gate is clear, required UAT is accepted, documentation is updated and rollback is understood.
