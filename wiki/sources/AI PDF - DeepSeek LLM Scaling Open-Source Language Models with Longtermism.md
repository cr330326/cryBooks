---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/DeepSeek LLM Scaling Open-Source Language Models with Longtermism.pdf
tags:
  - collection/ai
  - ai/llm
  - ai/scaling
---

# AI PDF - DeepSeek LLM Scaling Open-Source Language Models with Longtermism

## 来源

- 来源路径：`AI/Paper/DeepSeek LLM Scaling Open-Source Language Models with Longtermism.pdf`
- 抽取质量：PDF 共 48 页；可抽取文本页 48 页；约 112,663 个抽取字符。
- 目录线索：Introduction；Pre-Training；Data；Architecture；Hyperparameters；Infrastructures；Scaling Laws；Scaling Laws for Hyperparameters

## 一句话总结

DeepSeek LLM 报告围绕开源语言模型的预训练、数据、架构、基础设施、scaling laws、对齐和评估展开，强调长期主义地建设开放模型能力。

## 深度摄入

- 报告把数据、架构、训练超参、基础设施和 scaling laws 放在同一条工程链路中，说明模型能力来自系统性配方而不是单点技巧。
- scaling law 部分用于估计模型和数据的最优扩展关系，是理解 DeepSeek 后续推理模型路线的重要前置材料。
- 对齐部分连接 SFT/RLHF 或偏好优化，使 base model 进入可交互助手形态。
- 适合与 DeepSeek-R1 对读：前者解释基础模型如何扩展，后者解释推理能力如何通过强化学习被激发。

## 需要更新的链接

- [[大语言模型]]
- [[大语言模型论文深度摄入]]

## 使用边界

报告以模型家族技术说明为主，评估结果应结合发布时间和当时基准理解；不要直接外推到后续模型。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
