# 技能仓库说明

这个仓库主要用于存储、整理和快速查找个人维护的技能内容，核心目录是 `skills/`。这里不是以功能开发为目标的主项目仓库；`superpowers/` 只是引用进来的上游内容，主要用于参考、对照和测试入口查看。

## 目录导航

- `skills/`：主要技能存储区。
- `AGENTS.md`：贡献与协作约定。
- `superpowers/`：上游引用目录，用于参考结构、文档和测试脚本。

## 技能索引

- `ant-design`：用于 Ant Design、ProComponents 和 Ant Design X 的组件选型与实现决策。
- `brainstorming`：用于在动手前澄清需求、比较方案并形成设计。
- `commit`：用于整理改动、拆分提交并生成规范的 Git 提交信息。
- `docx`：用于创建、编辑、分析和批注 `.docx` 文档。
- `find-skills`：用于查找、筛选和安装可用的 agent skills。
- `golang-pro`：用于 Go 并发、微服务、性能优化和工程化实现。
- `mcp-builder`：用于设计和实现高质量 MCP 服务端。
- `pdf`：用于提取、生成、拆分、合并和填写 PDF。
- `pptx`：用于处理演示文稿的创建、编辑、解析和拆分合并。
- `seaborn`：用于统计图表、探索性分析和出版级可视化。
- `skill-creator`：用于创建新 skill 或完善已有 skill。
- `template-skill`：用于新技能的占位模板和结构起点。
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

## 关于 superpowers/

`superpowers/` 不是本仓库的主要维护对象。只有在以下场景才需要进入该目录：

- 对照上游技能或文档写法
- 查找现成测试入口
- 验证与上游引用内容的对应关系

如果只是日常存放、查找或整理技能，优先停留在 `skills/` 即可。
