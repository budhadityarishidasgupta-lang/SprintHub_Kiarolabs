# Project: AFL++ Point-and-Shoot

## Identity
- PROJECT_ID: `aflpp-point-shoot`
- Type: authorized security-testing
- Repository: `budhadityarishidasgupta-lang/AFLplusplus`
- Status: active

## Objective
Develop and validate a point-and-shoot security-testing workflow around AFL++ for systems the operator is explicitly authorized to test.

## Environment boundary
- Development: repository branch/worktree as defined per task.
- Test execution: isolated sandbox/test systems explicitly designated by the operator.
- Production: no implicit production testing or deployment.

## Hard authorization rules
1. A reachable host is not automatically an authorized target.
2. Before active testing, record the target and confirm it is owned by the operator or explicitly authorized for testing.
3. Default to sandbox/test targets.
4. Do not reuse KiaroLabs credentials, deployment assumptions, endpoints or memory unless a task explicitly selects an authorized KiaroLabs sandbox as the target.
5. Preserve evidence sufficient to reproduce findings and distinguish test artifacts from real incidents.
6. Resource/rate limits must be set for each target before sustained fuzzing or automated testing.

## Allowed by default
- Repository analysis and refactoring.
- Harness development.
- Test fixture creation.
- Local/unit/integration testing.
- Fuzzing of local fixtures and explicitly authorized sandbox targets.
- Defensive finding analysis and remediation guidance.

## Requires explicit target authorization in the task/profile
- Network interaction with a target system.
- Credentialed application testing.
- Sustained fuzzing against deployed services.
- Any action capable of materially degrading a shared environment.

## Prohibited by project default
- Unscoped third-party targets.
- Implicit production testing.
- Credential harvesting or persistence outside the approved test design.
- Cross-project secret or identity reuse.

## Required gates
Specification -> architecture -> deterministic harness tests -> independent QA -> security/scope review -> authorized sandbox validation -> human approval for any broader environment.

## Project memory
Store AFL++ architecture decisions, target-independent lessons, known issues and test evidence only under this project namespace.
