# Project Memory Schema

Keep memory concise and retrieval-friendly. Each project may maintain these files under `.ai-context/`.

## architecture.md
Current system boundaries, services, data stores, deployment targets and critical integrations.

## decisions.md
Append Architecture Decision Records:
- Date
- Decision
- Context
- Alternatives considered
- Why chosen
- Consequences
- Revisit trigger

## conventions.md
Repository-specific coding, testing, API, database and UI conventions.

## known-issues.md
Known defects, technical debt and workarounds with severity and owner/status where known.

## incidents.md
Production/sandbox incidents: symptom, cause, remediation and prevention.

## lessons.md
Reusable lessons from completed work. Promote broadly useful lessons into harness rules/skills.

## releases.md
Release date, commit/PR, environment, verification evidence and rollback reference.

## Memory hygiene
- Do not store secrets, tokens, passwords or private keys.
- Avoid unnecessary PII.
- Prefer facts and decisions over chat transcripts.
- Mark superseded decisions rather than silently deleting history.
- Retrieve only relevant memory for the current task to preserve context window quality.
