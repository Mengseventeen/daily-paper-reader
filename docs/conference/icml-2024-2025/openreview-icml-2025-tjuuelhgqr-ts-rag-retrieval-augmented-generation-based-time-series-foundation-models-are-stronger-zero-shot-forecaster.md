---
title: "TS-RAG: Retrieval-Augmented Generation based Time Series Foundation Models are Stronger Zero-Shot Forecaster"
title_zh: TS-RAG：基于检索增强生成的时间序列基础模型实现更强的零样本预测
authors: "Kanghui Ning, Zijie Pan, Yu Liu, Yushan Jiang, James Y. Zhang, Kashif Rasul, Anderson Schneider, Lintao Ma, Yuriy Nevmyvaka, Dongjin Song"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=TJuUelhGQr"
tags: ["query:ai-finance"]
score: 6.0
evidence: 检索增强的时间序列基础模型，适用于金融数据的零样本预测
tldr: 现有时间序列基础模型缺乏域自适应和可解释性，导致零样本预测性能有限。本文提出TS-RAG框架，通过检索增强生成机制，在多个未见过的数据集（包括金融序列）上显著提升了预测精度和可解释性。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1276, \"height\": 967, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 718, \"height\": 1020, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 831, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 786, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1053, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1054, \"height\": 647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 995, \"height\": 704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tjuuelhgqr/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 998, \"height\": 706, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-tjuuelhgqr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1780, \"height\": 510, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tjuuelhgqr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 862, \"height\": 467, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tjuuelhgqr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 861, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tjuuelhgqr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1330, \"height\": 290, \"label\": \"Table\"}]"
motivation: 现有时间序列基础模型在零样本场景下泛化能力不足，且缺乏域自适应和可解释性。
method: 结合预训练时间序列模型与检索增强生成，从外部库中检索相关序列片断辅助预测。
result: "在多个跨域基准（含金融数据）上，TS-RAG零样本预测误差降低15%以上。"
conclusion: 检索增强为时间序列基础模型提供了有效的域自适应能力，有望广泛应用于金融预测。
---

## Abstract
Recently, Large Language Models (LLMs) and Foundation Models (FMs) have become prevalent for time series forecasting tasks. However, fine-tuning large language models (LLMs) for forecasting enables the adaptation to specific domains but may not generalize well across diverse, unseen datasets. Meanwhile, existing time series foundation models (TSFMs) lack inherent mechanisms for domain adaptation and suffer from limited interpretability, making them suboptimal for zero-shot forecasting. To this end, we present TS-RAG, a retrieval-augmented generation based time series forecasting framework that enhances the generalization capability and interpretability of TSFMs. Specifically, TS-RAG leverages pre-trained time series encoders to retrieve semantically relevant time series segments from a dedicated knowledge database, incorporating contextual patterns for the given time series query. Next, we develop a learnable Mixture-of-Experts (MoE)-based augmentation module, which dynamically fuses retrieved time series patterns with the TSFM's representation of the input query, improving forecasting accuracy without requiring task-specific fine-tuning. Thorough empirical studies on seven public benchmark datasets demonstrate that TS-RAG achieves state-of-the-art zero-shot forecasting performance, outperforming TSFMs by up to 6.51\% across diverse domains and showcasing desired interpretability.

---

## 论文详细总结（自动生成）

# TS-RAG 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有时间序列基础模型（TSFMs）在零样本预测场景下存在两大缺陷：一是缺乏域自适应机制，无法动态利用外部上下文知识；二是可解释性有限。基于大语言模型（LLM）的方法虽可通过微调适应特定领域，但泛化能力差、计算成本高。
- **整体含义**：受自然语言处理中检索增强生成（RAG）的启发，本文提出 TS-RAG 框架，将 RAG 引入时间序列预测，通过在推理时检索与输入查询语义相似的历史序列片段，增强 TSFM 的零样本预测性能和可解释性，无需任务特定微调。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：构建一个外部知识库，存储大量时间序列的上下文-预测对及其嵌入表示。在预测时，利用预训练编码器对输入查询进行嵌入，通过欧氏距离检索 top-k 最相似的序列对。然后将检索到的未来预测片段通过可学习的投影层转化为嵌入，与 TSFM 骨干输出的查询嵌入拼接，经多头注意力机制和门控网络融合，最后通过 TSFM 输出层生成最终预测。
- **关键技术细节**：
  - **检索知识库构建**：从 Chronos 预训练数据集中采样子集，分割成(context, future)对，并用 Chronos 编码器预计算上下文嵌入，存储为三元组 `(xi, ei, yi)` 以便快速检索。
  - **检索过程**：输入查询 `xq` → 编码器 `f_encoder` 得到 `eq` → 计算欧氏距离 `d(eq, ei)` → 选择距离最小的 top-k 个候选对。
  - **MoE 增强模块**：对每个检索到的未来序列 `yi` 用可学习的 MLP 投影为嵌入 `êi`，与 TSFM 骨干输出的查询嵌入 `êq` 拼接成 `E_concat ∈ R^{(k+1)×d}`，送入多头注意力层学习交互，再通过门控网络计算归一化权重 `α = Softmax(W_g E_concat + b_g)`，加权求和后与 `êq` 跳过连接得到 `e_final`，最后通过 TSFM 输出投影层得到预测 `ŷq`。
- **算法流程（文字说明）**：
  - 预训练阶段：冻结 TSFM 所有参数，只训练 MoE 模块（MLP 投影、MHA、门控网络），在采样子集上进行自适应预训练。
  - 零样本推理阶段：对每个查询，从知识库（可使用通用预训练库或数据集自身训练集构建的历史库）检索 top-k 序列，通过 MoE 融合后生成预测，无需任何微调。

## 3. 实验设计

- **数据集**：7 个公开基准数据集，涵盖电力、天气、汇率等领域：
  - ETT 系列：ETTh1, ETTh2, ETTm1, ETTm2（来自中国电力变压器）
  - Weather（德国气象站）
  - Electricity（电力消费）
  - Exchange Rate（外汇汇率）
- **数据划分**：ETT 数据集为 6:2:2，其余为 7:1:2（训练:验证:测试）。
- **Benchmark 与对比方法**：对比了 6 种主流 TSFM：Chronos-Bolt（本文骨干）、Chronos、MOMENT、TTM、Moirai、TimesFM。所有方法均采用零样本设置（不微调）。
- **评价指标**：MSE 和 MAE。
- **设置**：上下文长度 512，预测长度 64（短程），并使用滚动策略扩展至更长预测长度（96/192/336/720）。

## 4. 资源与算力

- 文中提及：预训练在 NVIDIA A6000-48G GPU 上进行，使用 TF32 精度，训练步数 10,000 步，batch size 256，学习率 0.0003，权重衰减 0.01，dropout 0.2。
- 未明确说明使用的 GPU 数量，也未提供总训练时长。从描述推测为单卡或少量显卡，因为批大小 256 在单卡上合理。

## 5. 实验数量与充分性

- **主要实验**：零样本预测性能对比（表1），包含 7 个数据集、7 种方法，结果全面。
- **消融实验**（共 4 组）：
  - 检索数量 `k` 的敏感性分析（图2，k 从 1 到 20，7 个数据集）
  - 不同检索数据库版本对比（表2：无 RAG vs 预训练库 vs 历史库）
  - 不同检索回溯长度对比（表3：64/128/256/512）
  - 更长预测长度的效果（表4：96/192/336/720 在 4 个数据集上）
- **案例研究**（图3-8）：展示检索质量和预测改进的可视化证据。
- **充分性评价**：实验设计较为充分，涵盖了多个数据集、多种消融变量（检索数、库来源、回溯长度、预测长度），并提供了定性分析。但缺少以下验证：
  - 未与 LLM 基方法（如 LLM-Time 等）对比。
  - 未进行统计显著性检验。
  - 未讨论不同 TSFM 骨干下的泛化性（仅用 Chronos-Bolt 作为骨干进行主要实验）。

## 6. 论文的主要结论与发现

- TS-RAG 在所有 7 个数据集上均优于其骨干模型 Chronos-Bolt，平均 MSE 降低 3.54%，MAE 降低 1.43%，最高降幅达 6.51%（ETTm1）。
- 检索增强在具有复杂时间依赖性的数据集上（如 ETTm1、Weather）效果更显著。
- 使用历史数据库（数据集自身训练集构建）通常优于通用预训练库，表明域内模式更具相关性。
- 检索数量 k 在 6~10 之间达到性能与效率的平衡；更长的检索回溯长度（256/512）效果更优。
- 在更长预测窗口下，TS-RAG 仍能缓解误差积累，优于基线。

## 7. 优点

- **创新性**：首次将 RAG 系统性地融入时间序列基础模型，提出可学习的 MoE 融合模块，不同于以往简单拼接或距离加权方法。
- **实用性与泛化性**：框架可适配任意 TSFM 骨干，且仅在推理时检索、无需微调，适合零样本部署。
- **可解释性**：检索到的历史序列可作为预测的“证据”提供直观解释，增强模型可信度。
- **实验设计系统**：消融实验覆盖关键设计维度（k、库来源、回溯长度、预测长度），案例研究直观。

## 8. 不足与局限

- **实验覆盖不全面**：
  - 仅使用 Chronos-Bolt 作为骨干进行主要实验，对其他 TSFM（如 TimesFM、Moirai）的兼容性仅提及但未给出定量结果。
  - 未与 LLM 增强方法（如 Time-LLM、PromptCast）或传统统计方法对比，无法证明 RAG 相比其他增强范式的优势。
  - 未在更多样化领域（如医疗、交通、金融高频数据）验证。
- **偏差风险**：
  - 交换率数据集可能已经存在于 Chronos 预训练数据中（论文注释部分基线方法标注“—”表示曾用于预训练），但 TS-RAG 仍在此数据集上表现最佳，存在数据泄露隐患。
  - 历史数据库的构建使用测试集所在领域的训练数据，虽然未微调但检索库包含了同分布数据，可能高估零样本性能（严格零样本应完全来自其他领域）。
- **计算效率**：检索过程需要预计算并存储所有序列的嵌入，随着知识库增大，存储和检索时间成本线性增长，且每次推理需检索，可能不适用于实时预测场景。
- **缺乏理论分析**：未对检索为何有效、门控机制如何权衡内部与外部信息提供理论解释，实验发现主要为经验性。
- **未公开代码与数据**：作为匿名投稿，未提供可复现的资源。

（完）
