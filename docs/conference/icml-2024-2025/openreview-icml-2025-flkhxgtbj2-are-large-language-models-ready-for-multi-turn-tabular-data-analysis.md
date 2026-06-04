---
title: Are Large Language Models Ready for Multi-Turn Tabular Data Analysis?
title_zh: 大型语言模型能否胜任多轮表格数据分析？
authors: "Jinyang Li, Nan Huo, Yan Gao, Jiayi Shi, Yingxiu Zhao, Ge Qu, Bowen Qin, Yurong Wu, Xiaodong Li, Chenhao Ma, Jian-Guang Lou, Reynold Cheng"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=flKhxGTBj2"
tags: ["query:ai-finance"]
score: 7.0
evidence: 评估LLM在交互式表格数据分析中表现，涵盖财务报告
tldr: 针对对话式表格数据分析任务缺乏评测基准的问题，提出CoTA基准，含1013个对话覆盖四个场景（包括财务报告分析）。利用多智能体环境低人力构造成本高效。实验发现LLMs在处理组合条件时仍有限，为未来改进提供方向。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1737, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1589, \"height\": 727, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 865, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 839, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 814, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 687, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1580, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 799, \"height\": 802, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1176, \"height\": 698, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1412, \"height\": 1049, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1760, \"height\": 1303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 779, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 813, \"height\": 542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 109, \"height\": 110, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 108, \"height\": 110, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 99, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1501, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-flkhxgtbj2/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 64, \"height\": 73, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 693, \"height\": 645, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1773, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1769, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1555, \"height\": 680, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1483, \"height\": 774, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1771, \"height\": 390, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1480, \"height\": 154, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1505, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1280, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1251, \"height\": 159, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-flkhxgtbj2/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1262, \"height\": 160, \"label\": \"Table\"}]"
motivation: 缺乏对话式表格数据分析的全面评估基准。
method: 构建多智能体环境自动生成带标注的对话数据，创建CoTA基准。
result: 覆盖四种实用场景，揭示LLMs在处理组合条件时的不足。
conclusion: 为LLMs在表格分析（含金融报告）提供有效评测工具。
---

## Abstract
Conversational Tabular Data Analysis, a collaboration between humans and machines, enables real-time data exploration for informed decision-making. The challenges and costs of collecting realistic conversational logs for tabular data analysis hinder comprehensive quantitative evaluation of Large Language Models (LLMs) in this task. To mitigate this issue, we introduce **CoTA**, a new benchmark to evaluate LLMs on conversational tabular data analysis. **CoTA** contains 1013 conversations, covering 4 practical scenarios: Normal, Action, Private, and Private Action. Notably, **CoTA** is constructed by an economical multi-agent environment, Decision Company, with few human efforts. This environment ensures efficiency and scalability of generating new conversational data. Our comprehensive study, conducted by data analysis experts, demonstrates that Decision Company is capable of producing diverse and high-quality data, laying the groundwork for efficient data annotation. We evaluate popular and advanced LLMs in **CoTA**, which highlights the challenges of conversational tabular data analysis. Furthermore, we propose Adaptive Conversation Reflection (ACR), a self-generated reflection strategy that guides LLMs to learn from successful histories. Experiments demonstrate that ACR can evolve LLMs into effective conversational data analysis agents, achieving a relative performance improvement of up to 35.14%.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究动机**：对话式表格数据分析（Conversational Tabular Data Analysis）是人类与机器协作进行实时数据探索的重要方式，但在多轮交互中，用户意图往往不明确，需要模型进行澄清、假设或修改代码。现有基准大多关注单轮或固定格式的文本到SQL/代码生成，缺乏对多轮对话、用户反馈、私有库等复杂场景的综合评估。
- **核心问题**：当前大型语言模型（LLMs）是否具备处理多轮交互式表格数据分析的能力？如何系统评估并提升其在真实分析场景中的表现？
- **背景**：收集真实的人机对话日志存在隐私、成本高昂、难以规模化等问题。因此需要构建一个高效、可扩展、高质量的基准数据集。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：通过多智能体沙盒（**Decision Company**）自动生成对话数据，再辅以人工校准，以低成本构建高质量基准。在此基础上提出**自适应对话反思（ACR）**策略，让LLM从成功历史中学习推理逻辑，提升后续交互表现。
- **关键技术细节**：
  - **数据生成流程**（Decision Company）：
    1. 数据获取与预处理：从Kaggle收集5个领域18个主题的表格。
    2. 客户角色生成：管理员Agent创建具有多样背景的虚拟客户（Client Agent）。
    3. 分析场景模拟：Client Agent提出3个场景，人工选择最合适的1个。
    4. 计划讨论：数据科学家Agent与Client Agent对话，将需求细化为带条件的具体问题，并指定结果类型（如列表、数据框、图表）。
    5. 对话日志生成：AI聊天机器人Agent与数据科学家Agent交互，生成代码并分析结果，人工执行并验证、修复代码，作为静态历史保存。
    6. 私有库模式：人工将标准库函数重构为用户自定义函数，生成对应代码。
  - **评价指标**：
    - **Acc**：代码执行结果或选择题答案与参考答案的完全匹配率。
    - **AccR**：Acc基础上乘以私有库函数的召回率，衡量代码中正确使用用户定义函数的情况。
    - **CSE**（代码相似度等价）用于更细粒度的排名（附录K.6）。
  - **自适应对话反思（ACR）**：
    1. **伪代码逻辑生成**：对上一轮成功的交互（用户查询 + 正确代码），让LLM反思并生成中间推理的伪代码。
    2. **重组织单样本推理**：将历史成功案例组织为 `(用户输入; {伪代码; 答案})` 格式，作为当前轮的自生成单样本示例，引导模型先产生推理再生成回答。
- **公式**（Acc与AccR）：
  - Acc = (1/N) Σ I(C_i = Ĉ_i)
  - AccR = (1/N) Σ [I(C_i = Ĉ_i) · |F(C_i) ∩ F(Ĉ_i)| / |F(C_i)|]

## 3. 实验设计：数据集、基准、对比方法

- **数据集**：**CoTA** 包含1013个对话，1162个用户意图，覆盖 **Normal**（显式查询）、**Action**（需澄清/假设等6种动作）、**Private**（用户自定义库）、**Private Action**（结合私有库与动作）四种场景。答案类型分为代码生成（590个）和多选（423个）。平均对话轮次14.15。
- **Benchmark**：对比现有单轮数据集（HumanEval, MBPP, Spider, BIRD, DS-1000）和多轮数据集（SparC, CoSQL, ARCADE），显示CoTA在私有库、多轮、多模态、多种回答类型上最全面。
- **对比方法**：
  - **模型基座**（Model-Base）：直接提示LLM生成答案。
  - **Agent**：使用COT（代码生成）和CodeAct（多选题）加上工具（执行器、用户模拟器、图表转表格）。
  - **Agent-R**：Agent基础上增加文本反思。
  - **Multi-Agent**：多个专门Agent协作（控制器、代码Agent、决策Agent等）。
  - **Inter-Agent**：Agent + ACR策略。
  - 评估模型族：Mistral-7B、Mistral-8×7B、CodeLlama-34B、GPT-4-Turbo、Claude-3-Opus、GPT-4-32k、Llama-3.3-70B、Claude-3.5-Sonnet。
- **消融与错误分析**：200个错误样本的三种错误类型（Key Error、Lazy Assumption、Bad Instruction Following）以及私有库模式下的检索与生成错误。同时进行人类评估（500样本，10位外部专家）验证数据集质量。

## 4. 资源与算力

- 论文**未明确说明**使用的GPU型号、数量及训练时长。文中仅提及LLM推理（如GPT-4、Claude等），未涉及模型训练。标注成本统计：总花费$1,464.03（其中API调用$71.39，人工费用$1,392.66），每个CoTA实例约$1.45。
- 所有实验均在推理阶段完成，未进行微调或再训练，因此无法报告标准算力开销。

## 5. 实验数量与充分性

- **实验规模**：主实验（Table 4）覆盖8种LLM × 5种设置（Base, Agent, Agent-R, Multi-Agent, Inter-Agent），共40组对比。额外包含动作模式细粒度分析（Figure 6）、错误类型分布（Figure 7, Table 5）、私有库模式分析（Figure 12a）及人类评估（Table 3, Figure 4）。
- **充分性与公平性**：
  - 消融实验：Agent vs 基座、ACR vs 无ACR，验证各模块贡献。
  - 多场景覆盖：四种对话模式独立报告，体现不同难度。
  - 外部专家验证数据集质量，避免过拟合GPT生成偏差。
  - 指标设计避免简单匹配（如AccR评估私有库使用情况），并引入CodeT5+相似度进行辅助评估。
  - 不足：所有实验仅基于CoTA，未在其他多轮数据集上验证泛化性；API版本固定，未来模型更新可能改变结论。

## 6. 主要结论与发现

- **CoTA难度高**：最佳方法（Claude-3.5-Sonnet + Inter-Agent）仅达40.0%总体分，表明当前LLM在多轮表格数据分析中仍有巨大提升空间。
- **Agent模式带来显著提升**：工具、推理和反思均改善性能，ACR在大部分动作上优于普通Agent，相对提升最高达35.14%（Claude-3.5-Sonnet）。
- **私有库模式最具挑战**：最好模型仅18.0%，LLM难以正确选择和运用用户自定义函数，倾向于高召回却低精度或保守使用。
- **常见错误模式**：Lazy Assumption（39%）和Bad Instruction Following（49%）占主导，Key Error（23%）次之；模型经常假设中间结果已存在或不严格遵守指令。
- **Multi-Agent有效但成本高**：性能与Inter-Agent接近，但提示消耗高出5.3倍，不适合长对话。
- **人类参与显著提升数据质量**：人工校准后接受率从0.19-0.67升至0.93-1.00。

## 7. 优点：方法或实验设计亮点

- **创新数据生成流程**：利用多智能体沙盒（Decision Company）高效生成多样化、符合真实场景的对话数据，并融合人工校准保障质量，成本仅为传统方法的1/4。
- **全面评估维度**：涵盖正常、动作（6种）、私有库及组合场景，答案类型包括代码生成与多选题，评价指标兼顾执行正确性与函数使用召回率。
- **ACR策略简洁有效**：无需外部数据或微调，仅通过自生成的伪代码逻辑+历史重组织即可显著提升性能，且适用于不同LLM。
- **严格人类验证**：外部专家评估数据集质量，确保无偏见、逻辑连贯、脚本鲁棒；私有库模式采用三步转换流程（功能提取→重命名→代码重写），降低人工负担。
- **错误分析深入**：系统归类错误类型，揭示模型在指令遵循、状态假设、列名匹配方面的系统性问题。

## 8. 不足与局限

- **实验覆盖**：仅基于CoTA一个基准，未在更多多轮数据集（如CoSQL、ARCADE）上横向验证，泛化性存疑。
- **偏差风险**：数据生成过程依赖GPT-4，可能引入对该模型的偏好；ACR中的历史选择完全由LLM自身决定，若历史包含错误可能误导后续。
- **私有库模式表现较差**：当前LLM在准确检索和利用自定义函数方面能力不足，且评估指标AccR可能过于严苛（完全召回才得满分）。
- **资源默认**：未报告具体推理资源和时间，复现难度增加；也未尝试微调或提供持续学习方案。
- **应用限制**：静态评估（给定完整历史）与实际动态交互仍有差距；未考虑用户不耐烦、长上下文记忆退化等问题；多轮动作依赖真实用户模拟器（GPT-4），可能无法完全反映人类反馈。
- **数据集规模**：虽然覆盖多种场景，但1013个对话相对于真实世界海量分析场景仍较小，某些动作类型（如Update_Code仅6.9%）样本较少，统计意义有限。

（完）
