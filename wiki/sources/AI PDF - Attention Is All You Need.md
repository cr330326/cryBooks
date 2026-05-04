---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/Attention Is All You Need.pdf
tags:
  - collection/ai
  - ai/llm
  - ai/transformer
---

# AI PDF - Attention Is All You Need

## 来源

- 来源路径：`AI/Paper/Attention Is All You Need.pdf`
- 抽取质量：PDF 共 15 页；可抽取文本页 15 页；约 39,612 个抽取字符。
- 目录线索：Introduction；Background；Model Architecture；Encoder and Decoder Stacks；Attention；Scaled Dot-Product Attention；Multi-Head Attention；Applications of Attention in our Model

## 一句话总结

Transformer 原论文提出完全基于注意力的序列建模架构，用 self-attention、multi-head attention、position-wise feed-forward 与 positional encoding 替代循环和卷积。

## 深度摄入

- 核心贡献是把序列依赖建模交给自注意力，使长距离依赖路径更短，也更适合并行训练。
- encoder-decoder 架构由多层 attention 和前馈网络堆叠而成，decoder 通过 masked self-attention 保持自回归生成约束。
- multi-head attention 让模型在多个子空间中并行关注不同关系，是后续 LLM 架构的基础组件。
- 它是本 AI 书库的地基层来源，后续 GPT、Llama、Qwen、DeepSeek、Apple AFM 等报告都可回链到这里。

## 需要更新的链接

- [[大语言模型]]
- [[大语言模型论文深度摄入]]
- [[AI学习路线]]

## 使用边界

原文面向机器翻译任务，不能直接等同于现代 LLM 的完整训练体系；现代 LLM 还叠加了规模化数据、后训练、工具和安全层。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
