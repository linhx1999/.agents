# 投稿信与投稿前检查

用于准备投稿信（Cover Letter）、投稿前全文自查与录用后终稿（Camera-ready）核查。以用户给出的目标期刊/会议、当前投稿轮次和实际稿件材料为准；不包含审稿意见回复（Rebuttal）或代替用户操作投稿系统。

## 先取得本次适用要求

从已有材料读取目标期刊/会议（Venue）、文章类型、稿件标题、通讯作者、当前版本状态及作者指南。需要核实篇幅上限、双盲匿名规则、必交声明或附件要求时，以本次会议/期刊的当前官方说明为准；无访问条件时明确列为待核实项，不套用历史年份的过时规定。

只有影响本次交付的关键信息缺失时才向用户询问。可先完成有依据的正文检查或信件草稿，再将缺失事项集中列出。

## Cover Letter（投稿信）

用精炼段落涵盖以下核心要素，具体篇幅与必备声明服从目标期刊规定：

1. **提交目的**：写明准确的稿件标题、文章类型（如 Original Research Article / Regular Paper）与目标期刊名称。
2. **核心工作与适配度**：简述研究问题、核心方法机制与已有证据支持的主要发现；具体说明工作为何契合该期刊的读者群与收录范围（Scope），避免整段照抄论文摘要。
3. **必要合规声明**：仅写入作者已明确提供或确认的事实声明（如原创性、未一稿多投、全体作者知情同意、关联已发表/在审稿件说明、利益冲突或资助信息）。
4. **通讯作者信息**：写明已确认的通讯作者姓名、所属单位与联系邮箱，礼貌简短收尾。

**硬底线**：格式模板不能充当事实依据。在作者未明确确认前，严禁自动写入“所有作者均已阅读并同意投稿”“不存在任何利益冲突”“未同时投递其他刊物”“无外部资金支持”等法律或伦理声明，须将此类声明保留为醒目占位符或信外待确认清单。

推荐或回避审稿人仅在用户主动提出且目标期刊要求时处理，理由须基于具体的学术领域匹配度或已确认的利益关系；不得仅凭“同行竞争”或“私人熟识”自动生成推荐/回避理由。

### 英文起草骨架

以下为含占位符的草稿骨架；须由作者用已确认事实替换占位符后再作为正式提交版本：

```text
Dear [Editor Name or Editorial Team],

Please consider our manuscript, “[Manuscript Title],” for publication as a [Article Type] in [Journal Name].

The manuscript addresses [specific research problem and context]. To overcome [key technical bottleneck], we propose [core method or mechanism supported by the manuscript]. Experiments on [evaluated benchmarks/settings] show that [principal supported finding and its scope]. This work is relevant to the readership of [Journal Name] because [specific fit with journal scope].

[Include ONLY the declarations required by the journal and explicitly confirmed by the authors, e.g., originality, concurrent submission status, related manuscripts, conflicts of interest, and funding.]

Please address all correspondence concerning this manuscript to [Corresponding Author Name, Affiliation, Email].

Sincerely,
[Corresponding Author Name]
[Affiliation]
```

中文投稿信对应结构：投稿目的与稿件题名 → 研究问题、核心方法与已证实结果 → 与本刊领域的契合点 → 作者已确认的合规声明 → 通讯作者联系方式。信中提炼的“研究亮点”必须能严格追溯至稿件正文，不额外夸大实验范围、排名或独创性。

## 投稿前按证据检查

只报告在当前材料范围内实际核查过的内容。每个检查项明确标注状态：**`已核对` / `发现问题` / `待作者确认` / `未检查` / `不适用`**，并附具体章节、图表或行号位置，绝不把未执行的工具检查当作“已通过”。

| 检查维度 | 核对要点 |
|---|---|
| 研究主线与贡献 | 问题定义、挑战、方法设计与贡献列表一一对应；实验结果足以支撑结论强度；未把未来计划或机理推测写成既成发现 |
| 实验与图表一致性 | 摘要、正文、表格、图注和附录中的数值、指标名称、升降方向（$\uparrow/\downarrow$）、数据集划分与实验条件完全一致；最优/次优高亮标记与真实数值相符；主实验与消融实验各司其职 |
| 文字与结构自洽 | 摘要独立可读；方法含整体概览与符号定义；段落与句子逻辑连贯；术语、缩写首次定义、语法和时态合理 |
| 引用与学术归属 | 引文真实存在且确实支持所附论断，`\cite` 键与参考文献条目对应；借用或改编图表已注明来源；文献著录格式统一遵循目标模板；前人工作与本文增量界限清晰 |
| 双盲匿名与自引 | 若本轮要求双盲匿名：核查署名、单位、致谢、基金号、页眉页脚及 PDF 元数据是否隐去；检查自引是否采用第三人称（如 `Prior work [1]` 而非 `Our previous work [1]`）；开源链接是否已做匿名化处理。切勿未经确认擅自切换匿名/实名状态 |
| 必交专门声明 | 核对目标会议/期刊要求的专门段落（如 `Limitations`、`Broader Impact / Ethics Statement`、`Reproducibility / Data & Code Availability`）是否齐全、位置合规，且代码/数据开源承诺与实际准备状态一致 |
| 版式与文件合规 | 使用本次适用模板；正文、参考文献与附录页数符合当前规定；分辨率、字体嵌入、超链接与补充材料（Supplementary Material）符合要求 |
| 作者与伦理元数据 | 实名轮次下，作者顺序、单位编号、共同一作/通讯作者标记、资助项目、致谢和利益冲突均严格依据作者提供的事实核对 |

指出技术或证据缺口时，须具体说明**“哪项论断缺少哪组对照/哪项消融/哪个数据来源”**，避免笼统评价“实验不够充分”。文本审查不自动触发运行新实验。

### 检查报告输出结构

交付投稿前自查或终稿核查结果时，按以下结构清晰呈现：

1. **阻断项与证据硬伤**：直接影响投稿合规性或科学真实性的问题（如表文数值矛盾、过度承诺无实验支撑、双盲违规泄露身份、必交声明缺失）。
2. **逻辑与一致性缺口**：需补充说明或微调范围的问题（如某模块缺少消融呼应、符号/术语跨节不一致、待核实引用）。
3. **表达与排版建议**：可进一步提升可读性的语言润色、图注自洽性或参考文献格式细节。
4. **待作者确认与未检查项**：需作者补填的真实声明信息，以及因缺少编译环境或外部文件而明确标为`未检查`的项目。

## Camera-ready（录用终稿）与交付

稿件录用后，按本次最终版（Camera-ready）指南逐项复核：标题大小写规范、全体作者姓名拼写与单位映射、共同一作/通讯作者符号标记、基金资助号与致谢、图表清晰度与版权来源、参考文献完整性、补充材料以及代码/数据可用性声明。作者排序与贡献分配不由本技能推断；涉及作者权益与声明的信息一律以本稿已确认事实为准，不增设额外的通用审批流程。

具备编译与检查工具时，实际运行编译并核查未解析交叉引用、PDF 字体嵌入（如 Type 1 / TrueType 要求）与页面边界，如实报告执行输出；未运行相关工具时直接标为`未检查`。最终文件是否通过官方出版系统校验，以投稿系统或其指定检查工具（如 IEEE PDF eXpress 等）的实际结果为准。
