---
type: health
status: reviewed
created: 2026-05-04
updated: 2026-05-04
sources:
  - wiki/index.md
  - wiki/log.md
  - wiki/sources/计算机图书馆藏.md
  - wiki/sources/经济馆藏.md
tags:
  - meta/health
  - meta/wiki
---

# 2026-05-04 Wiki 整体健康检查

## 范围

在完成 `经济/` 目录级摄入后，对整个 `wiki/` 做结构、索引、双链、frontmatter 和过期结构假设检查。

## 发现

- `wiki/` 当前共有 16 个 Markdown 页面。
- 除 `wiki/index.md`、`wiki/log.md` 和 `_templates/` 模板外，所有正式 wiki 页面都有 YAML frontmatter。
- 共检查到 25 个 Obsidian 双链，没有断链。
- 已建立的正式页面都已经被 `wiki/index.md` 覆盖。
- 顶层 `raw/` 目录不存在；当前结构仍是“顶层来源目录 + wiki 知识层”。
- `raw/` 相关命中均为说明“当前没有 raw 目录”的文字，不是过期路径依赖。
- 英文模板标题已清理；剩余英文主要来自书名、技术名词或 tag。

## 已应用修复

- 新增 [[经济馆藏]]、[[经济]]、[[经济学习路线]]。
- 更新 [[00-overview]]、[[index]] 和 [[log]]，纳入 `经济/` 的摄入结果。
- 新增本整体健康检查报告。
- 更新 `README.md`，让仓库入口反映当前 wiki 状态。

## 需要确认后再做的修复

- 是否要为每本已目录级摄入的书预生成空来源页，还是只在深度摄入时创建。
- 是否要安装或启用能处理 AES PDF 的抽取路径。
- 是否要将 `Agent.md` 与 `AGENT.md` 的大小写差异在 git 层面统一处理。当前文件系统上显示为 `AGENT.md`，git 历史跟踪名为 `Agent.md`。

## 新问题或来源缺口

- 下一轮摄入应选择 `AI/`、`论文/`，还是从 `计算机图书/`/`经济/` 中选一本书做深度摄入？
- `经济/趣味类/` 下的 TXT 文件需要确认是正文材料还是下载说明。

