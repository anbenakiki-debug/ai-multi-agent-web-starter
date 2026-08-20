# AI Multi-Agent Website Development Starter

一套可直接放进网站项目的 AI 多 Agent 开发规范：GitHub Issues、Projects、PR 和 Actions 保存交付状态；项目文档保存需求、架构、风险和决策；人类负责关键审批。

从这里开始：[`GUIDE.md`](GUIDE.md)

## 核心文件

- `AGENTS.md`：所有 Agent 的共用规则、状态来源与人工审批门。
- `.agents/agents/`：orchestrator、architect、frontend、backend、database、QA、reviewer 的职责。
- `.agents/skills/`：从需求分析、任务拆分到测试、审查、进度汇总的 10 个工作流。
- `.github/`：Feature/Bug Issue 模板、PR 模板和 Issue ↔ PR 关联检查。

## 建议的第一步

1. 填写 `PROJECT.md` 和 `REQUIREMENTS.md`。
2. 按 `GUIDE.md` 创建 GitHub Project。
3. 让 orchestrator 将获批需求拆成 GitHub Issues，并仅分派状态为 Ready 的任务。
