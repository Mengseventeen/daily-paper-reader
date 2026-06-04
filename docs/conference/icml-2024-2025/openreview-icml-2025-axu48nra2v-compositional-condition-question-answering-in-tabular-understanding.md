---
title: Compositional Condition Question Answering in Tabular Understanding
title_zh: 表格理解中的组合条件问答
authors: "Jun-Peng Jiang, Tao Zhou, De-Chuan Zhan, Han-Jia Ye"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=aXU48nrA2v"
tags: ["query:ai-finance"]
score: 7.0
evidence: 改进表格组合条件问答，应用于财务报告分析
tldr: 多模态大语言模型在表格理解中处理组合条件问答时存在视觉编码器准确性和条件忽略问题。提出CoCoTab方法，通过增强表格结构关系建模和条件注意力，提升在财务报告分析等任务上的表现。实验表明CoCoTab能有效解决组合条件问题。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1760, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 771, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1728, \"height\": 797, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 753, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 789, \"height\": 406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 716, \"height\": 704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 759, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1764, \"height\": 798, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-axu48nra2v/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1697, \"height\": 706, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 722, \"height\": 551, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1469, \"height\": 638, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 688, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1203, \"height\": 894, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 777, \"height\": 705, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1201, \"height\": 742, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 875, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 622, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 650, \"height\": 339, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-axu48nra2v/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 656, \"height\": 340, \"label\": \"Table\"}]"
motivation: MLLMs在处理表格组合条件问答时性能有限，尤其在财务报告场景。
method: 提出CoCoTab方法，增强表格结构关系捕捉和条件引导注意力。
result: 在组合条件问答任务上显著提升性能。
conclusion: 为表格理解中的组合条件推理提供有效方案，助力金融分析。
---

## Abstract
Multimodal Large Language Models (MLLMs) for tabular understanding have made significant progress in tasks such as financial report analysis and public data tests. However, our comprehensive analysis shows that these models are still limited in certain simple scenarios, particularly when handling compositional conditions in QA. Further investigation reveals that the poor performance can be attributed to two main challenges: the visual encoder's inability to accurately recognize the content of a row, and the model's tendency to overlook conditions in the question.
To address these, we introduce a new Compositional Condition Tabular Understanding method, called {\sc CoCoTab}. Specifically, to capture the structural relationships within tables, we enhance the visual encoder with additional row and column patches. Moreover, we introduce the conditional tokens between the visual patches and query embeddings, ensuring the model focuses on relevant parts of the table according to the conditions specified in the query.
Additionally, we also introduce the Massive Multimodal Tabular Understanding (MMTU) benchmark, which comprehensively assesses the full capabilities of MLLMs in tabular understanding. Our proposed method achieves state-of-the-art performance on both existing tabular understanding benchmarks and MMTU.
Our code can be available at \url{https://github.com/LAMDA-Tabular/MMTU}.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：当前多模态大语言模型（MLLMs）在表格理解中的“组合条件问答”（Compositional Condition QA）任务上表现不佳。例如，回答“哪个村庄的负增长率最接近0？”时，模型常忽略“负增长率”这一条件，或错误对齐行/列内容。这类任务在财务报告分析、公共服务数据管理等场景中至关重要。
- **背景**：现有MLLMs在简单任务（如提取单元格值、识别行/列）上尚可，但在需要深层理解表格结构与条件组合的任务上严重受限。论文通过预实验（图1）发现，即使GPT-4o等闭源模型在组合条件任务上也仅达到约50%准确率，远低于人类水平。
- **整体含义**：揭示了MLLMs在表格理解中的两大瓶颈——视觉编码器无法准确捕捉表格行/列结构，以及模型容易忽略问题中的条件。本文旨在通过改进架构（行/列补丁+条件注意力）来提升组合条件QA能力，并构建更全面的评测基准MMTU。

### 2. 方法论：核心思想、关键技术细节、算法流程
- **核心思想**：
  - 增强视觉编码器对表格结构化信息的捕捉，通过额外引入行补丁和列补丁，保留样本级和属性级关系。
  - 引入条件标记（Conditional Tokens），通过交叉注意力机制让模型根据问题条件动态聚焦表格中的相关区域。
- **关键技术细节**：
  - **视觉编码增强**：在原始ViT标准补丁基础上，增加行补丁（宽度=图像宽，高度=补丁大小）和列补丁（高度=图像高，宽度=补丁大小），总补丁数从729增至783（仅增加7%）。
  - **多投影映射**：使用三个独立的MLP投影器分别将标准补丁、行补丁、列补丁映射到语言嵌入空间，保留各自的结构信息。
  - **条件注意力**：计算问题嵌入（Hq）与视觉特征（Hv）之间的交叉注意力：  
    H'_v = Attention(Q=Hq, K=Hv, V=Hv)  
    得到问题引导的视觉特征H'_v，与原始Hv、Hq一起输入LLM生成答案。
- **训练流程（两阶段）**：
  - **阶段1（补丁学习与模态对齐）**：冻结视觉编码器和LLM，训练三个投影器（包括行/列补丁投影），使用LAION、CC12M、PUB-1M、WTQ等图文对和表格QA数据。
  - **阶段2（表格理解指令微调）**：冻结视觉编码器，训练投影器和LLM，使用WTQ、TabFact、NAT-QA等表格QA数据，以及OCR-VQA等描述数据。

### 3. 实验设计
- **数据集与Benchmark**：
  - **现有基准**：WikiTableQuestions (WTQ)、TabFact、ComTQA。
  - **新基准MMTU**：包含4类任务（IE个体元素、RC行/列、CC组合条件、CR计算推理），共8921个QA对，覆盖10+领域，通过GPT-4生成+多模型投票+人工校准构建。
- **对比方法**：
  - 开源模型：LLaVA-1.6-7B/13B、Monkey、TextMonkey、mPlug-Owl、DocOwl、ShareGPT4V、VisCPM、InstructBLIP、Donut。
  - 闭源模型（附录及初步分析）：GPT-4o、Qwen-VL-Max、Qwen2-VL。
- **评估方式**：使用Qwen2.5-72B-Instruct作为评判器评估生成答案的正确性，避免GPT-4自身偏差。

### 4. 资源与算力
- **硬件**：4张NVIDIA A800 80GB GPU。
- **训练时长**：约5天（第一阶段1 epoch，第二阶段2 epoch）。
- **精度**：BF16 + TF32混合精度。
- **超参数**：第一阶段batch size=64，学习率2e-4；第二阶段batch size=32，学习率2e-6；视觉编码器学习率5e-7（仅第一阶段）。

### 5. 实验数量与充分性
- **主要实验**：
  - 主表（表2）：对比10个开源模型+CoCoTab在4个基准上的准确率。CoCoTab在所有基准上取得最佳（如MMTU总准确率0.68，CC准确率0.43远优于DocOwl的0.26）。
  - 消融实验（图5）：在MMTU上分解Baseline、加行/列补丁、加条件token、全组件，验证各部分贡献。
  - 错误分析（图2）：统计OCR错误率、缺失条件率、对齐错误率，解释模型失败原因。
  - 与结构化方法对比（表6）：与TAPEX、TaPas比较，CoCoTab在CC/CR任务上显著领先。
  - 计算开销对比（表7）：CoCoTab推理时间和内存与LLaVA1.6相近，增加有限。
  - 可视化注意力（图7）：证明行/列补丁和条件token在关键位置获取高注意力。
- **充分性与公平性**：实验覆盖多个数据集、多个维度，消融和对比完整。评估使用独立LLM评判器减少偏差，且对比方法均为公开可复现的模型。但主表未包含闭源模型（仅附录提供），这可能弱化了与SOTA的对比强度。

### 6. 主要结论与发现
- **发现**：当前MLLMs在组合条件任务上表现差，根源在于视觉编码器无法准确捕捉行/列结构（错误对齐）和模型忽略条件（遗漏条件）。
- **结论**：CoCoTab通过增加行/列补丁和条件注意力机制，显著提升表格理解中的组合条件QA能力，在MMTU CC任务上达到0.43（开源最佳DocOwl仅0.26），接近闭源模型水平。同时，MMTU基准能更全面、系统地评估表格理解能力。
- **局限性**：在计算/推理（CR）任务上提升有限，因主要依赖LLM本身的推理能力；与闭源模型仍有差距，主要受模型规模和训练数据限制。

### 7. 优点
- **方法轻量高效**：仅增加7% token数，计算开销极小，但性能增益显著。
- **创新性架构**：针对表格特点设计行/列补丁和条件注意力，方法简洁且可迁移。
- **系统化基准MMTU**：填补了现有基准缺乏标准图像格式、多维度评测的空白，为后续研究提供统一评估平台。
- **深入分析**：通过错误类型分析和注意力可视化，揭示了模型失败的根因，具有解释性。

### 8. 不足与局限
- **实验局限**：
  - 主表未直接与GPT-4o等闭源模型对比（仅在附录展示），可能低估与SOTA的差距。
  - MMTU基准虽覆盖多领域，但可能缺乏复杂表头、合并单元格等真实场景的表格变体。
  - 训练数据中部分由GPT-4生成，存在潜在噪声（尽管经人工校准）。
- **方法局限**：
  - 对计算/推理（CR）任务改善不大，因为其瓶颈在LLM的数学推理能力，而非视觉理解。
  - 行/列补丁假设表格为矩形规则布局，对不规则表格（如嵌套表格）可能适用性有限。
- **应用限制**：目前模型规模（基于Qwen2-7B）较小，在大规模工业场景下效果可能不如超大模型；未见在非英语表格上的表现验证。

（完）
