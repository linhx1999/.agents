# Agent 技能仓库

这是个人维护的 agent 技能集合。每个技能以 `skills/<skill-name>/SKILL.md` 为入口；贡献约定见 [`AGENTS.md`](AGENTS.md)。`skills/.system/` 存放平台打包的系统技能，不属于下方个人技能索引。

## 技能索引

| 技能 | 用途 |
| --- | --- |
| `anti-defensive-writing` | 减少学术及各类写作中的防御性表达，去除不必要的免责声明、模糊限定和道歉式措辞，同时保留必要的范围与准确性说明。 |
| `commit-work` | 审查和暂存预期改动、拆分逻辑提交并编写规范提交信息。 |
| `csv` | 使用 Bash 工具分析和转换 CSV 数据。 |
| `docx` | 创建、编辑、分析和批注 Word 文档。 |
| `domain-modeling` | 梳理领域术语，维护上下文文档和架构决策。 |
| `excel-automation` | 自动化处理 Excel 工作簿。 |
| `figedit-v2` | 将位图图示重建为高保真可编辑 SVG 和原生 PowerPoint。 |
| `find-skills` | 查找、筛选和安装可用的 agent 技能。 |
| `frontend-design` | 构建或重塑 UI 时提供独特且有意图的视觉设计指导。 |
| `grill-me` | 手动调用 `grilling` 的别名。 |
| `grilling` | 通过分轮追问检验计划、决策或想法。 |
| `handoff` | 把当前对话压缩为可供下一位 agent 接手的交接文档。 |
| `mcp-builder` | 设计和实现连接外部 API 或服务的 MCP 服务端。 |
| `paddleocr-doc-parsing` | 从复杂 PDF 和文档图像中提取版面、表格、公式及阅读顺序。 |
| `pdf` | 提取、生成、拆分、合并和填写 PDF。 |
| `playwright-cli` | 自动化浏览器交互、网页测试和 Playwright 测试。 |
| `ppt-master` | AI 驱动的工作流，用于生成、重建、模板化和增强 PPTX 演示文稿。 |
| `pptx` | 创建、编辑、解析、合并和拆分 PowerPoint 演示文稿。 |
| `research-paper-writing` | 改进 ML/CV/NLP 论文的结构、论证和审稿呈现。 |
| `research-writing` | 起草、润色和检查中英文学术论文、学位论文、开题报告及投稿信，核查论断与证据一致性及 LaTeX/图表规范。 |
| `seaborn` | 创建统计分析和出版级数据可视化。 |
| `skill-creator` | 创建新技能或完善已有技能。 |
| `tdd` | 以红—绿循环进行测试驱动开发和集成测试。 |
| `teach` | 在工作区内以多会话方式教授用户新技能或概念。 |
| `template-skill` | 新技能的最小占位模板。 |
| `ui-ux-pro-max` | Web、移动和桌面的 UI/UX 设计智能与可搜索设计数据。 |
| `writing-for-agents` | 编写和改进技能、`AGENTS.md`、`CLAUDE.md` 等供 agent 使用的文档。 |
| `xlsx` | 创建、修改、分析、可视化和重算电子表格。 |

其中 `grill-me`、`handoff` 和 `teach` 是仅限用户手动调用的入口。

## 目录约定

技能可按需包含以下内容：

```text
skills/<skill-name>/
├── SKILL.md     # 规范入口
├── scripts/     # 辅助脚本
├── references/  # 按条件加载的参考资料
├── assets/      # 模板或静态资源
└── agents/      # agent 集成元数据
```

目录名使用 `kebab-case`。仅限用户手动调用的入口在 `SKILL.md` front matter 中设置 `disable-model-invocation: true`。

## 查找技能

列出所有个人技能入口：

```bash
find skills -maxdepth 2 -name SKILL.md | sort
```

按名称或文件查找：

```bash
rg --files skills | rg '<skill-name>|SKILL\.md'
```
