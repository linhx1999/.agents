# 技能仓库说明

这个仓库主要用于存储、整理和快速查找个人维护的技能内容，核心目录是 `skills/`。这里不是以功能开发为目标的主项目仓库。

## 目录导航

- `skills/`：主要技能存储区。
- `AGENTS.md`：贡献与协作约定。

## 技能索引

- `ant-design`：用于 Ant Design、ProComponents 和 Ant Design X 的组件选型与实现决策。
- `codebase-design`：用于以深模块、接口、接缝和适配器等统一词汇设计代码结构。
- `commit-work`：用于审查改动、拆分提交并生成规范的 Git 提交信息。
- `csv`：用于通过 Bash 工具分析和转换 CSV 数据。
- `docx`：用于创建、编辑、分析和批注 `.docx` 文档。
- `domain-modeling`：用于梳理领域术语、维护上下文文档并记录架构决策。
- `excel-automation`：用于自动化处理 Excel 工作簿。
- `figedit`：用于将位图图示重建为可编辑 SVG 和 PowerPoint。
- `find-skills`：用于查找、筛选和安装可用的 agent skills。
- `frontend-design`：用于设计和改进具有明确视觉风格的前端界面。
- `golang-pro`：用于 Go 并发、微服务、性能优化和工程化实现。
- `grill-with-docs`：用于在分轮追问计划或设计的同时维护领域文档和架构决策。
- `grilling`：用于通过分轮追问检验计划、决策或想法。
- `handoff`：用于把当前对话压缩为可供下一位 agent 接手的交接文档。
- `improve-codebase-architecture`：用于扫描代码库的深模块改进机会并生成可视化报告。
- `mcp-builder`：用于设计和实现高质量 MCP 服务端。
- `paddleocr-doc-parsing`：用于解析复杂 PDF 和文档图像的结构、表格及公式。
- `pdf`：用于提取、生成、拆分、合并和填写 PDF。
- `pptx`：用于处理演示文稿的创建、编辑、解析和拆分合并。
- `research`：用于基于高可信一手资料开展研究并把结果写入仓库。
- `research-paper-writing`：用于提升 ML/CV/NLP 类论文的写作质量、结构与审稿友好度。
- `resolving-merge-conflicts`：用于追溯改动意图并解决进行中的合并或变基冲突。
- `seaborn`：用于统计图表、探索性分析和出版级可视化。
- `setup-matt-pocock-skills`：用于初始化工程技能所需的问题追踪、标签和领域文档配置。
- `skill-creator`：用于创建新 skill 或完善已有 skill。
- `template-skill`：用于新技能的占位模板和结构起点。
- `triage`：用于按状态机分类、核验和整理 issue 及外部 PR。
- `ui-ux-pro-max`：用于检索 UI/UX 风格、配色、字体、交互与技术栈指南。
- `use-x-chat`：用于讲解和实现 Ant Design X 的 `useXChat` 用法。
- `vercel-react-best-practices`：用于 React 和 Next.js 的性能优化与最佳实践对照。
- `writing-for-agents`：用于编写和改进 skill、`AGENTS.md`、`CLAUDE.md` 等 agent 消费的文档。
- `x-chat-provider`：用于将自定义流式接口适配为 Ant Design X Chat Provider。
- `x-request`：用于配置和使用 Ant Design X 的 `XRequest`。
- `xlsx`：用于创建、修改、分析和重算电子表格文件。

## skills/ 组织方式

每个技能通常放在 `skills/<skill-name>/` 下，入口文件为 `SKILL.md`。常见附属目录如下：

- `scripts/`：辅助脚本。
- `references/`：参考资料。
- `assets/`：模板或静态资源。

命名建议保持 `kebab-case`，例如 `skills/use-x-chat/`、`skills/x-request/`。

## 日常查找入口

查看所有技能入口：

```bash
find skills -maxdepth 2 -name SKILL.md | sort
```

按名称查找某个技能：

```bash
rg --files skills | rg 'SKILL\.md|use-x-chat|x-request'
```

快速浏览仓库前两层目录：

```bash
find . -maxdepth 2 -type d | sort
```
