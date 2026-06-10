# Agents Workflow

一个用于新项目启动和长期维护的 Agent 工作流模板。

本 README 只是模板首次说明；派生项目可以完全覆盖为自己的项目介绍。

## 使用

1. 从本仓库创建 GitHub Template repository。
2. 保留 `AGENTS.md`、`.agents/skills/`、`.codex/agents/`。
3. 把项目目标写给主 agent；复杂任务先用 `$flow-kickoff`。

## Skills

| Skill | 何时使用 |
| --- | --- |
| `$flow-goal` | 把模糊想法生成可复制的 goal prompt。 |
| `$flow-research` | 联网搜索、核验当前事实、更新 `docs/websearch/index.md`。 |
| `$flow-kickoff` | 新项目、重大功能、架构决策、多 Sprint 任务。 |
| `$flow-maintenance` | 已交付项目的新需求、问题、CR、回归和维护账本。 |
| `$flow-review` | Git diff、PR、提交前风险和测试缺口审查。 |

## Agents

| Agent | 模型 | 思考等级 | 作用 |
| --- | --- | --- | --- |
| `architect` | `gpt-5.5` | `xhigh` | 主架构师和调度者，负责拆分、分派、合成和最终判断。 |
| `planner` | `gpt-5.4` | `high` | 把需求整理成规格、风险和 Sprint 计划。 |
| `researcher` | `gpt-5.4-mini` | `medium` | 核验当前事实和外部资料。 |
| `implementer` | `gpt-5.4-mini` | `medium` | 按 Sprint 契约实施边界清晰的改动。 |
| `fast-editor` | `gpt-5.3-codex-spark` | `high` | 处理低风险、短上下文、可验证的局部编辑。 |
| `evaluator` | `gpt-5.4-mini` | `high` | 验证行为、失败路径、回归风险和验收标准。 |
| `reviewer` | `gpt-5.4-mini` | `high` | 做 Git 审查和提交前风险扫描。 |

## 目录

- `AGENTS.md`：仓库级强制规则。
- `.agents/skills/`：可复用 workflow。
- `.codex/agents/`：项目级运行角色配置。
- `docs/websearch/index.md`：联网研究索引。
