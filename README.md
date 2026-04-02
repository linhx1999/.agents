# 技能仓库说明

这个仓库主要用于存储、整理和快速查找个人维护的技能内容，核心目录是 `skills/`。这里不是以功能开发为目标的主项目仓库；`superpowers/` 只是引用进来的上游内容，主要用于参考、对照和测试入口查看。

## 目录导航

- `skills/`：主要技能存储区。
- `skills/.system/`：系统级技能。
- `AGENTS.md`：贡献与协作约定。
- `superpowers/`：上游引用目录，用于参考结构、文档和测试脚本。

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
