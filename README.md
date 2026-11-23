# Design Skills · 软件设计技能

三个面向软件开发的 Codex 技能，用于构建、改进和审查软件界面。它们可以独立使用，也可以在设计仪表盘等任务时配合使用。

| 技能 | 适用任务 |
| --- | --- |
| [视觉设计](visual-design/SKILL.md) | 组织界面的构图、信息层级、排版、色彩和整体风格。 |
| [交互设计](interaction-design/SKILL.md) | 设计和走查操作路径、控件行为、状态反馈与错误恢复。 |
| [数据可视化](data-visualization/SKILL.md) | 设计和审查图表、仪表盘与报表，让数据关系准确且容易读懂。 |

## 安装

在 Codex 中发送这条请求，将三个技能安装到用户级技能目录。也可以只列出需要的技能路径。

```text
使用 $skill-installer，从 GitHub 仓库 Ethan-decoy/design-skills 的 main 分支安装三个技能。路径分别为 visual-design、interaction-design 和 data-visualization。
```

## 试用

安装后，在下一轮对话中提供现有界面或设计需求。Codex 可以根据任务自动选择相关技能。

```text
从专业审美和 UI/UX 角度审查这个仪表盘，看看信息层级、筛选流程和趋势图哪里最值得改。
```

需要明确指定某个技能时，在请求中写出 `$visual-design`、`$interaction-design` 或 `$data-visualization`。

研究笔记用零件照片复核页说明怎样把产品气质落实到构图、排版和色彩。[视觉设计研究笔记](research/visual-design.md)
