---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Harness/book1-claude-code.pdf
tags:
  - collection/ai
  - ai/agent-runtime
  - ai/harness
---

# AI PDF - Claude Code Harness Engineering 设计指南

## 来源

- 来源路径：`AI/Harness/book1-claude-code.pdf`
- 抽取质量：PDF 共 87 页；可抽取文本页 87 页；约 61,406 个抽取字符。
- 目录线索：导读；序言 Harness；第 1 章 为什么需要 Harness Engineering；1.1 问题在于让模型别乱来；1.2 Claude Code 的第一层 Harness：受约束的会话系统；1.3 第二层 Harness：代理依赖持续循环；1.4 第三层 Harness：工具调用必须服从调度；1.5 第四层 Harness：最危险的工具，必须配最细的规矩

## 一句话总结

这本书把 Claude Code 看成一套受约束的 agent harness，而不是单纯的聊天 prompt；核心关心控制面、循环、工具调度、权限、恢复、上下文治理和验证。

## 深度摄入

- 把 prompt 降级为控制平面的一部分：真正决定系统可靠性的，是规则优先级、工具协议、状态治理和恢复路径。
- 强调 agent 的主路径必须包含失败处理：权限拒绝、工具错误、上下文逼近、compact 失败和中断都应被设计进循环。
- Claude Code 的价值不只是模型能力，而是运行时约束：受限会话、持续循环、工具调度、危险工具细规和团队 CLAUDE.md 共同组成治理层。
- 对本仓库的启发是：wiki 摄入也要有明确 schema、日志、健康检查和可恢复的下一步，而不能只依赖一次性总结。

## 需要更新的链接

- [[AI Agent Runtime]]
- [[Agent Harness与OpenClaw深度摄入]]
- [[AI学习路线]]

## 使用边界

偏工程设计解读，适合作为 agent harness 方法论来源；具体源码细节需要回到原文和对应项目核验。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
