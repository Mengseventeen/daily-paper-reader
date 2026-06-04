---
title: "Position: What Can Large Language Models Tell Us about Time Series Analysis"
title_zh: 立场：大型语言模型能为我们揭示时间序列分析的什么？
authors: "Ming Jin, YiFan Zhang, Wei Chen, Kexin Zhang, Yuxuan Liang, Bin Yang, Jindong Wang, Shirui Pan, Qingsong Wen"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=iroZNDxFJZ"
tags: ["query:ai-finance"]
score: 4.0
evidence: LLM用于时间序列分析，可应用于金融预测
tldr: 本文认为大型语言模型（LLM）有潜力彻底改变时间序列分析，促进高效决策，为金融时序预测等应用提供通用智能，但目前仍处于早期阶段。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 440, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1427, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 446, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 459, \"height\": 301, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 802, \"height\": 813, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1769, \"height\": 710, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 81, \"height\": 78, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 94, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 81, \"height\": 78, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 109, \"height\": 101, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 93, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 92, \"height\": 107, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 94, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-irozndxfjz/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 94, \"height\": 108, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-irozndxfjz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1437, \"height\": 249, \"label\": \"Table\"}]"
motivation: 现有时间序列模型依赖领域知识和大量调参，且主要集中在预测任务。
method: 本文提出观点，LLM可以利用其预训练语义空间增强时间序列分析。
result: 论证了LLM在时间序列分析中的潜力，但未提供具体实验结果。
conclusion: LLM有望推动时间序列分析迈向通用人工智能，但仍需进一步研究。
---

## Abstract
Time series analysis is essential for comprehending the complexities inherent in various real-world systems and applications. Although large language models (LLMs) have recently made significant strides, the development of artificial general intelligence (AGI) equipped with time series analysis capabilities remains in its nascent phase. Most existing time series models heavily rely on domain knowledge and extensive model tuning, predominantly focusing on prediction tasks. In this paper, we argue that current LLMs have the potential to revolutionize time series analysis, thereby promoting efficient decision-making and advancing towards a more universal form of time series analytical intelligence. Such advancement could unlock a wide range of possibilities, including time series modality switching and question answering. We encourage researchers and practitioners to recognize the potential of LLMs in advancing time series analysis and emphasize the need for trust in these related efforts. Furthermore, we detail the seamless integration of time series analysis with existing LLM technologies and outline promising avenues for future research.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：传统时间序列分析主要依赖统计模型和深度学习模型（如ARIMA、RNN、GNN），这些方法高度依赖领域知识、大量调参，且主要集中在预测任务（如预测、分类、异常检测）。这限制了时间序列分析的通用性和智能性，难以实现通用人工智能（AGI）在时间序列理解上的突破。
- **核心问题**：大型语言模型（LLM）是否有潜力作为通用时间序列分析的核心引擎？论文主张LLM可以彻底改变时间序列分析，实现从预测任务到通用分析智能的跃迁，包括时态模态转换、问答、交互式可解释分析等。
- **整体含义**：该论文是一篇立场论文，旨在激发研究社区对LLM用于时间序列分析的关注，并提出LLM可扮演三类角色：增强器（Enhancer）、预测器（Predictor）、智能体（Agent），从而推动更通用的时间序列分析系统。

### 2. 方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：将LLM视为时间序列分析的中心枢纽，利用其丰富的预训练语义空间和推理能力来弥补传统模型的不足。论文提出了三种集成形式：
  1. **LLM-assisted Enhancer（增强器）**：使用LLM增强数据（如生成文本描述、补充上下文）或增强模型（如通过双塔结构、对比学习将LLM知识注入时间序列模型）。关键技术包括：模板提示、冻结LLM + 可学习适配层。
  2. **LLM-centered Predictor（预测器）**：直接利用LLM进行时间序列预测或分类。分为两类：
     - **调谐法（Tuning-based）**：将时间序列分块（Patching）成补丁，与文本令牌一起输入白盒LLM，通过部分微调或适配层执行下游任务。公式：X_inp = Patching(X), T_inp = Tokenizer(T), Y_hat = Task( f_LLM (X_inp, T_inp, P) )。
     - **非调谐法（Non-tuning-based）**：对黑盒LLM，通过模板工程或定制Tokenizer将时间序列转化为LLM可理解的格式，再使用解析函数提取结果。公式：X_inp = Template(X, P) 或 Tokenizer(X), Y_hat = Parse( f_LLM (X_inp) )。
  3. **LLM-empowered Agent（智能体）**：将LLM作为高层面交互代理，能够理解用户查询、调用外部工具（如预训练时间序列模型库）、进行多步推理。论文通过提示工程让GPT-3.5作为零样本时间序列分析师，展示了在HAR数据集上的分类、数据增强、异常检测等任务，并分析了其能力与局限。

- **关键技术细节**：
  - 补丁化（Patching）操作参考了PatchTST（Nie et al., 2022）。
  - 对比学习对齐：如IMU2CLIP、STLLM使用对比学习对齐传感器文本与时间序列表示。
  - 提示增强：如Time-LLM使用文本作为提示前缀，将时间序列重新编程到语言空间。
  - 外部工具调用：参考Toolformer（Schick et al., 2024），LLM作为协调器调用专用模型。

- **公式/算法流程**：论文没有提出统一的新算法，而是对现有方法进行分类描述，上述公式（2）和（3）为示例性流程。

### 3. 实验设计：数据集、Benchmark、对比方法
- **实验场景**：论文并未进行大规模系统性基准实验，而是通过两个小型演示来验证LLM作为时间序列分析代理的零样本能力：
  1. **HAR（Human Activity Recognition）数据集**（Anguita et al., 2013）：来自30名受试者的智能手机惯性传感器数据，目标是将活动分类为Stand、Sit、Lay、Walk四类。使用了10个实例/类进行零样本分类测试（使用GPT-3.5）。
  2. **ETT（Electric Transformer Temperature）数据集**：用于演示数据增强和异常检测，包括油温及6个电力负载特征。论文展示了LLM生成类似模式的数据和识别异常点的能力（同样是零样本提示）。
- **Benchmark与对比方法**：论文没有设置正式的benchmark对比。在实验部分，仅展示了GPT-3.5在HAR上的混淆矩阵（图5），未与其他基线（如传统分类器或深度学习模型）比较。在LLM-centered Predictor讨论中，引用了其他研究（如Time-LLM、LLMTime）在多个数据集上的结果，但未在本论文中复现。
- **对比方法**：因论文是立场综述，未进行自身方法与其他方法的对比实验。

### 4. 资源与算力
- **文中明确说明**：论文未提及使用的GPU型号、数量、训练时长等算力资源。实验部分仅调用GPT-3.5 API进行零样本推理，未涉及训练。
- **结论**：未报告算力，因为实验规模极小，且论文本身不追求计算开销分析。

### 5. 实验数量与充分性
- **实验数量**：仅有两个简单演示实验：一个分类（HAR，10个实例/类），一个数据增强+异常检测（ETT，少量实例）。此外，在5.1节进行了定性分析（混淆矩阵、对话记录）。
- **充分性评估**：
  - **不充分**：作为实证支持其立场缺乏力度。没有在标准时间序列基准（如Monas、Lub、ETTx、UCR等）上对比多种方法，也没有进行消融实验或统计检验。
  - **客观性**：实验结果（如混淆矩阵）是客观的，但缺乏对比基线，无法判断LLM相对于传统方法的优劣。对于幻觉、偏差等问题的分析是定性且主观的。
  - **公平性**：未提供复现代码或详细设定，实验可重复性有限。

### 6. 主要结论与发现
- LLM可以作为有效的零样本时间序列分析代理，在简单分类、数据增强、异常检测任务上展现了一定能力（如Stand类100%正确分类）。
- LLM提供了良好的可解释性（以自然语言解释判断理由）和诚实性（当不确定时会主动承认）。
- 但LLM存在明显局限：
  - 对复杂时间序列模式理解不足，可能拒绝回答或产生幻觉（如生成虚假数据或错误解释）。
  - 存在语言分布偏差（如Lay被误分类为Sit和Stand）。
  - 幻觉问题严重：生成的数据可能是简单复制，而分类理由可能是编造的。
- 未来方向：增强时间序列知识融入（特征对齐、融合、外部工具调用）；减少幻觉（可靠提示、指令微调）；发展多智能体系统；处理概念漂移和持续学习。

### 7. 优点
- **视野前瞻**：首次系统性地将LLM在时间序列分析中的角色划分为增强器、预测器、智能体三类，提供了一个清晰的路线图，有助于领域研究者定位和比较不同方法。
- **文献综述全面**：附录A列出了大量相关研究，并进行了分类（增强器/预测器/智能体），为读者提供了丰富的参考文献。
- **基于实证的讨论**：尽管实验规模小，但通过具体案例（对话记录）直观展示了LLM的行为特性（可解释性、幻觉、偏差），使论点更具说服力。
- **提出了未来方向**：如特征对齐、外部工具调用、多智能体系统等，具有启发性。

### 8. 不足与局限
- **实验不充分**：缺乏大规模、标准化的定量实验来支撑“LLM可以彻底改变时间序列分析”这一核心主张。仅依赖于两个小规模零样本演示，且没有与现有最优方法（SOTA）比较。
- **缺乏消融与分析**：未对LLM不同角色（增强器/预测器/智能体）进行公平比较，也未对调谐法与非调谐法的性能差异进行实验验证。
- **偏差风险**：作者自身立场可能导致对LLM潜力的过度乐观，例如文中多次声称“LLM具有巨大潜力”，但实验却展示了其易产生幻觉和偏差的问题，可能选择性呈现了有利结果。
- **应用限制**：
  - LLM的推理成本高、速度慢，不适合实时或大规模时间序列分析。
  - 数据隐私和安全性问题未深入讨论（仅提及）。
  - 对于高精度数值任务（如金融预测、医学信号），LLM的数值处理能力有限（如Tokenizer不适合连续数值）。
  - 幻觉问题未得到有效解决，降低了可靠性和可信度。
- **方法论局限性**：论文本身是立场论文，没有提出新的算法或模型，因此缺乏可复现的技术贡献。

（完）
