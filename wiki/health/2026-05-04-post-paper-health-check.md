---
type: health
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - wiki/index.md
  - wiki/log.md
  - wiki/sources/论文馆藏.md
tags:
  - meta/health
  - meta/wiki
  - collection/papers
---

# 2026-05-04 论文摄入后 Wiki 健康检查

## 范围

在完成 `论文/` 目录级摄入后，对整个 `wiki/` 做结构、索引、双链、frontmatter 和来源目录假设检查。

## 发现

- `wiki/` 当前共有 20 个 Markdown 页面。
- 除 `wiki/index.md`、`wiki/log.md` 和 `_templates/` 模板外，所有正式 wiki 页面都有 YAML frontmatter。
- 共检查到 39 个 Obsidian 双链，没有断链。
- 已建立的正式页面都已经被 `wiki/index.md` 覆盖。
- 顶层 `raw/` 目录不存在；当前结构仍是“顶层来源目录 + wiki 知识层”。
- `TODO`、`TBD`、`待补充`、`待确认` 等占位标记未发现。
- 当前矛盾相关命中来自标准章节标题和索引中的“暂无矛盾记录”，不是未处理冲突。

## 已应用修复

- 新增 [[论文馆藏]]、[[论文]]、[[论文阅读路线]]。
- 更新 [[00-overview]]、[[index]] 和 [[log]]，纳入 `论文/` 的摄入结果。
- 新增本健康检查报告。

## 需要确认后再做的修复

- 是否将 Spring 三份大文档从“论文”语义拆分为“工程参考文档”或 `wiki/works/` 作品页。
- 是否围绕 Dapper、Borg/Omega/K8s、LSM Tree、复制状态机建立第一批系统论文深度来源页。
- 是否在 `README.md` 中继续保留 Obsidian 双链写法，还是改成普通 Markdown 路径链接。

## 新问题或来源缺口

- 下一轮是继续摄入 `AI/`，还是先深度摄入一篇系统论文？
- GPT 相关论文应独立在 `论文/` 下维护，还是与 `AI/` 目录摄入后合并成统一 AI 模型评估知识簇？

