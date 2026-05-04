---
type: source
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - AI/Harness/book2-comparing.pdf
tags:
  - collection/ai
  - ai/agent-runtime
  - ai/harness
---

# AI PDF - Claude Code 与 Codex Harness 设计哲学比较

## 来源

- 来源路径：`AI/Harness/book2-comparing.pdf`
- 抽取质量：PDF 共 52 页；可抽取文本页 52 页；约 32,833 个抽取字符。
- 目录线索：导读；阅读地图；先看第一本书：Claude Code 给出的九个结构判断；再看这本比较书：同一个问题，Claude Code 和 Codex 从哪里起笔；合起来以后，真正清楚的是什么；推荐阅读顺序；一句话总结；序言 两套 Harness

## 一句话总结

这本比较笔记把 Claude Code 与 Codex 放在同一个 harness 问题下观察：两者都在约束模型行动，但一个偏运行时纪律，一个偏显式控制面和本地规则资产。

## 深度摄入

- Claude Code 被描述为运行时优先：秩序更多落在 query loop、工具编排、中断、compact 与恢复机制里。
- Codex 被描述为制度层优先：秩序更多落在 instruction fragment、tool schema、approval policy、thread/state 与本地规则里。
- 真正的分野不是界面或文风，而是工具动手前谁拥有最后解释权、失败后谁负责恢复、团队规则如何持续进入系统。
- 对本仓库的启发是：`CLAUDE.md`、`Agent.md`、目录 schema、健康报告和日志要共同构成可审计控制面。

## 需要更新的链接

- [[AI Agent Runtime]]
- [[Agent Harness与OpenClaw深度摄入]]

## 使用边界

这是比较工程笔记，不是官方产品规范；用于抽象设计原则时很有价值，但不能替代官方行为文档。

## 待解决问题

- 是否需要继续拆成章节级笔记或实验/案例级笔记？
- 本页中的综合判断是否需要与其它 AI 来源做对照页？
