# Reusable Skill Contract

Every local skill should be small, auditable and provider-portable.

## Metadata
- Name:
- Purpose:
- Version:
- Owner:
- Upstream/provenance:
- Classification: ADAPTED | LOCAL | VENDORED

## Trigger
Describe exactly when the skill should be used and when it should not.

## Inputs
List required and optional inputs. Never require secrets unless the runtime integration explicitly needs them.

## Procedure
Numbered deterministic steps. Separate repository inspection, reasoning, mutations and verification.

## Outputs
Define the expected artifact/result schema.

## Verification
State how the output is checked independently.

## Permissions
Declare required tools, filesystem paths, network destinations and write permissions. Default deny anything not declared.

## Failure behavior
Fail closed for ambiguous destructive actions, missing credentials, failed tests, security findings or production writes without approval.

## Provider portability
Do not encode Claude-specific commands or assumptions in the core contract. Provider adapters may translate this contract for Codex/OpenAI or another approved runtime.
