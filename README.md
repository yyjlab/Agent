# Agent 规范库

集中维护 AI 协作规则和专项规范，通过入口文件按任务引用。

## 现有规范

| 文件 | 用途 |
| --- | --- |
| [AGENTS.md](AGENTS.md) | 规则入口，说明何时读取专项规范 |
| [documentation.md](documentation.md) | 文档编写规范，涵盖标题、内容、命令、排版和维护 |
| [ui-design.md](ui-design.md) | 界面精简规范，以操作和结果为主，避免冗余说明和提示块 |
| [tool-usage.md](tool-usage.md) | PowerShell 7、FastCtx 的使用分工及上下文节省规则 |
| [linux.md](linux.md) | Linux 执行身份、软件安装目录、Nginx 静态目录和部署验证 |
| [development.md](development.md) | 代码与配置、Code Review、新需求的 GitHub 调研 |
| `devops-lab.local.md` | 本机实验环境和学习方式 |

## 使用方法

- 在目标项目中使用时，将 `AGENTS.md` 与所需专项规范一并放到项目内，保持引用路径有效。
- 目标项目已有 `AGENTS.md` 时，保留原有规则，只补充专项规范的适用场景和读取要求。
- 也可以在目标项目入口中引用本仓库的本地文件，但必须写明实际路径，并确保 AI 能读取；只粘贴仓库链接不能保证自动加载规范。
- 规则只在对应专项文档中维护。新增规范时，同步更新入口和上方列表。
- 本机全局入口先读取这里的 AGENTS.md。全局原件备份和本机实验环境文件留在本地，请按主题维护上表中的规范。
