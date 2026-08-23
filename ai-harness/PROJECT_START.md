# Project Start Protocol

Use this at the beginning of every harness-driven task.

## Required declaration

```text
PROJECT_ID: <registered project id>
TASK: <desired outcome>
ENVIRONMENT: local | sandbox | test | production
REPOSITORY: <repo in project scope>
PRODUCTION_CHANGE_ALLOWED: yes | no
```

For security-testing projects also declare:

```text
AUTHORIZED_TARGET: <explicit target or local fixture>
AUTHORIZATION_BASIS: owned | explicit permission | local fixture
RESOURCE_LIMIT: <task-specific limit>
```

## Resolver behavior

1. Match PROJECT_ID to `PROJECT_REGISTRY.md`.
2. Load `projects/<PROJECT_ID>/PROJECT.md`.
3. Validate repository and environment against that profile.
4. Load only that project's relevant memory/specification.
5. Reject or clarify any cross-project assumption.
6. Proceed through `WORKFLOW.md`.

## Convenience interaction

A human does not need to type the full declaration every time. Natural-language requests such as "use the AFL++ project in my sandbox" or "this is for KiaroLabs verbal reasoning" may be resolved to a registered PROJECT_ID when unambiguous. Before a state-changing action, the resolved project/environment must be made explicit in the working record.
