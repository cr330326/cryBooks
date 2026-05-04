---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/The Llama 3 Herd of Models.pdf
tags:
  - collection/ai
  - ai/llm
  - ai/model-report
---

# AI PDF - The Llama 3 Herd of Models

## 来源

- 来源路径：`AI/Paper/The Llama 3 Herd of Models.pdf`
- 抽取质量：PDF 共 92 页；可抽取文本页 92 页；约 356,341 个抽取字符。
- 目录线索：Introduction；General Overview；Pre-Training；Pre-Training Data；Web Data Curation；Determining the Data Mix；Annealing Data；Model Architecture

## 一句话总结

Llama 3 报告介绍 Meta 的 Llama 3.1 模型族，覆盖 8B/70B/405B、128K 上下文、多语言、代码、推理、工具使用、安全模型和开放发布策略。

## 深度摄入

- 报告把 Llama 3 描述为一群模型，而不是单个模型：不同尺寸和 instruct 版本共同覆盖端侧、服务端、研究和应用需求。
- 预训练部分详细讨论数据清洗、数据混合、退火、架构、scaling law、并行训练和基础设施。
- 后训练部分连接指令微调、偏好优化、工具使用、多语言和安全能力。
- 开放发布让 Llama 3 成为比较其他闭源/开源模型的重要基准，也让本 wiki 的 LLM 主线获得可复用参照系。

## 需要更新的链接

- [[大语言模型]]
- [[大语言模型论文深度摄入]]
- [[AI学习路线]]

## 使用边界

模型能力和安全评估基于报告发布时间；实际部署还要考虑具体 checkpoint、推理配置和许可边界。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
