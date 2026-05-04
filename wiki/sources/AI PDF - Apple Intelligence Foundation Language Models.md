---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/Apple Intelligence Foundation Language Models.pdf
tags:
  - collection/ai
  - ai/llm
  - ai/model-report
---

# AI PDF - Apple Intelligence Foundation Language Models

## 来源

- 来源路径：`AI/Paper/Apple Intelligence Foundation Language Models.pdf`
- 抽取质量：PDF 共 47 页；可抽取文本页 47 页；约 109,112 个抽取字符。
- 目录线索：Introduction；Architecture；Pre-training；Data；Web pages；Licensed datasets；Code；Math

## 一句话总结

Apple 这份技术报告介绍 AFM-on-device 与 AFM-server：一套面向 Apple Intelligence 的端侧/云侧基础语言模型，重点在架构、训练数据、推理优化、评估和 Responsible AI。

## 深度摄入

- 模型家族服务于系统级个人智能：端侧模型强调低延迟、隐私和设备效率，服务器模型服务更重任务并结合 Private Cloud Compute。
- 报告明确描述训练数据构成、tokenizer、预训练 recipe、后训练、量化和推理优化，体现产品约束下的模型工程路线。
- Responsible AI 被放在模型开发全流程中，包括用户赋能、表示、隐私、安全和误用防护。
- 适合与 Llama、Qwen、DeepSeek 等开源/开放报告对比：Apple 的重点不是最大参数，而是生态集成、端云协同和隐私边界。

## 需要更新的链接

- [[大语言模型]]
- [[大语言模型论文深度摄入]]
- [[AI学习路线]]

## 使用边界

这是厂商技术报告，部分实现细节和训练数据仍是高层描述；不能当作完整复现实验说明。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
