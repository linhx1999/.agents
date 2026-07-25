# 技能仓库说明

这个仓库主要用于存储、整理和快速查找个人维护的技能内容，核心目录是 `skills/`。这里不是以功能开发为目标的主项目仓库。

## 目录导航

- `skills/`：主要技能存储区。
- `AGENTS.md`：贡献与协作约定。

## 技能索引

- `ant-design`：用于 Ant Design、ProComponents 和 Ant Design X 的组件选型与实现决策。
- `commit-work`：用于审查改动、拆分提交并生成规范的 Git 提交信息。
- `csv`：用于通过 Bash 工具分析和转换 CSV 数据。
- `docx`：用于创建、编辑、分析和批注 `.docx` 文档。
- `excel-automation`：用于自动化处理 Excel 工作簿。
- `figedit`：用于将位图图示重建为可编辑 SVG 和 PowerPoint。
- `find-skills`：用于查找、筛选和安装可用的 agent skills。
- `frontend-design`：用于设计和改进具有明确视觉风格的前端界面。
- `grilling`：用于通过逐项追问检验计划、决策或想法。
- `golang-pro`：用于 Go 并发、微服务、性能优化和工程化实现。
- `mcp-builder`：用于设计和实现高质量 MCP 服务端。
- `paddleocr-doc-parsing`：用于解析复杂 PDF 和文档图像的结构、表格及公式。
- `pdf`：用于提取、生成、拆分、合并和填写 PDF。
- `pptx`：用于处理演示文稿的创建、编辑、解析和拆分合并。
- `seaborn`：用于统计图表、探索性分析和出版级可视化。
- `skill-creator`：用于创建新 skill 或完善已有 skill。
- `template-skill`：用于新技能的占位模板和结构起点。
- `ui-ux-pro-max`：用于检索 UI/UX 风格、配色、字体、交互与技术栈指南。
- `use-x-chat`：用于讲解和实现 Ant Design X 的 `useXChat` 用法。
- `vercel-react-best-practices`：用于 React 和 Next.js 的性能优化与最佳实践对照。
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
