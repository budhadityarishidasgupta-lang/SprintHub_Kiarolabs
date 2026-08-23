# Upstream Registry

These projects are references, not trusted executable dependencies by default.

| Capability | Upstream | Intended use | Adoption |
|---|---|---|---|
| Agent harness | https://github.com/affaan-m/ECC | orchestration, skills, memory, security, research-first patterns | Adapt for OpenAI/Codex |
| Spec-driven development | https://github.com/github/spec-kit | constitution/spec/clarify/plan/tasks/analyze/implement flow | Adopt workflow |
| Specialist roles | https://github.com/garrytan/gstack | product/engineering/review/QA/release role separation | Adapt concepts |
| Reusable skills | https://github.com/vercel-labs/agent-skills | focused reusable agent capabilities | Curate only |
| MCP catalogue | https://github.com/punkpeye/awesome-mcp-servers | connector discovery | Reference only; audit each server |
| Visual agent workflows | https://github.com/langgenius/dify | visual orchestration/RAG/workflow patterns | Reference/selective use |
| Coding executor | https://github.com/openai/codex | primary implementation agent | Preferred executor |
| UI/UX skills | https://github.com/nextlevelbuilder/ui-ux-pro-max-skill | UI/UX review and design patterns | Review before adaptation |

## Supply-chain gate

Before copying/installing any upstream component: verify canonical repository -> inspect license -> inspect maintainer/activity -> inspect prompts/scripts/hooks/MCP permissions -> scan for secrets/network/shell behavior -> sandbox test -> pin reviewed version/commit -> document attribution and modifications.

Never run an upstream installer merely because a social post recommends it.
