---
type: health
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - CLAUDE.md
  - AGENT.md
  - wiki/index.md
  - wiki/00-overview.md
tags:
  - meta/health
  - meta/structure
---

# 2026-05-04 仓库结构检查

## 范围

检查 `raw/` 删除后的实际仓库结构，并将 agent 文档与 wiki 页面统一为中文说明。

## 当前结构结论

当前仓库结构是正确的“顶层来源目录 + wiki 知识层”：

- 顶层来源目录：`计算机图书/`、`AI/`、`论文/`、`经济/`、`数学/`、`文章合集/`、`名人/`、`其它/`、`图片/`、`效能/`。
- 知识层目录：`wiki/`。
- Agent 入口：`AGENT.md`。
- 维护规范：`CLAUDE.md`。
- 方法原文：`llm-wiki.md`。

## 已应用修复

- 将 `CLAUDE.md` 改为中文，并明确当前没有 `raw/` 目录。
- 将 `AGENT.md` 改为中文，并要求 agent 不再假设来源资料位于 `raw/`。
- 将 `wiki/index.md`、`wiki/00-overview.md`、[[计算机图书]]、[[计算机图书学习路线]]、[[计算机图书馆藏]] 和本健康检查相关页面中文化。
- 在 [[index]] 中补充本结构检查记录。

## 后续建议

- 若后续新增临时收件箱，建议直接建立 `收件箱/` 或 `inbox/`，不要重新引入 `raw/`，以免和当前结构混淆。
- 下一次摄入时，直接从用户指定的顶层来源目录开始。

