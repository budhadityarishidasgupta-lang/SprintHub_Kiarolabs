# Third-Party Skill / MCP / Agent Intake

Never install or execute a repository merely because it is popular.

## Intake checklist
- [ ] Confirm canonical upstream repository and maintainer.
- [ ] Record license and compatibility with intended use.
- [ ] Pin a tag or commit SHA before adoption.
- [ ] Inspect executable hooks, install scripts, CI workflows and package scripts.
- [ ] Inspect MCP/tool permissions and network/file-system access.
- [ ] Search for secrets, credential collection, telemetry and unexpected external endpoints.
- [ ] Review dependencies and lockfiles for supply-chain risk.
- [ ] Identify prompt-injection or arbitrary-command surfaces.
- [ ] Test in isolated sandbox with no production credentials.
- [ ] Extract only the capability required; prefer adaptation over wholesale vendoring.
- [ ] Record provenance and local modifications.
- [ ] Require independent security review before enabling execution.

## Classification
REFERENCE — documentation/inspiration only.
ADAPTED — selected concepts/content rewritten into this harness.
VENDORED — source copied and pinned; requires license/provenance record.
EXECUTABLE — code/hooks/tools enabled; requires security approval.

The upstream registry defaults new discoveries to REFERENCE.
