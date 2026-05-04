---
type: health
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/
  - wiki/sources/AI馆藏.md
  - wiki/syntheses/AI PDF深度摄入总览.md
  - wiki/health/2026-05-04-global-coverage-diagnostic.md
tags:
  - collection/ai
  - health/coverage
  - ingest/deep
---

# AI PDF 深度摄入后健康检查

## 范围

本次检查针对 `AI/` 目录下全部 PDF 文件。目标是把全局诊断中指出的“许多材料仍停留在目录级、馆藏级或主题级综合”进一步推进到单 PDF 深度来源页。

## 处理结果

- `AI/` 下共 25 个 PDF，已全部建立单文件深度来源页。
- 25 个 PDF 共 3,067 页；本地可抽取文本页 3,061 页。
- 大多数 PDF 文本可完整抽取；主要例外是 `AI/报告/2026 年 AI 与数据发展预测.pdf`，32 页中仅 2 页可抽取文本，已在对应来源页标注限制。
- 新增 [[AI PDF深度摄入总览]] 作为 25 个 PDF 来源页的总入口。
- 更新 [[AI馆藏]]、[[AI]]、[[AI学习路线]]、[[index]] 和 [[2026-05-04-global-coverage-diagnostic]]。

## 新增来源页范围

- Agent Runtime 与工具系统：Harness、OpenClaw、ReAct、Generative Agents、Claude Skills、Hello Agents。
- LLM 基础与模型报告：Transformer、GPT-4、Llama 3、Qwen、DeepSeek、Apple AFM、OpenAI 竞赛推理模型。
- RAG 与知识系统：GraphRAG。
- 趋势、组织与应用报告：Agentic Coding、AI 与数据预测、中国企业 AI 人才组织、得到 AI 年度报告。

## 当前仍待处理

- `AI/` 下 9 个 PPTX 尚未拆成课程章节页。
- `AI/` 下 2 个 Markdown 尚未建立单文件深度来源页。
- 本轮来源页是单 PDF 深度摄入，不是逐页摘录；长书如 [[AI PDF - Hello Agents 从零构建智能体系统]]、[[AI PDF - 大语言模型从理论到实践 第二版]] 后续仍可按章节继续拆分。

## 风险与边界

- 趋势报告具有时效性和预测性质；查询时应标注报告时间背景。
- 厂商技术报告通常不会公开完整训练配方；不能把它们当作可复现实验说明。
- 抽取质量受限的 PDF 需要 OCR 或人工复核后再做更细综合。
