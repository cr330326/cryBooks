---
type: synthesis
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - wiki/sources/AI馆藏.md
  - wiki/syntheses/AI PDF深度摄入总览.md
  - wiki/syntheses/Agent Harness与OpenClaw深度摄入.md
  - wiki/syntheses/大语言模型论文深度摄入.md
tags:
  - collection/ai
  - learning-path
---

# AI学习路线

## 简短结论

当前 AI 资料最适合按四条线推进：LLM 基础、模型训练与评估、Agent Runtime、产业趋势与组织落地。25 个 PDF 已完成单文件深度来源页，后续应优先拆 PPTX 课程章节和抽取稳定概念页。

## 路线一：LLM 基础

1. Transformer：[[AI PDF - Attention Is All You Need]]。
2. 教材总览：[[AI PDF - 大语言模型 RUC AI Box]]、[[AI PDF - 大语言模型从理论到实践 第二版]]、[[AI PDF - 大规模语言模型从理论到实践 第一版]]。
3. PPT 课程：第 1-3 章，覆盖绪论、Transformer 基础、预训练数据。

## 路线二：训练、对齐与评估

1. 分布式训练：大模型理论与实践第 4 章 PPT。
2. SFT/提示/上下文学习：第 5 章 PPT。
3. RLHF/奖励模型/PPO：第 6 章 PPT。
4. 模型评估：第 8 章 PPT、[[AI PDF - GPT-4 Technical Report]]、GPTV System Card。
5. 推理强化学习：[[AI PDF - DeepSeek-R1 强化学习推理模型]]、[[AI PDF - Competitive Programming with Large Reasoning Models]]。

## 路线三：Agent Runtime 与工具系统

1. Agent Harness：`The-Anatomy-of-an-Agent-Harness-LangChain.md`。
2. Claude Code/Codex Harness：[[AI PDF - Claude Code Harness Engineering 设计指南]]、[[AI PDF - Claude Code 与 Codex Harness 设计哲学比较]]。
3. ReAct：[[AI PDF - ReAct Reasoning and Acting]]。
4. OpenClaw：`AI/Openclaw/OpenClaw 万字原理深度分析.md`、[[AI PDF - OpenClaw 实现原理与模块拆解]]。
5. Skills：[[AI PDF - Claude Skills 构建指南 中文版]]、[[AI PDF - The Complete Guide to Building Skills for Claude]]。

## 路线四：RAG、知识库与长期记忆

1. GraphRAG：[[AI PDF - GraphRAG Query-Focused Summarization]]。
2. LLM Wiki 方法：`llm-wiki.md`。
3. OpenClaw Memory：SOUL、IDENTITY、短期会话、长期 RAG/BM25。
4. 本仓库实践：`wiki/`、`CLAUDE.md`、`wiki/index.md`、`wiki/log.md`。

## 路线五：产业趋势与组织落地

1. [[AI PDF - 2026 Agentic Coding Trends Report]]。
2. [[AI PDF - 2026 年 AI 与数据发展预测]]。
3. [[AI PDF - 2026 中国企业 AI 人才与组织发展报告]]。
4. [[AI PDF - AI 年度报告 2025-2026 得到 AI 学习圈]]。
5. `云器AI Agent开发技术分享20260114.pptx`。

## 下一步 Wiki 工作

- 把 `大规模语言模型：从理论到实践` 的 8 章 PPT 拆成课程章节页。
- 为 `AI/Article/` 和 `AI/Openclaw/` 的 Markdown 来源建立单文件深度来源页。
- 用 Claude Skills 指南反向改进本 wiki 的 agent skill/workflow 规范。
