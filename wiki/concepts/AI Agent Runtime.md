---
type: concept
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - wiki/sources/AI馆藏.md
  - wiki/syntheses/Agent Harness与OpenClaw深度摄入.md
  - AI/Article/The-Anatomy-of-an-Agent-Harness-LangChain.md
  - AI/Openclaw/OpenClaw 万字原理深度分析.md
tags:
  - ai/agent-runtime
  - ai/harness
---

# AI Agent Runtime

## 概要

AI Agent Runtime 是把“只能生成文本的模型”变成“能持续执行任务的系统”的运行层。它通常包含控制面、工具系统、文件系统、沙盒、状态管理、记忆、上下文压缩、权限、验证和长期运行机制。

## 核心判断

- Agent 不是模型本身，而是 `Model + Harness`。
- Harness 是模型外的一切工程结构：系统提示、工具、技能、MCP、文件系统、沙盒、浏览器、编排逻辑、hooks、压缩、验证和恢复。
- OpenClaw 把 Agent Runtime 进一步本地化：Gateway 是控制面，Workspace/Agent 是执行单元，Skills 是手脚，Memory 是长期状态。
- 真正可靠的 Agent 不是“更会说”，而是拥有可审计、可恢复、可验证、可授权的执行闭环。

## 关键组件

- 控制面：Gateway、会话管理、路由、认证、日志。
- 执行循环：ReAct/Agent Loop，Reason -> Act -> Observe -> Repeat。
- 工具层：shell、filesystem、browser、email、calendar、skills、MCP。
- 状态层：文件系统、AGENTS/CLAUDE 文档、长期记忆、RAG/BM25。
- 安全层：沙盒、权限最小化、allowlist、pairing code、审计日志。
- 长期运行：cron、heartbeat、后台 agent、自恢复循环。

## 相关页面

- [[Agent Harness与OpenClaw深度摄入]]
- [[AI]]
- [[论文]]
- [[效能]]

