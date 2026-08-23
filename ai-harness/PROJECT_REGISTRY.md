# Project Registry

The harness is universal. This registry selects the project context for each run.

| PROJECT_ID | Project | Repository | Type | Default environment | Status |
|---|---|---|---|---|---|
| `kiarolabs-platform` | KiaroLabs platform | `budhadityarishidasgupta-lang/kiarolabs-Learning-platform` plus explicitly selected KiaroLabs service repos | product | sandbox/test | active |
| `aflpp-point-shoot` | AFL++ point-and-shoot authorized security testing | `budhadityarishidasgupta-lang/AFLplusplus` | security-testing | authorized sandbox/test target only | active |

## Selection rules

1. Every state-changing run declares exactly one `PROJECT_ID`.
2. A project may reference multiple repositories, but only those explicitly listed in its profile are writable.
3. Cross-project changes require separate runs/specifications unless an explicit integration task authorizes both sides.
4. Project memory never automatically flows into another project.
5. Universal lessons may be promoted to the base harness only after review.
6. Adding a new project requires a project profile based on `PROJECT_PROFILE_TEMPLATE.md`.

## Invocation examples

- `PROJECT_ID=kiarolabs-platform` — load KiaroLabs product/deployment context.
- `PROJECT_ID=aflpp-point-shoot` — load only the authorized security-testing profile and its target restrictions.
- A new HR automation, personal tool, SaaS product or research project gets its own PROJECT_ID and profile without changing the base harness.
