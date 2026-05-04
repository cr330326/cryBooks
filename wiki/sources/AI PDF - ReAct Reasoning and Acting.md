---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/REACT.pdf
tags:
  - collection/ai
  - ai/agent-runtime
  - ai/reasoning
---

# AI PDF - ReAct Reasoning and Acting

## 来源

- 来源路径：`AI/Paper/REACT.pdf`
- 抽取质量：PDF 共 33 页；可抽取文本页 33 页；约 110,022 个抽取字符。
- 目录线索：1 Introduction；2 ReAct: Synergizing Reasoning + Acting；3 Knowledge-Intensive Reasoning Tasks；3.1 Setup；3.2 Methods；3.3 Results and Observations；4 Decision Making Tasks；5 Related Work

## 一句话总结

ReAct 提出让语言模型交替生成 reasoning trace 与 task-specific action，使内部推理和外部行动互相校正，成为现代工具型 agent 的基础范式之一。

## 深度摄入

- ReAct 的关键不是单纯 CoT，也不是单纯 action generation，而是 Thought/Action/Observation 的交替循环。
- 在 HotpotQA、Fever、ALFWorld、WebShop 等任务中，ReAct 通过外部观察减少幻觉，并通过推理轨迹改善行动选择。
- 它解释了为什么 agent 需要工具反馈：模型的内部知识不稳定，外部环境观察可以更新状态。
- 对本仓库的 agent schema 来说，ReAct 是摄入、查询、健康检查工作流背后的基本模式：思考、行动、观察、修正。

## 需要更新的链接

- [[AI Agent Runtime]]
- [[大语言模型论文深度摄入]]
- [[AI学习路线]]

## 使用边界

ReAct prompt 示例和抽取文本中部分图示乱码；核心方法清楚，但具体实验数字需要回原 PDF 表格核验。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
