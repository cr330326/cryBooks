---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/From Local to Global- A GraphRAG Approach to  Query-Focused Summarization.pdf
tags:
  - collection/ai
  - ai/rag
  - ai/graph
---

# AI PDF - GraphRAG Query-Focused Summarization

## 来源

- 来源路径：`AI/Paper/From Local to Global- A GraphRAG Approach to  Query-Focused Summarization.pdf`
- 抽取质量：PDF 共 26 页；可抽取文本页 26 页；约 89,639 个抽取字符。
- 目录线索：Introduction；Background；RAG Approaches and Systems；Using Knowledge Graphs with LLMs and RAG；Adaptive benchmarking for RAG Evaluation；RAG evaluation criteria；Methods；GraphRAG Workflow

## 一句话总结

GraphRAG 提出从文档块抽取实体与关系，构建知识图谱和社区摘要，再用于回答全局性、综合性问题，以补足普通向量 RAG 在全局问题上的短板。

## 深度摄入

- 传统 vector RAG 擅长局部事实检索，但面对“整个语料总体说了什么”这类问题时，单点相似度召回不够。
- GraphRAG 的工作流是文档切块、实体关系抽取、知识图谱构建、社区发现、社区摘要和查询时聚合。
- 社区摘要相当于语料的分层自记忆，使系统可以从局部证据逐步上升到全局综合。
- 对本 wiki 的启发很直接：馆藏页像全局目录，单篇来源页像局部节点，综合页像社区摘要。

## 需要更新的链接

- [[大语言模型]]
- [[AI学习路线]]
- [[AI Agent Runtime]]

## 使用边界

GraphRAG 增强全局总结但成本更高，且依赖实体抽取和社区摘要质量；不能替代来源级核验。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
