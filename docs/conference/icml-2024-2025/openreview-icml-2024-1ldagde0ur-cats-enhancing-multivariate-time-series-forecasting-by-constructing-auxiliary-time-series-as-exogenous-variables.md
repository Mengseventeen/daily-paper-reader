---
title: "CATS: Enhancing Multivariate Time Series Forecasting by Constructing Auxiliary Time Series as Exogenous Variables"
title_zh: CATS：通过构建辅助时间序列作为外生变量增强多元时间序列预测
authors: "Jiecheng Lu, Xu Han, Yan Sun, Shihao Yang"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=1lDAGDe0UR"
tags: ["query:ai-finance"]
score: 8.0
evidence: 深度学习多元时间序列预测，可应用于股市
tldr: 多元时间序列预测中，单变量模型常优于多变量模型，存在不足。本文提出CATS方法，通过构建辅助时间序列作为外生变量，有效捕获序列间关系，即使使用简单MLP也能达到最优性能。该方法显著提升多变量预测准确度，可直接应用于金融时序分析。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 620, \"height\": 682, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 781, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 766, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 818, \"height\": 286, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 765, \"height\": 469, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1ldagde0ur/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1714, \"height\": 2315, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 663, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 858, \"height\": 398, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 201, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1773, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 863, \"height\": 403, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1765, \"height\": 370, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1777, \"height\": 1006, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1776, \"height\": 650, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1769, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1772, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1774, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1787, \"height\": 125, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1ldagde0ur/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1773, \"height\": 196, \"label\": \"Table\"}]"
motivation: 多元时间序列预测中，现有模型未能充分利用序列间关系，性能劣于单变量模型。
method: 提出CATS，从原始序列生成辅助时间序列，类似2D时序-上下文注意力机制，实现序列间关系表示。
result: 使用简单2层MLP作为核心预测器即达到最先进水平，大幅降低预测误差。
conclusion: CATS方法有效解决了多元模型的缺陷，为金融等领域的时序预测提供了强基线。
---

## Abstract
For Multivariate Time Series Forecasting (MTSF), recent deep learning applications show that univariate models frequently outperform multivariate ones. To address the deficiency in multivariate models, we introduce a method to Construct Auxiliary Time Series (CATS) that functions like a 2D temporal-contextual attention mechanism, which generates Auxiliary Time Series (ATS) from Original Time Series (OTS) to effectively represent and incorporate inter-series relationships for forecasting. Key principles of ATS—continuity, sparsity, and variability—are identified and implemented through different modules. Even with a basic 2-layer MLP as the core predictor, CATS achieves state-of-the-art, significantly reducing complexity and parameters compared to previous multivariate models, marking it as an efficient and transferable MTSF solution.

---

## 论文详细总结（自动生成）

# 论文核心问题与整体含义（研究动机和背景）

多元时间序列预测（MTSF）在金融、健康、交通等领域至关重要，需要同时建模序列内部的时间依赖性和序列之间的关联。然而，近年来的深度学习方法观察到一种反直觉现象：忽略序列间关系的单变量模型常常优于多变量模型。论文指出这可能源于两方面原因：一是真实基准数据集的序列间关系本身偏弱；二是现有多变量模型结构未能有效捕获序列间关系，反而容易过拟合或拟合错误模式。因此，核心问题是如何在保留单变量模型优势的同时，有效引入并利用序列间信息，从而提升多变量预测性能。

# 论文提出的方法论

## 核心思想

提出**CATS（Constructing Auxiliary Time Series）** 方法，通过构造辅助时间序列（ATS）作为外生变量，表征序列间关系，然后将其整合到原始时间序列（OTS）的预测中。该方法本质上类似于一种二维的“时间-上下文”注意力机制：ATS从OTS中抽取与多变量相关的信息，通过时间序列预测器将信息从输入域转移到输出域，最后通过线性投影融合到OTS输出。

## 关键技术细节

1. **ATS构造器**：设计了多种类型的ATS构造器 \( \mathcal{F}_m \)，用于从OTS输入生成ATS。包括：
   - **卷积**（不同核大小）
   - **非重叠卷积**（类似Patching）
   - **独立卷积**（每个序列独立卷积）
   - **线性投影**（逐点通道混合）
   - **恒等映射**（直接复制OTS）
   - **嵌入**（可学习的与时间相关的矩阵）
   多种构造器同时使用，提升灵活性。

2. **三个关键原则**：
   - **连续性**：通过连续性损失 \( \mathcal{L}_{\text{cont}} \) 平滑ATS，使其聚焦于长期趋势而非细节噪声，增强对序列间关系的表征。从谱密度和二次变差角度理论分析其低通滤波和去噪效果。
   - **稀疏性**：分为通道稀疏性和时间稀疏性。通道稀疏性通过注意力机制动态激活或抑制ATS通道，适应不同强度的多变量关系；时间稀疏性通过自适应截断机制为每个序列选择最优输入长度，避免固定长度带来的过拟合。
   - **变异性**：通过多种结构不同的ATS构造器（如卷积、线性、恒等、嵌入等）实现多样化的特征提取，确保模型能适应不同特性的数据集。

3. **预测与融合流程**：
   - 将OTS输入 \( X_I \) 和构造的ATS \( A_I \) 拼接，作为时间序列预测器 \( \Phi_{N+C} \) 的输入。
   - 预测器（默认简单2层MLP）输出第一阶段的预测 \( [\hat{A}_P, \hat{X}_P] \)。
   - 保留 \( \hat{X}_P \) 作为OTS短期路径（保留时间信息）。
   - 对 \( [\hat{A}_P, \hat{X}_P] \) 进行线性投影，得到 \( \tilde{X}_P \)（捕获多变量关系）。
   - 最终预测 \( \hat{X}_P^* = \hat{X}_P + \tilde{X}_P \)，即OTS短期结果与多变量修正结果相加。

4. **训练损失**：MSE + 连续性损失（权重 \( \beta_{\text{cont}}=1 \)）。

# 实验设计

## 数据集

- **常用基准数据集（9个）**：ETTm1, ETTm2, ETTh1, ETTh2（电力变压器温度/负荷）；Electricity（电力消耗）；Weather（气象变量）；Exchange（汇率）；Traffic（道路占用率）；Multi（ARM论文提出的人工数据集，含移位关系）。
- **延伸数据集**：MultiX（Multi20, Multi50, Multi100, Multi200），由主AR(1)序列经移位和叠加噪声生成，系列数更多（20-200个），以测试强多变量关系下的性能。

## Benchmark与对比方法

- 对比方法：ARM, PatchTST, DLinear, FEDformer, Autoformer, Informer, Repeat（重复最后值的朴素基线）。
- CATS使用简单2层MLP作为核心预测器，与上述方法公平比较。

## 实验设置

- 输入长度 \( L_I \)：CATS固定720（利用时间稀疏性自动调整），其他方法从{96,192,336,720}中选优。
- 预测长度 \( L_P \in \{96,192,336,720\} \)，共36个子实验（主实验）+ 16个延伸实验。
- 训练策略：last-value demeaning, random dropping，这些策略也应用于所有基线，确保公平。
- 评估指标：MSE（均方误差）和MAE（平均绝对误差），主报告平均MSE及相对Repeat的百分比。

# 资源与算力

- 文中明确提到使用**单个 Nvidia RTX 4090 GPU**，批量大小32，训练100轮，早停30步，学习率0.00005，线性衰减。
- 未明确给出总训练时长（如小时数），但提供了各模型的FLOPs和参数量比较（表5），显示CATS相比Transformer模型显著降低计算复杂度（例如LP=96时，CATS FLOPs 382M，ARM 426M，Autoformer 10.9G，Informer 9.41G）。

# 实验数量与充分性

- **主实验**：36组（9个数据集 × 4个预测长度），CATS在28组取得最佳，平均排名1.25。
- **延伸实验**：16组（4个MultiX数据集 × 4个预测长度），CATS在12组最佳。
- **消融实验**：大量消融，包括：
  - 不同时间序列预测器（2L, DLinear, Autoformer, IndLin, Mean）有/无CATS（表3，共20组）。
  - 三个原则的逐一/组合去除（表4，共16组）。
  - 不同ATS构造器的影响（表12，11组）。
  - 对更多早期方法（FITS, NBeats, TiDE, TimesNet, ARIMA）的增强（表11，40组）。
- **充分性判断**：实验覆盖了通用真实数据集和人工合成强关系场景，消融全面，对比基线涵盖近年主流方法。采用统一实验环境、固定输入长度、相同训练策略，公平性良好。但不足之处在于部分真实数据集（如ETT）本身多变量关系弱，导致CATS提升幅度较小，可能低估其潜力。

# 论文的主要结论与发现

1. CATS方法有效解决了多变量模型在MTSF中性能不佳的问题，即使配合简单2层MLP也能显著优于多种复杂模型（在28/36主实验、12/16延伸实验中取得最佳）。
2. ATS的三大原则（连续性、稀疏性、变异性）对性能至关重要，去除任何一个都会导致性能下降。
3. CATS的结构可轻松集成到不同时间序列预测器中（如DLinear、Autoformer等），带来稳定且显著的提升，在弱多变量关系下也能通过稀疏性防止过拟合。
4. CATS计算复杂度远低于Transformer模型，参数量更少，是一种轻量、易迁移的MTSF方案。
5. 该方法可视为一种高效的2D时序-上下文注意力机制，通过ATS构造、预测和投影实现序列间信息提取与融合。

# 优点

- **创新性**：首次提出通过构造辅助时间序列（ATS）作为外生变量来捕获序列间关系，概念新颖且理论分析扎实（谱密度、二次变差、ACF分离等）。
- **模块化与灵活性**：ATS构造器多样，可混合使用；三个原则通过可微分模块实现；核心预测器可任意替换，便于与现有模型结合。
- **鲁棒性**：在强弱多变量关系场景下均表现优异，通过稀疏性自适应调整ATS的激活，避免过拟合。
- **计算开销低**：使用简单MLP即可达到SOTA，FLOPs和参数量远小于Transformer模型，便于实际部署。
- **消融设计全面**：系统验证了每个组件（原则、构造器、OTS短期路径）的必要性，提供了深入理解。

# 不足与局限

- **ATS数量固定**：当真实序列间关系非常复杂，需要更多的ATS超出预设数量时，模型无法自动扩展（训练期间固定）。
- **数据集局限性**：真实基准数据集（如ETT）大多序列间关系较弱，导致CATS的提升在部分子实验中不够显著；人工数据集Multi/MultiX虽能展示潜力，但合成性质可能限制了结论的通用性。
- **可解释性不足**：虽然论文演示了简单移位问题的可解释例子，但对于复杂真实场景，ATS的具体含义和所学关系的可解释性尚未深入探讨。
- **未涉及在线或大规模场景**：实验在固定划分的离线数据集上进行，未测试模型在数据分布漂移、在线学习或超大规模（如数百个序列）下的表现。
- **公平性细节**：虽然对基线方法也应用了统一训练策略，但不同基线的最优输入长度是通过调参选择的（而CATS固定为720），这可能对部分基线不利；另外，CATS的3个原则和多个构造器引入了额外超参数，但论文未进行详细敏感性分析。

（完）
