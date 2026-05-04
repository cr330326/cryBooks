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

## [2026-05-04] 摄入 | 名人、数学、文章合集、图片、效能馆藏

- 对 `名人/`、`数学/`、`文章合集/`、`图片/`、`效能/` 完成目录级摄入。
- `名人/`：8 个 EPUB，当前集中在李笑来作品集。
- `数学/`：4 个 PDF，共 1,357 页。
- `文章合集/`：9 个 PDF，共 7,001 页。
- `图片/`：4 个 WebP 图片。
- `效能/`：1 个 PDF，共 145 页。
- 新增对应馆藏页和概念页。

## [2026-05-04] 健康检查 | 多目录摄入后 Wiki 整体检查

- 检查 `wiki/` 中 31 个 Markdown 页面。
- 确认正式 wiki 页面 frontmatter 完整。
- 检查到 77 个 Obsidian 双链，无断链。
- 确认已建立页面都被 `wiki/index.md` 覆盖。
- 新增 `wiki/health/2026-05-04-multi-directory-health-check.md`。

## [2026-05-04] 摄入 | AI馆藏与核心材料深度摄入

- 对 `AI/` 完成目录级摄入。
- 确认 `AI/` 排除 `.DS_Store` 后包含 36 个可摄入文件：25 个 PDF、9 个 PPTX、2 个 Markdown。
- 使用本地 `pypdf` 统计到 25 个可读取 PDF，共 3,067 页。
- 本地解析 9 个 PPTX，共 674 张幻灯片。
- 新增 `wiki/sources/AI馆藏.md`。
- 新增 `wiki/concepts/AI.md`、`wiki/concepts/AI Agent Runtime.md`、`wiki/concepts/大语言模型.md`。
- 新增 `wiki/syntheses/Agent Harness与OpenClaw深度摄入.md`、`wiki/syntheses/大语言模型论文深度摄入.md`、`wiki/syntheses/AI学习路线.md`。

## [2026-05-04] 健康检查 | AI 深度摄入后 Wiki 整体检查

- 检查 `wiki/` 中 39 个 Markdown 页面。
- 确认正式 wiki 页面 frontmatter 完整。
- 检查到 116 个 Obsidian 双链，无断链。
- 确认已建立页面都被 `wiki/index.md` 覆盖。
- 新增 `wiki/health/2026-05-04-ai-deep-ingest-health-check.md`。

## [2026-05-04] 摄入 | 其它目录深度摄入

- 对 `其它/` 完成目录级和主题级深度摄入。
- 确认 `其它/` 排除 `.DS_Store` 后包含 15 个可摄入文件：12 个 PDF、3 个 EPUB。
- 使用本地 `pypdf` 统计到 11 个可读取 PDF，共 2,715 页；1 个 PDF 读取失败。
- 新增 `wiki/sources/其它馆藏.md`、`wiki/concepts/其它.md`。
- 新增 `wiki/syntheses/历史商业与货币史.md`、`wiki/syntheses/风水与民俗材料.md`、`wiki/syntheses/生存与灾难叙事材料.md`。

## [2026-05-04] 健康检查 | 其它目录深度摄入后 Wiki 整体检查

- 检查 `wiki/` 中 45 个 Markdown 页面。
- 确认正式 wiki 页面 frontmatter 完整。
- 检查到 143 个 Obsidian 双链，无断链。
- 确认已建立页面都被 `wiki/index.md` 覆盖。
- 新增 `wiki/health/2026-05-04-misc-deep-ingest-health-check.md`。

## [2026-05-04] 结构更新 | raw 新增文件收件箱

- 确认 `raw/` 目录存在，并加入 `.gitkeep` 空占位符。
- 将 `raw/` 定义为后续新增、未分类、待摄入文件的收件箱。
- 更新 `CLAUDE.md`、`Agent.md`、`README.md` 和 `wiki/00-overview.md` 中的当前结构说明。
- 新增 `wiki/health/2026-05-04-raw-inbox-structure-update.md`。

## [2026-05-04] 健康检查 | 全局覆盖诊断

- 新增 `raw/.gitkeep` 空占位符，确保 `raw/` 能被版本控制保留。
- 检查 10 个顶层资料目录，共 328 个可摄入文件；均已有目录级馆藏页。
- 确认 `raw/` 除 `.gitkeep` 外没有待摄入文件。
- 识别当前主要缺口：大量材料仍停留在目录级或主题级综合，尚未形成单书、单篇论文、单份报告或课程章节深度页。
- 新增 `wiki/health/2026-05-04-global-coverage-diagnostic.md`。

## [2026-05-04] 摄入 | AI 目录 25 个 PDF 深度来源页

- 对 `AI/` 下 25 个 PDF 完成单文件深度摄入。
- 新增 25 个 `wiki/sources/AI PDF - ...` 来源页。
- 新增 `wiki/syntheses/AI PDF深度摄入总览.md`。
- 更新 `wiki/sources/AI馆藏.md`、`wiki/concepts/AI.md`、`wiki/syntheses/AI学习路线.md` 和 `wiki/index.md`。
- 新增 `wiki/health/2026-05-04-ai-pdf-deep-ingest-health-check.md`。
