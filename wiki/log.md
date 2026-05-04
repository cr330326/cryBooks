# Wiki 日志

这里按时间追加记录摄入、查询、健康检查和结构维护。标题保持统一格式，便于用 `rg "^## \\[" wiki/log.md` 检索。

## [2026-05-04] 初始化 | 个人 LLM Wiki 骨架

- 初始化 LLM Wiki 目录结构。
- 新增 `CLAUDE.md` 和 `AGENT.md` schema 文件。
- 新增初始索引、总览、页面模板和健康检查模板。

## [2026-05-04] 摄入 | 计算机图书馆藏

- 对 `计算机图书/` 完成目录级摄入。
- 新增 `wiki/sources/计算机图书馆藏.md`。
- 新增 `wiki/concepts/计算机图书.md`。
- 新增 `wiki/syntheses/计算机图书学习路线.md`。
- 更新 schema，使其识别顶层来源目录。

## [2026-05-04] 健康检查 | 计算机图书目录级摄入

- 确认 `计算机图书/` 排除 `.DS_Store` 后包含 202 个可摄入文件。
- 使用本地 `pypdf` 统计到 187 个可读取 PDF，共 74,263 页。
- 新增 `wiki/health/2026-05-04-health-check.md`。

## [2026-05-04] 健康检查 | 仓库结构与中文化

- 确认当前仓库没有 `raw/` 目录，来源资料位于顶层分类目录。
- 将 `CLAUDE.md` 和 `AGENT.md` 改为中文 schema。
- 将主要 wiki 页面、模板和健康检查内容改为中文。
- 新增 `wiki/health/2026-05-04-structure-check.md`。

## [2026-05-04] 摄入 | 经济馆藏

- 对 `经济/` 完成目录级摄入。
- 确认 `经济/` 排除 `.DS_Store` 后包含 39 个可摄入文件。
- 使用本地 `pypdf` 统计到 32 个可读取 PDF，共 11,046 页。
- 新增 `wiki/sources/经济馆藏.md`。
- 新增 `wiki/concepts/经济.md`。
- 新增 `wiki/syntheses/经济学习路线.md`。

## [2026-05-04] 健康检查 | Wiki 整体检查

- 检查 `wiki/` 中 16 个 Markdown 页面。
- 确认正式 wiki 页面 frontmatter 完整。
- 检查到 25 个 Obsidian 双链，无断链。
- 确认已建立页面都被 `wiki/index.md` 覆盖。
- 新增 `wiki/health/2026-05-04-wiki-health-check.md`。

## [2026-05-04] 摄入 | 论文馆藏

- 对 `论文/` 完成目录级摄入。
- 确认 `论文/` 排除 `.DS_Store` 后包含 10 个 PDF。
- 使用本地 `pypdf` 统计到 10 个可读取 PDF，共 1,562 页。
- 新增 `wiki/sources/论文馆藏.md`。
- 新增 `wiki/concepts/论文.md`。
- 新增 `wiki/syntheses/论文阅读路线.md`。

## [2026-05-04] 健康检查 | 论文摄入后 Wiki 整体检查

- 检查 `wiki/` 中 20 个 Markdown 页面。
- 确认正式 wiki 页面 frontmatter 完整。
- 检查到 39 个 Obsidian 双链，无断链。
- 确认已建立页面都被 `wiki/index.md` 覆盖。
- 新增 `wiki/health/2026-05-04-post-paper-health-check.md`。
