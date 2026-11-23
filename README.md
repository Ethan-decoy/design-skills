# Design Skills · 软件设计技能

[中文](README.md) · [English](README.en.md)

Codex skills for visual design, interaction design, and data visualization in software.

帮助 Codex 构建、改进和审查软件界面及数据可视化。三个技能可独立使用，也可以在设计仪表盘或工作台时配合使用。

## 技能

| 技能 | 用途 | 状态 |
| --- | --- | --- |
| [visual-design · 视觉设计](visual-design/SKILL.md) | 从产品气质与真实内容出发，组织构图、视觉层级、排版和色彩。 | 已发布 `v0.1.0` |
| [interaction-design · 交互设计](interaction-design/SKILL.md) | 设计和走查操作路径、控件行为、状态反馈及错误恢复。 | 已发布 `v0.1.0` |
| [data-visualization · 数据可视化](data-visualization/SKILL.md) | 选择和审查图表表达，核对视觉编码与数据含义。 | 已发布 `v0.1.0` |

## 语言

中文是主要维护和验证的版本，安装入口为每个技能目录中的 `SKILL.md`，界面说明也使用中文。英文译文供阅读，分别对应[视觉设计](visual-design/SKILL.en.md)、[交互设计](interaction-design/SKILL.en.md)和[数据可视化](data-visualization/SKILL.en.md)。

## 安装

### 在 Codex 中安装

按需向 Codex 发送对应的一行。

```text
$skill-installer 安装 https://github.com/Ethan-decoy/design-skills/tree/v0.1.0/visual-design
$skill-installer 安装 https://github.com/Ethan-decoy/design-skills/tree/v0.1.0/interaction-design
$skill-installer 安装 https://github.com/Ethan-decoy/design-skills/tree/v0.1.0/data-visualization
```

链接固定到 `v0.1.0`。要安装主线源码，可将链接中的 `v0.1.0` 换成 `main`。更新已安装的技能时，在请求中明确说明要替换同名安装。

### 手动安装

从发布页下载所需的 ZIP，解压后将整个技能目录复制到用户目录 `~/.agents/skills/`，或项目中的 `.agents/skills/`。每个压缩包包含中文入口、英文译文和界面元数据，文件校验值见同页的 `SHA256SUMS.txt`。[v0.1.0 发布页](https://github.com/Ethan-decoy/design-skills/releases/tag/v0.1.0) · [Codex 技能目录说明](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## 使用

在请求中点名技能即可明确调用。下面每行都是一个独立示例。

```text
用 $visual-design 改进照片复核页的构图，让照片、编号和复核状态的主次更清楚。
用 $interaction-design 走查保存失败后的恢复流程，确认用户能怎样继续操作。
用 $data-visualization 检查这张月度趋势图，结合原表核对刻度、缺测和增幅。
```

### 自动调用

三个技能都允许自动调用。Codex 可以根据请求与技能描述选择相关技能。综合评审可以用同一条请求交代关联的界面、操作和图表问题。[Codex 的技能调用方式](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills)

```text
从专业审美和 UI/UX 角度审查这个仪表盘，看看信息层级、筛选流程和趋势图哪里最值得改。
```

## 内容

三个技能使用相同的目录结构。以视觉设计为例。

```text
visual-design/
├── SKILL.md
├── SKILL.en.md
└── agents/
    └── openai.yaml
```

研究笔记用零件照片复核页说明怎样把产品气质落实到构图、排版和色彩。[视觉设计研究笔记](research/visual-design.md)

## 验证与反馈

`v0.1.0` 是首个版本。发布检查覆盖技能格式、中英文对应、单技能安装包及校验值。中文样例试读检查了技能选择与交付判断，本机 Codex 检查确认了全局技能发现。项目作者实际试用后反馈效果良好。

欢迎反馈使用场景、触发方式和实际结果。[提交反馈](https://github.com/Ethan-decoy/design-skills/issues)
