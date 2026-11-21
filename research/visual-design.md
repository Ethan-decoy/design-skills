# 软件界面的视觉设计与 AI 提示

「沉静、精确」描述的是希望人感受到的品质。照片占多大面积、编号多粗、两组内容隔多远，是设计者可以改变的变量。这些变量通过相互关系产生效果。例如，同样的 16 px 留白，在组内间距为 4 px 时可以提示分组，在各行间隔相同时则形成均匀的节奏。选值要结合真实内容和相邻元素一起看。[IBM 的版式设计方法](https://www.ibm.com/design/language/layout/tips-and-techniques/)

## 视觉设计需要作哪些判断

Moshagen 与 Thielsch 的研究将人对网站视觉美感的评价归纳为简洁性、多样性、色彩和整体制作质量。Seckler 等人的五项网站截图实验比较了对称性、复杂度和色彩等因素。在其样本中，结构因素影响的评价维度比色彩因素更广。对本项目的启发是，当一个界面显得杂乱时，值得同时考察布局、分组与色彩。具体软件适合什么视觉风格，要结合产品和使用者验证。[VisAWI 原始研究](https://www.uni-muenster.de/OWMS/uploads/drafts_thielsch/pdf/moshagen_2010.pdf) · [Seckler 等人的实验](https://edoc.unibas.ch/entities/publication/cb4fcc08-1fa2-422d-abdf-4e79f8bd9ae2)

| 视觉关系 | 可调整的变量 | 构建与审查时可观察什么 |
| --- | --- | --- |
| 构图与层级 | 主体面积、位置、对齐线、明暗对比 | 希望用户先看什么？把方案并排看，哪些元素实际上在争夺注意？ |
| 图底与分组 | 组内距、组间距、留白、边界、背景层次 | 标签、值与操作看起来属于哪一组？长标题换行后，这些关系还清楚吗？ |
| 排印与阅读节奏 | 字体、字号比例、字重、行长、行高、段距 | 用项目里的中文长标题、数字和单位读一遍。标题的表现力、正文的连续性和同屏容量怎样取舍？ |
| 色彩与强调 | 色相、明度、彩度、色块面积、背景与前景的搭配 | 品牌、选择和警示各自怎样表达？两个状态同时出现时各自能否辨认？ |
| 图像与图标 | 主体选择、裁切、图标轮廓与线重、图文比例 | 图片突出了什么？换尺寸后主体是否完整？同级图标与文字放在一起时，轻重是否协调？ |

这些问题可用于讨论整幅画面的统一与变化。Carbon 用相对大小、邻近关系和排印层级组织内容，IBM 的摄影与图标指导分别讨论主体裁切和视觉重量。它们是特定设计系统的实践，项目可以借鉴其中的判断方法。网页用颜色传递状态时，WCAG 2.2 的用色条款还要求提供颜色之外的视觉线索，文字或形状都可参与表达。[布局](https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines) · [排印](https://www.carbondesignsystem.com/building-blocks/foundations/typography/overview) · [摄影](https://www.ibm.com/design/language/photography/tips-and-techniques/) · [图标](https://www.ibm.com/design/language/iconography/ui-icons/design/) · [WCAG 用色条款](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html)

## AI 能从哪些输入获得引导

在 Codex 中，用户说「从审美角度看看这页」时，任务与技能描述的匹配可触发隐式调用。技能被选中后，正文进入当前任务的上下文。模型的权重在训练中学得，激活值是模型处理当前输入时产生的中间计算结果。上下文学习实验展示过在权重固定时，用指令和示例改变任务表现的做法。在这个项目里，可以改变任务信息与参考材料，观察画面中的设计变量怎样变化。要定位模型内部的特定激活，还需要取得内部数据并作专门分析。[Codex 技能说明](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills) · [上下文学习原始研究](https://openai.com/index/language-models-are-few-shot-learners/) · [Anthropic 的内部特征研究](https://www.anthropic.com/research/mapping-mind-language-model)

OpenAI 的 GPT-6.2 前端指南建议说清项目所需的风格、字体和图像，借参考图传达文字难以说清的细节，再渲染并对照修改。Anthropic 也展示过在相同任务中加入排印、主题等提示后，Claude 前端作品出现的变化。这些厂商案例提供了可尝试的方法。它们在本项目使用的模型、中文字体和软件类型上的效果仍待实测。[OpenAI 前端指南](https://developers.openai.com/api/docs/guides/latest-model#gpt-6.2-astra-frontend-design) · [Anthropic 前端设计案例](https://claude.com/resources/articles/improving-frontend-design-through-skills)

## 用零件照片复核页推演一次

假设工程师每天复核一批零件照片。软件已有蓝色选中态，照片需要保留原始色彩和完整边缘，产品希望显得沉静、精确。用户可以只说「从专业视觉设计角度改一下这个复核页」。当项目资料和现有界面已交代这些背景时，可以测试技能在上下文中给模型补充这样一段引导。

> 设计零件照片复核页。让工程师先看到当前照片的细节，再找到对应编号和复核状态。沿用现有蓝色选中态。图像、编号和状态各应占多少空间，由你根据这批实际内容选择。用一条较长的编号和一条同时被选中、等待复核的记录检查方案。

一个可比较的方向是把最大面积留给原图，让记录编号沿共同的起点排列，用相对安静的背景衬托照片，再用文字与形状表达待复核状态。审查时，在实际窗口与窄窗口中看同一条长编号、明暗两张照片和两个同时出现的状态。评语可以具体到哪条对齐线使画面有秩序、哪块背景抢过了照片，以及收小强调色面积后是否仍能辨认选中项。使用者实际先关注什么、是否觉得沉静，需要请使用者看过画面后判断。

要检验提示是否有帮助，可以保留同一需求、内容、模型与工具，仅改变一个引导条件，例如是否向模型解释参考图中需要借鉴的是图文比例。独立生成数次，隐去版本来源后比较方案的气质、照片的可辨程度和评语的具体性。技能是否被选中则用不点名技能的真实请求另作观察。上面的零件案例是实验设想，实际效果有待验证。
