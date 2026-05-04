---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Paper/DeepSeek_R1.pdf
tags:
  - collection/ai
  - ai/llm
  - ai/reasoning
---

# AI PDF - DeepSeek-R1 强化学习推理模型

## 来源

- 来源路径：`AI/Paper/DeepSeek_R1.pdf`
- 抽取质量：PDF 共 22 页；可抽取文本页 22 页；约 56,882 个抽取字符。
- 目录线索：Introduction；Contributions；Summary of Evaluation Results；Approach；Overview； DeepSeek-R1-Zero: Reinforcement Learning on the Base Model；Reinforcement Learning Algorithm；Reward Modeling

## 一句话总结

DeepSeek-R1 报告展示了通过大规模强化学习激发推理能力的路线：R1-Zero 直接从 base model 训练，R1 则加入冷启动和多阶段训练来改善可读性与稳定性。

## 深度摄入

- R1-Zero 的关键观察是，纯 RL 可以自发出现反思、长链推理和“aha moment”，说明推理行为可由奖励信号诱导。
- R1 在 R1-Zero 基础上加入冷启动数据、多阶段 RL、拒答/安全/格式改善，使推理能力更适合真实使用。
- 报告还强调蒸馏：把大模型推理能力迁移到较小 dense model，是推理模型落地的重要路径。
- 与 ReAct 不同，R1 主要在模型内部推理轨迹上发力；与工具型 agent 结合时，需要额外治理可见思维、验证和工具调用边界。

## 需要更新的链接

- [[大语言模型]]
- [[大语言模型论文深度摄入]]
- [[AI学习路线]]

## 使用边界

推理轨迹、奖励设计和安全行为存在实现细节；应用时不能把长推理等同于正确性，仍需外部验证。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
