---
title: LAST SToP for Modeling Asynchronous Time Series
title_zh: 建模异步时间序列的LAST SToP方法
authors: "Shubham Gupta, Thibaut Durand, Graham W. Taylor, Lilian Bialokozowicz"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=TpP47EH1xG"
tags: ["query:ai-finance"]
score: 4.0
evidence: 异步时间序列建模，可用于金融事件序列
tldr: 针对异步时间序列（如金融事件序列）建模问题，本文提出一种面向大语言模型的提示设计和随机软提示机制，使模型能利用事件描述的自然语言进行推理。该方法将异步时间序列分析扩展到预测、异常检测和数据填补等多任务，为金融领域不规则事件建模提供了通用工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 868, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 828, \"height\": 231, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1730, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 852, \"height\": 299, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 846, \"height\": 742, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 689, \"height\": 816, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 842, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1512, \"height\": 457, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1766, \"height\": 593, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1659, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1410, \"height\": 699, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1755, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tpp47eh1xg/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1543, \"height\": 491, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 855, \"height\": 1089, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1359, \"height\": 472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1358, \"height\": 471, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1253, \"height\": 472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1780, \"height\": 389, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1781, \"height\": 391, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1782, \"height\": 648, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1772, \"height\": 1279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tpp47eh1xg/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1766, \"height\": 1352, \"label\": \"Table\"}]"
motivation: 现有时间序列模型假设等间距采样，但金融等领域的异步事件序列难以直接处理。
method: 提出专为异步时间序列设计的LLM提示机制，并引入随机软提示调优来提升性能。
result: 在多个域（包括金融相关事件）上，该方法在预测和异常检测任务中显著优于基线模型。
conclusion: 该方法有效利用自然语言事件描述，扩展了异步时间序列分析的能力范围。
---

## Abstract
We present a novel prompt design for Large Language Models (LLMs) tailored to **Asynchronous Time Series**. Unlike regular time series, which assume values at evenly spaced time points, asynchronous time series consist of timestamped events occurring at irregular intervals, each described in natural language. Our approach effectively utilizes the rich natural language of event descriptions, allowing LLMs to benefit from their broad world knowledge for reasoning across different domains and tasks. This allows us to extend the scope of asynchronous time series analysis beyond forecasting to include tasks like anomaly detection and data imputation. We further introduce **Stochastic Soft Prompting**, a novel prompt-tuning mechanism that significantly improves model performance, outperforming existing finetuning methods such as QLORA. Through extensive experiments on real-world datasets, we demonstrate that our approach achieves state-of-the-art performance across different tasks and datasets.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：传统时间序列建模假设均匀采样，而现实中的异步时间序列（如金融交易、社交媒体交互）由不规则间隔的自然语言事件描述组成。传统方法（如时间点过程 TPP）将事件映射到少量离散类别，丢失语义信息，难以扩展到大类别数量，且通常只支持预测任务。
- **背景**：大语言模型（LLM）在规则时间序列上已有应用，但直接处理异步时间序列的文本事件序列仍未被探索。
- **意义**：本文首次将 LLM 用于文本异步时间序列的多任务处理（预测、异常检测、数据填补），利用 LLM 的世界知识理解事件语义，避免了传统方法需要预定义类别、忽略事件交互和语义损失的缺陷。

## 2. 方法论：核心思想与关键技术

- **核心框架 – LASTS**：
  - 将异步时间序列表示为文本提示（prompt），包括系统提示（任务描述、数据集说明）、用户提示（事件序列：`(时间间隔, 事件描述)`）、助手提示（正确结果/待预测）。
  - 事件类型保留自然语言描述，时间用间隔表示；提示格式采用 `(时间, 事件)` 的顺序。
- **参数高效适配技术**：
  - **Soft Prompting (SP)**：在输入嵌入前添加可学习的连续软提示。
  - **Stochastic Soft Prompting (StoP)** —— 本文核心创新：
    - 训练时，对每个 batch 从软提示前缀中随机截取一段长度（均匀分布），仅使用该前缀参与前向/反向传播。
    - 优势：学习到粗到细的结构（早期 token 负责通用任务信息，后期 token 细化预测）；所有前缀均可作为独立提示使用；训练速度约比 SP 快 25%（更短前缀的 batch 更多）；在 Macro-F1 上平均比 SP 提升 12.69%，比 QLoRA 提升 13.55%。
  - **QLoRA**：作为另一种对比的 PEFT 方法（低秩分解 + 量化）。
- **模型 backbone**：LLaMA-3-8B-Instruct，训练时冻结主模型，仅更新软提示（1.6M 参数，占模型 0.02%）或 QLoRA 适配器（1.7M 参数）。

## 3. 实验设计

- **数据集**：
  - **文本动作数据集（3 个）**：Breakfast（177 类动作）、MultiTHUMOS（65 类动作）、EPIC-KITCHENS-100（约 20K 独特描述，如“拿碗”等自然语言）。事件描述直接作为文本输入。
  - **标准 TPP 数据集（5 个）**：Amazon（16 类）、Retweet（3 类）、Taxi（10 类）、Taobao（20 类）、StackOverflow（22 类）。此类数据集仅有事件索引（整数），仍可视作文本字符串输入。
- **任务**：预测（下一事件）、数据填补（遮罩位置预测）、异常检测（替换一个事件找出异常）。
- **对比方法**：
  - 随机基线
  - 专为时间序列设计的基础模型：Chronos（零样本预测）
  - 基于 LLM 的时间序列方法：LLMTime、LLM Processes
  - 传统 TPP 模型：RMTPP、NHP、SAHP、THP、AttNHP（仅在预测任务上比较）
  - 本文变体：LASTS Zero Shot / Few Shot、LASTS + QLoRA、LASTS + SP、LASTS + StoP
- **评估指标**：事件类型用 Macro-F1 和 Accuracy（因类别不平衡支持 Macro-F1），时间预测用 MAE 或 RMSE。
- **数据划分**：70% 训练、10% 验证、20% 测试。

## 4. 资源与算力

- **文中未明确说明**使用的 GPU 型号、数量、训练时长等信息。
- 仅提及训练时使用 LLaMA-3-8B-Instruct 作为骨干，且 StoP 训练速度比 SP 快约 25%（同样 400 长度的软提示）。但具体硬件规格未给出。

## 5. 实验数量与充分性

- **实验数量**：在 8 个数据集上执行了 3 个不同任务（预测、填补、异常检测），对每种方法均报告了指标，共包含：
  - 零样本 / 少样本 / 多种 PEFT 适配方法的对比。
  - 消融实验：提示变体（乱序名称、时间表示顺序、使用时长 vs 间隔）、StoP 与随机 token 选择对照、模型规模（1B/3B/8B）实验、不同 few-shot 数量（1-10）影响。
  - 模型分析：t-SNE 可视化、余弦相似度、前缀有效性、探测解释等。
- **充分性和公平性**：实验设计系统，涵盖了零样本、少样本、全量微调范式，对比了多种强基线（包括专门化的 TPP 模型和 LLM 方法），指标选择合理（Macro-F1 应对类别不平衡）。文本数据集和仅含索引的 TPP 数据集均被覆盖。实验在统计上未提及多次运行取平均，但总体结果稳健清晰。
- **不足之处**：对时间预测在部分数据集上（如 Amazon）不如 TPP，但作者提供了合理解释（缺乏时间分布先验）。此外未进行对模型不同训练成本的详细对比。

## 6. 主要结论与发现

- **LASTS 表示的有效性**：零样本 LASTS 在所有文本数据集和任务上优于 LLMTime、LLM Processes 和 Chronos，证明保留自然语言描述是关键优势。
- **StoP 显著优于标准 Soft Prompt 和 QLoRA**：平均 Macro-F1 提升 12.69%（vs SP）和 13.55%（vs QLoRA）；时间预测也通常更好。
- **在多类 TPP 数据集上，事件类型预测达到 SOTA**：在 18 项评估中 13 项最佳，17 项前两名。
- **模型规模扩展性**：从 1B 到 8B 参数，StoP 性能持续提升。
- **StoP 的粗到细结构**：t-SNE 和余弦相似度分析显示早期 token 更分散、后期更聚集；所有前缀均能独立作为有效提示。
- **Scrambled Names 实验**：去掉事件语义后性能大幅下降，证明 LLM 利用世界知识进行推理。

## 7. 优点

- **方法创新点**：
  - 首次将 LLM 用于文本异步时间序列的多任务处理，提出通用的 LASTS 提示框架。
  - StoP 是一种新颖的软提示调优机制，简单高效，可迁移到其他模态。
- **实验设计亮点**：
  - 覆盖多种数据集（文本和仅有索引）和多任务，对比充分。
  - 深入分析 Stope 的内部表征（t-SNE、余弦相似度），并展示其每个前缀的有效性。
  - 消融实验验证了提示结构、时间表示、随机性等设计选择的合理性。
- **实用价值**：参数高效（仅微调 0.02% 参数），易于部署在资源受限场景；无需为不同任务设计专用模型。

## 8. 不足与局限

- **时间预测精度有限**：在部分 TPP 数据集（如 Amazon）上时间预测不及专门化模型，主要因为缺乏对时间分布的显式建模（如泊松或 Hawkes 过程）。
- **计算资源细节缺失**：未报告 GPU 型号、数量、总训练时长，不利于他人复现和估算成本。
- **偏差风险**：未讨论 LLM 固有偏见对时间序列预测的影响，尤其是在高风险应用（如金融、医疗）中。
- **任务局限性**：异常检测任务定义简单（替换一个事件），更复杂的异常模式未涉及；且 LLM 可能受提示长度限制无法处理极长序列。
- **应用范围**：虽然提到可推广到金融等领域，但实验中未直接使用金融数据集；仅凭索引输入时性能有下降，依赖文本描述的质量。
- **可解释性**：软提示的“探测”虽有趣，但未提供定量的可解释性评估。

（完）
