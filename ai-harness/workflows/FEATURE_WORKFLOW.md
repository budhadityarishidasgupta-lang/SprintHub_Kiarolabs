# New Feature Workflow

## Required artifacts
1. Feature specification
2. Research note when current external evidence is required
3. Architecture/implementation plan
4. Implementation diff
5. Automated test/build evidence
6. Independent QA result
7. Security result
8. Sandbox/UAT evidence
9. Human production approval
10. Release + memory update

## State machine
`INTAKE -> SPECIFIED -> RESEARCHED(if needed) -> ARCHITECTED -> BUILDING -> VERIFIED -> REVIEWED -> SECURITY_CLEARED -> UAT -> APPROVED -> RELEASED -> LEARNED`

Any blocking failure returns the task to the responsible earlier state.

## Handoff contract
Every handoff includes:
- objective
- approved scope
- explicit exclusions
- relevant repository/context
- acceptance criteria
- evidence produced so far
- unresolved risks/questions

## Research routing
Use Perplexity only when freshness/external evidence materially matters. Do not spend research calls on facts available in the repository or stable engineering knowledge.

## Build routing
Codex receives the approved spec, relevant `.ai-context` memory, architecture plan and exact repository/branch. It should not receive an entire historical conversation when structured artifacts suffice.

## Review routing
QA receives the spec + diff + evidence, not the Builder's reasoning transcript. This reduces anchoring and preserves independence.

## Production rule
Sandbox success is necessary but not sufficient for production. A human explicitly approves production after reviewing UAT and release evidence.
