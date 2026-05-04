---
type: synthesis
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Article/The-Anatomy-of-an-Agent-Harness-LangChain.md
  - AI/Openclaw/OpenClaw 万字原理深度分析.md
  - AI/Openclaw/OpenClaw实现原理与模块拆解.pdf
  - AI/Harness/book1-claude-code.pdf
  - AI/Harness/book2-comparing.pdf
tags:
  - ai/agent-runtime
  - ai/harness
  - deep-ingest
---

# Agent Harness与OpenClaw深度摄入

## 核心结论

Agent 的关键不是“模型更聪明”，而是模型外部的 Harness 是否能把智能约束成可靠工作流。Harness 提供持久状态、工具执行、沙盒权限、上下文管理、恢复机制和验证闭环；OpenClaw 则把这一套运行时本地化，形成以 Gateway 为中心的个人 AI 控制面。

## Agent = Model + Harness

`The Anatomy of an Agent Harness` 明确提出：Agent 等于模型加 Harness。模型本身主要输入多模态数据、输出文本；它不会天然维护长期状态、执行代码、访问实时知识、安装依赖或完成环境配置。这些都是 Harness 级能力。

Harness 包括系统提示词、工具/技能/MCP、文件系统、沙盒、浏览器、子 Agent 编排、模型路由、handoff、上下文压缩、继续执行、lint/test hooks 等。

## Harness 的工程原语

- 文件系统：持久存储、上下文卸载、跨会话状态、人与多个 Agent 的协作表面。
- Bash/代码执行：通用工具，让模型能按需生成临时工具，而不是依赖预制工具清单。
- 沙盒：隔离执行、权限约束、可扩展环境、预装运行时和测试工具。
- 记忆与搜索：通过文件标准和搜索/MCP 做持续学习与新知识注入。
- 上下文治理：压缩、工具输出卸载、技能渐进披露，缓解 context rot。
- 长任务执行：计划、状态、验证、恢复和继续循环，支撑跨上下文窗口的工作。

## OpenClaw 的 Runtime 化实现

OpenClaw 将 Agent Runtime 设计为本地优先的 Hub-and-Spoke 架构：

- Gateway 是单一控制面，负责认证、路由、日志、会话管理和 WebSocket 控制平面。
- Channels 连接 WhatsApp、Telegram、微信、Slack 等用户入口，并把消息标准化。
- Workspace/Agent 是执行单元，加载记忆、系统提示和历史，调用模型并驱动工具链。
- Skills 是执行能力层，包含文件系统、shell、浏览器、email、calendar、web-search 等。
- Memory 由 SOUL/IDENTITY、短期会话和长期 RAG/BM25 组成。
- Cron/Heartbeat 让 Agent 从被动回复走向主动执行。

## 两条路线的合流

Claude Code/Codex Harness 材料强调“控制流、权限、恢复、验证、制度层”；OpenClaw 强调“本地 Gateway、渠道原生、技能系统、长期记忆和主动性”。二者合起来指向同一个原则：可靠 Agent 的核心是运行时治理，而不是单次回复质量。

## 对本知识库的启发

- `wiki/` 就是 Agent 的长期记忆和协作表面。
- `CLAUDE.md`/`AGENT.md` 是 Harness 注入的制度层。
- 摄入/查询/健康检查是固定工作流，等价于工具化的执行闭环。
- 每轮完成后必须更新索引和日志，这是可恢复、可审计的关键。
- 深度摄入应引入验证步骤：来源可读性、frontmatter、双链、索引覆盖、断链检查。

## 后续问题

- 是否把本 wiki 的摄入流程进一步拆成可复用 Skills？
- 是否建立“Agent Runtime 架构模式”专题页，对比 Claude Code、Codex、OpenClaw、LangChain/ReAct？

