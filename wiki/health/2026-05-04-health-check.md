---
type: health
status: draft
created: 2026-05-04
updated: 2026-05-04
sources:
  - wiki/index.md
  - wiki/log.md
  - wiki/sources/计算机图书馆藏.md
tags:
  - meta/health
  - collection/computer-books
---

# 2026-05-04 健康检查

## 范围

`计算机图书/` 目录级摄入后的初始健康检查。

## 发现

- `计算机图书/` 排除 `.DS_Store` 后包含 202 个可摄入文件。
- 格式分布：193 个 PDF、4 个 PNG、2 个 ZIP、1 个 XMind、1 个 WebP、1 个 EPUB。
- 本地 `pypdf` 成功统计 187 个可读取 PDF，共 74,263 页。
- 6 个 PDF 暂时无法统计页数，因为本地抽取 AES PDF 需要 `cryptography>=3.1`。
- 存在一些重复或近似重复书籍，后续应整理版本：`代码大全`、`重构`、`MySQL技术内幕`、`Linux内核设计与实现`、`算法`、`编程珠玑`、`Effective Java`。
- 当前摄入是目录级，不是逐本全文摄入。单本书的具体观点应等待后续抽取后再作为来源引用。

## 已应用修复

- 新增来源页 [[计算机图书馆藏]]。
- 新增概念页 [[计算机图书]]。
- 新增综合页 [[计算机图书学习路线]]。
- 更新 [[00-overview]]、[[index]] 和 [[log]]。
- 更新 agent schema，使其识别顶层来源目录。

## 需要确认后再做的修复

- 为重复书籍选择推荐版本。
- 决定第一条深度摄入路线：后端工程、系统基础、架构设计、Android、算法或 AI/ML。
- 启用能处理 AES PDF 的抽取路径。
- 如果 ZIP 和 XMind 资料重要，将其展开成派生 Markdown 笔记。

## 新问题或来源缺口

- 用户已经读过哪些书？
- 哪个书架应优先建设成完整双链知识簇？
- 是否应该先为每本书创建空的来源页，还是等实际抽取时再创建？

