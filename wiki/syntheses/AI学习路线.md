---
type: synthesis
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - wiki/sources/AI馆藏.md
  - wiki/syntheses/Agent Harness与OpenClaw深度摄入.md
  - wiki/syntheses/大语言模型论文深度摄入.md
tags:
  - collection/ai
  - learning-path
---

# AI学习路线

## 简短结论

当前 AI 资料最适合按四条线推进：LLM 基础、模型训练与评估、Agent Runtime、产业趋势与组织落地。若目标是增强本知识库的 agent 维护能力，应优先深度摄入 Agent Runtime 线。

## 路线一：LLM 基础

1. Transformer：`AI/Paper/Attention Is All You Need.pdf`。
2. 教材总览：`AI/图书/LLMBook.pdf`、`AI/图书/大规模语言模型：从理论到实践/...pdf`。
3. PPT 课程：第 1-3 章，覆盖绪论、Transformer 基础、预训练数据。

## 路线二：训练、对齐与评估

1. 分布式训练：大模型理论与实践第 4 章 PPT。
2. SFT/提示/上下文学习：第 5 章 PPT。
3. RLHF/奖励模型/PPO：第 6 章 PPT。
4. 模型评估：第 8 章 PPT、GPT-4 Technical Report、GPTV System Card。
5. 推理强化学习：DeepSeek-R1、OpenAI 竞赛推理报告。

## 路线三：Agent Runtime 与工具系统

1. Agent Harness：`The-Anatomy-of-an-Agent-Harness-LangChain.md`。
2. Claude Code/Codex Harness：`AI/Harness/book1-claude-code.pdf`、`book2-comparing.pdf`。
3. ReAct：`AI/Paper/REACT.pdf`。
4. OpenClaw：`AI/Openclaw/OpenClaw 万字原理深度分析.md`、`OpenClaw实现原理与模块拆解.pdf`。
5. Skills：Claude Skills 构建指南。

## 路线四：RAG、知识库与长期记忆

1. GraphRAG：`From Local to Global- A GraphRAG Approach...pdf`。
2. LLM Wiki 方法：`llm-wiki.md`。
3. OpenClaw Memory：SOUL、IDENTITY、短期会话、长期 RAG/BM25。
4. 本仓库实践：`wiki/`、`CLAUDE.md`、`wiki/index.md`、`wiki/log.md`。

## 路线五：产业趋势与组织落地

1. `2026 Agentic Coding Trends Report.pdf`。
2. `2026 年 AI 与数据发展预测.pdf`。
3. `2026 年中国企业AI人才与组织发展报告...pdf`。
4. `AI年度报告（2025-2026）｜得到AI学习圈出品.pdf`。
5. `云器AI Agent开发技术分享20260114.pptx`。

## 下一步 Wiki 工作

- 把 `大规模语言模型：从理论到实践` 的 8 章 PPT 拆成课程章节页。
- 为 ReAct、GraphRAG、DeepSeek-R1、GPT-4 Technical Report 建立单篇深度来源页。
- 用 Claude Skills 指南反向改进本 wiki 的 agent skill/workflow 规范。

