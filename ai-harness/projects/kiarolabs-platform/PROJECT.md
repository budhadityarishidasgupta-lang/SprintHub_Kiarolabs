# Project: KiaroLabs Platform

## Identity
- PROJECT_ID: `kiarolabs-platform`
- Type: product
- Status: active

## Objective
Develop, validate and release KiaroLabs learning-platform capabilities without treating the universal harness itself as KiaroLabs-specific.

## Repository scope
The exact KiaroLabs repository or repositories must be selected per task. The registry identifies the platform family; a task must not assume every KiaroLabs repository is writable.

## Environment boundary
- Prefer sandbox/test for implementation validation and UAT.
- Production changes require explicit human approval.
- A production service being similar to a test service does not make production an implicit test target.

## Core rules
1. Preserve existing production functionality unless the approved specification explicitly changes it.
2. Keep authentication, membership, learner data and admin boundaries explicit.
3. Do not reuse project secrets outside KiaroLabs.
4. Require rollback for production-affecting migrations or releases.
5. Store KiaroLabs-specific architecture and lessons only under this project namespace.

## Required gates
Specification -> architecture -> build -> deterministic tests -> independent QA -> security review -> sandbox/UAT -> human production approval -> release -> memory update.
