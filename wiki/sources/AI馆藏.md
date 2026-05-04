---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/
tags:
  - collection/ai
  - source/catalog
---

# AI馆藏

## 来源

- 来源路径：`AI/`
- 范围：排除 `.DS_Store` 后，共 36 个可摄入文件。
- 格式：25 个 PDF、9 个 PPTX、2 个 Markdown。
- PDF 页数扫描：本地 `pypdf` 成功读取全部 25 个 PDF，共 3,067 页。
- PPTX 抽取：本地解析 9 个 PPTX，共 674 张幻灯片。
- 摄入深度：已完成目录级摄入、核心材料综合，以及 25 个 PDF 的单文件深度来源页。单个长 PDF 的逐章/逐页笔记仍可后续继续拆分。

## 一句话总结

`AI/` 是本仓库的人工智能核心资料区，覆盖 Agent Harness、OpenClaw、Claude Skills、大语言模型论文、LLM 教材/PPT、Agent 趋势报告和企业 AI 组织报告。

## 馆藏结构

| 目录 | 文件数 | 读取信息 | 作用 |
|---|---:|---|---|
| Paper | 12 | 12 PDF，534 页 | LLM、RAG、推理、Agent、模型报告和系统论文 |
| 图书 | 12 | 4 PDF 1,864 页；8 PPTX 644 张幻灯片 | LLM 教材、Agent 图书、大模型理论课程 |
| 报告 | 5 | 4 PDF 442 页；1 PPTX 30 张幻灯片 | Agentic Coding、AI 趋势、企业 AI 人才与组织、Agent 技术分享 |
| Harness | 2 | 2 PDF，139 页 | Claude Code/Codex Harness 工程比较 |
| Openclaw | 2 | 1 Markdown；1 PDF 22 页 | OpenClaw 本地 Agent Runtime 原理 |
| Skills | 2 | 2 PDF，66 页 | Claude Skills 构建指南 |
| Article | 1 | 1 Markdown | Agent Harness 解剖 |

## 关键材料

- Agent Harness：`AI/Article/The-Anatomy-of-an-Agent-Harness-LangChain.md`、`AI/Harness/book1-claude-code.pdf`、`AI/Harness/book2-comparing.pdf`。
- OpenClaw：`AI/Openclaw/OpenClaw 万字原理深度分析.md`、`AI/Openclaw/OpenClaw实现原理与模块拆解.pdf`。
- LLM 基础论文：`Attention Is All You Need.pdf`、`GPT-4 Technical Report.pdf`、`The Llama 3 Herd of Models.pdf`、`Qwen Technical Report.pdf`、`DeepSeek LLM Scaling...pdf`、`DeepSeek_R1.pdf`、`Apple Intelligence Foundation Language Models.pdf`。
- Agent/RAG 论文：`REACT.pdf`、`From Local to Global- A GraphRAG Approach...pdf`、`斯坦福小镇论文.pdf`。
- 技能系统：`The-Complete-Guide-to-Building-Skill-for-Claude.pdf` 及中文无水印版。
- 课程体系：`大规模语言模型：从理论到实践` 两版 PDF 和 8 章 PPT。
- 趋势报告：`2026 Agentic Coding Trends Report.pdf`、`AI年度报告（2025-2026）`、`云器AI Agent开发技术分享20260114.pptx`。

## PDF 深度来源页

本轮已为 `AI/` 下 25 个 PDF 建立单文件来源页，详见 [[AI PDF深度摄入总览]]。

### Agent Runtime 与工具系统

- [[AI PDF - Claude Code Harness Engineering 设计指南]]
- [[AI PDF - Claude Code 与 Codex Harness 设计哲学比较]]
- [[AI PDF - OpenClaw 实现原理与模块拆解]]
- [[AI PDF - ReAct Reasoning and Acting]]
- [[AI PDF - Generative Agents 英文版]]
- [[AI PDF - Generative Agents 中文译本]]
- [[AI PDF - Claude Skills 构建指南 中文版]]
- [[AI PDF - The Complete Guide to Building Skills for Claude]]
- [[AI PDF - Hello Agents 从零构建智能体系统]]

### LLM 基础、训练与模型报告

- [[AI PDF - Attention Is All You Need]]
- [[AI PDF - GPT-4 Technical Report]]
- [[AI PDF - The Llama 3 Herd of Models]]
- [[AI PDF - Qwen Technical Report]]
- [[AI PDF - DeepSeek LLM Scaling Open-Source Language Models with Longtermism]]
- [[AI PDF - DeepSeek-R1 强化学习推理模型]]
- [[AI PDF - Apple Intelligence Foundation Language Models]]
- [[AI PDF - Competitive Programming with Large Reasoning Models]]
- [[AI PDF - 大语言模型 RUC AI Box]]
- [[AI PDF - 大语言模型从理论到实践 第二版]]
- [[AI PDF - 大规模语言模型从理论到实践 第一版]]

### RAG、趋势与组织报告

- [[AI PDF - GraphRAG Query-Focused Summarization]]
- [[AI PDF - 2026 Agentic Coding Trends Report]]
- [[AI PDF - 2026 年 AI 与数据发展预测]]
- [[AI PDF - 2026 中国企业 AI 人才与组织发展报告]]
- [[AI PDF - AI 年度报告 2025-2026 得到 AI 学习圈]]

## 需要更新的链接

- [[AI]]
- [[AI Agent Runtime]]
- [[大语言模型]]
- [[AI学习路线]]
- [[Agent Harness与OpenClaw深度摄入]]
- [[大语言模型论文深度摄入]]
- [[AI PDF深度摄入总览]]

## 矛盾或张力

- 本目录既包含论文、课程、报告，也包含项目分析和技能指南。后续需要把“研究结论”“工程方法”“趋势判断”分层处理。
- 部分报告涉及 2026 趋势预测，属于时效性材料；后续查询时应标注其预测性质。

## 待解决问题

- 是否继续把 9 个 PPTX 拆成课程章节页？
- 是否为 `AI/Article/The-Anatomy-of-an-Agent-Harness-LangChain.md` 和 `AI/Openclaw/OpenClaw 万字原理深度分析.md` 建立单文件深度来源页？
- 是否把 25 个 PDF 来源页进一步抽象成“推理模型”“工具调用”“Agent Memory”“AI 组织转型”等概念页？
