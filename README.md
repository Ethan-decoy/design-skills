# Design Skills · 软件设计技能

[中文](README.md) · [English](README.en.md)

Agent Skills for visual design, interaction design, and data visualization in software.

面向支持 Agent Skills 的工具，用于构建、改进和审查软件界面及数据可视化。三个技能可独立使用，也可以在设计仪表盘或工作台时配合使用。

## 技能

| 技能 | 用途 | 状态 |
| --- | --- | --- |
| [visual-design · 视觉设计](visual-design/SKILL.md) | 从产品气质与真实内容出发，组织构图、视觉层级、排版和色彩。 | 已发布 `v0.1.1` |
| [interaction-design · 交互设计](interaction-design/SKILL.md) | 设计和走查操作路径、控件行为、状态反馈及错误恢复。 | 已发布 `v0.1.1` |
| [data-visualization · 数据可视化](data-visualization/SKILL.md) | 选择和审查图表表达，核对视觉编码与数据含义。 | 已发布 `v0.1.1` |

## 语言

中文是主要维护和验证的版本。每个技能以中文 `SKILL.md` 为入口。英文译文供阅读，分别对应[视觉设计](visual-design/SKILL.en.md)、[交互设计](interaction-design/SKILL.en.md)和[数据可视化](data-visualization/SKILL.en.md)。

## 安装

按需下载 ZIP，或选用对应版本的技能目录。

| 技能 | 安装包 | 版本源码 |
| --- | --- | --- |
| `visual-design` | [下载 ZIP](https://github.com/Ethan-decoy/design-skills/releases/download/v0.1.1/visual-design-v0.1.1.zip) | [v0.1.1](https://github.com/Ethan-decoy/design-skills/tree/v0.1.1/visual-design) |
| `interaction-design` | [下载 ZIP](https://github.com/Ethan-decoy/design-skills/releases/download/v0.1.1/interaction-design-v0.1.1.zip) | [v0.1.1](https://github.com/Ethan-decoy/design-skills/tree/v0.1.1/interaction-design) |
| `data-visualization` | [下载 ZIP](https://github.com/Ethan-decoy/design-skills/releases/download/v0.1.1/data-visualization-v0.1.1.zip) | [v0.1.1](https://github.com/Ethan-decoy/design-skills/tree/v0.1.1/data-visualization) |

解压后，将整个同名目录导入所用工具，或复制到它读取的技能目录，确保 `SKILL.md` 直接位于技能目录中。采用 `.agents/skills/` 约定的工具可使用用户目录下的 `~/.agents/skills/` 或项目下的 `.agents/skills/`。安装和启用方式以所用工具为准。[Agent Skills 客户端指南](https://agentskills.io/client-implementation/adding-skills-support#where-to-scan)

下载校验值见发布页的 `SHA256SUMS.txt`。[v0.1.1 发布页](https://github.com/Ethan-decoy/design-skills/releases/tag/v0.1.1)

## 使用

在所用工具中选择技能，或在请求中写出技能名称。下面每行都是一个独立示例。

```text
请使用 visual-design 改进照片复核页的构图，让照片、编号和复核状态的主次更清楚。
请使用 interaction-design 走查保存失败后的恢复流程，确认用户能怎样继续操作。
请使用 data-visualization 检查这张月度趋势图，结合原表核对刻度、缺测和增幅。
```

### 自动调用

支持自动选择技能的工具可以根据任务和技能描述加载相关技能。综合评审可以用同一条请求交代关联的界面、操作和图表问题。[Agent Skills 的加载方式](https://agentskills.io/home#how-do-agent-skills-work)

```text
从专业审美和 UI/UX 角度审查这个仪表盘，看看信息层级、筛选流程和趋势图哪里最值得改。
```

## 内容

三个技能以 `SKILL.md` 为通用入口。目录也包含英文译文和可选的界面元数据。以视觉设计为例。

```text
visual-design/
├── SKILL.md
├── SKILL.en.md
└── agents/
    └── openai.yaml
```

研究笔记用零件照片复核页说明怎样把产品气质落实到构图、排版和色彩。[视觉设计研究笔记](research/visual-design.md)

## 验证与反馈

发布检查覆盖技能格式、中英文对应、单技能安装包及校验值。中文样例试读检查了技能选择与交付判断，也完成了本地安装和用户级技能发现检查。项目作者实际试用后反馈效果良好。

欢迎反馈使用场景、触发方式和实际结果。[提交反馈](https://github.com/Ethan-decoy/design-skills/issues)
