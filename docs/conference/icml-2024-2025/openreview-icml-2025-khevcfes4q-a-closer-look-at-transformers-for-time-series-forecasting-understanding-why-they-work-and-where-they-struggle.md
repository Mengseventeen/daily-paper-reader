---
title: "A Closer Look at Transformers for Time Series Forecasting: Understanding Why They Work and Where They Struggle"
title_zh: 再探时间序列预测中的Transformer：理解其工作原理与局限
authors: "Yu Chen, Nathalia Céspedes, Payam Barnaghi"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=kHEVCfES4Q"
tags: ["query:ai-finance"]
score: 6.0
evidence: 分析用于时间序列预测的transformer标记化策略，特别提到金融领域
tldr: 时间序列预测在金融等领域至关重要。本文深入分析了transformer中不同标记化策略（点式、块式、变量式）对预测性能的影响，解释了为何点式效果差以及复杂架构未必优于简单模型。该研究为金融时间序列模型设计提供了指导。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1614, \"height\": 300, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 790, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 1006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1669, \"height\": 1048, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1617, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 499, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-khevcfes4q/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1669, \"height\": 2345, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1651, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1714, \"height\": 292, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1796, \"height\": 461, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 846, \"height\": 156, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 586, \"height\": 200, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1857, \"height\": 823, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 840, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1376, \"height\": 671, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1675, \"height\": 1321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1681, \"height\": 1502, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1657, \"height\": 1492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1656, \"height\": 1492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1780, \"height\": 1495, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-khevcfes4q/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1830, \"height\": 1494, \"label\": \"Table\"}]"
motivation: Transformer在时间序列预测中表现优异，但其不同标记化策略的影响尚不明确，特别在金融等领域的适用性需要澄清。
method: 通过系统性实验比较点式、块式和变量式标记化在多个基准上的表现。
result: 发现简单transformer常优于复杂架构，点式标记化能力有限，块式和变量式各有优势。
conclusion: 该分析有助于指导金融时间序列预测中transformer的选型与设计。
---

## Abstract
Time-series forecasting is crucial across various domains, including finance, healthcare, and energy. Transformer models, originally developed for natural language processing, have demonstrated significant potential in addressing challenges associated with time-series data. These models utilize different tokenization strategies, point-wise, patch-wise, and variate-wise, to represent time-series data, each resulting in different scope of attention maps. Despite the emergence of sophisticated architectures, simpler transformers  consistently outperform their more complex counterparts in widely used benchmarks. This study examines why point-wise transformers are generally less effective, why intra- and inter-variate attention mechanisms yield similar outcomes, and which architectural components drive the success of simpler models. By analyzing mutual information and evaluating models on synthetic datasets, we demonstrate that intra-variate dependencies are the primary contributors to prediction performance on benchmarks, while inter-variate dependencies have a minor impact. Additionally, techniques such as Z-score normalization and skip connections are also crucial. However, these results are largely influenced by the self-dependent and stationary nature of benchmark datasets. By validating our findings on real-world healthcare data, we provide insights for designing more effective transformers for practical applications.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：Transformer模型在时间序列预测中表现出色，但不同标记化策略（point-wise、patch-wise、variate-wise）如何影响性能尚不清楚。尤其令人困惑的是，简单的Transformer（如iTransformer、PatchTST）常常优于更复杂的架构，而point-wise Transformer却普遍表现不佳。此外，intra-variate（变量内部）与inter-variate（变量间）注意力机制在基准上往往取得相似结果，这需要深入解释。
- **整体含义**：论文旨在揭示Transformer在时间序列预测中成功与失败的根源，为设计更有效的模型提供指导，同时警示当前基准数据集可能存在的偏差（高度自依赖、平稳性），并指出模型的选择应基于具体数据特性。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：通过模型无关的互信息指标，量化模型对“变量内依赖”和“变量间依赖”的捕捉能力，从而解释不同架构的行为。同时，利用合成数据集系统控制依赖强度，进行因果分析。
- **关键技术细节**：
  - **互信息指标（Intra MI / Inter MI）**：定义条件互信息 \( I(\hat{x}_j; x_i | x_{-i}) \)，由于模型输出对输入是确定的，该指标简化为条件方差 \( \sigma^2_{ij} \)，即固定其他变量时，预测值随第i个变量变化的离散程度。实际计算时，对每个样本生成5个变体（置零、保留原值、加不同噪声），估计 \( \bar{\sigma}_{ij} \)。当 \( i=j \) 为 Intra MI，否则为 Inter MI；进一步定义 Avg Inter MI 和 Max Inter MI。
  - **合成数据集**：生成2个变量的时间序列，控制自相关强度 \( \gamma \)（0.5低/0.95高）和变量间依赖强度 \( \alpha \)（0, 0.2, 0.4, 0.8），通过AR过程与正弦季节项叠加，并通过线性混合引入依赖。
  - **消融实验**：针对iTransformer模型，移除跳过连接（skip connections）、将变体无关解码器替换为变体相关解码器（Variate-Dependent Decoder，用二维卷积或平铺线性层实现），测试Z-score归一化的启用与否。
- **公式或算法流程（文字说明）**：
  1. 对每个待测模型，在给定数据集上训练后，对每个测试样本，复制生成5个变体（仅改变第i个变量的值）。
  2. 输入模型，得到预测值 \( \hat{x}_j \)。
  3. 计算每个时间步预测值的标准差 \( \sigma_{ij,k} \)，求所有样本和所有时间步的平均值，得到 \( \bar{\sigma}_{ij} \)。
  4. 对所有变量对计算，得到Intra MI (\( i=j \)) 和 Inter MI (\( i \neq j \))，再取平均或最大得到Avg/Max Inter MI。
  5. 将该指标与预测误差（MAE/MSE）进行相关性分析。

## 3. 实验设计
- **使用的数据集**：
  - **基准数据集**：Weather（21变量，10分钟采样）、Electricity（321变量，小时）、Traffic（862变量，小时）、ETT（ETTh1/ETTh2/ETTm1/ETTm2，7变量，小时/15分钟）。预测长度统一为{96,192,336,720}。
  - **合成数据集**：共8组，由 \( \gamma \in \{0.5,0.95\} \) 和 \( \alpha \in \{0,0.2,0.4,0.8\} \) 组合，2变量，小时数据，一年时长，预测长度同上。
  - **真实医疗数据集**：MINDER和TIHM（活动数据，8变量，小时，预测长度{48,96,192}）。
- **Benchmark与对比方法**：
  - 对比7种模型：Transformer（point-wise）、Autoformer、FEDformer、Crossformer、PatchTST、iTransformer、TimeXer。此外在消融实验中修改iTransformer架构。
  - 主要对比指标：MAE、MSE、Intra MI、Avg Inter MI、Max Inter MI；并计算这些MI指标与MAE的Spearman相关性。

## 4. 资源与算力
- 论文未明确说明使用的GPU型号、数量或训练时长。仅提到所有实验在Time Series Library统一配置下进行，结果平均3次随机种子运行。代码已在GitHub公开。

## 5. 实验数量与充分性
- **实验数量**：非常丰富。包括：
  - 基准数据集上7种模型对比（图4、附录图1），覆盖多个预测长度。
  - 合成数据集上对比（图5）。
  - 相关性分析（表2），涵盖9个基准数据集+8个合成数据集，计算MAE与Intra/Avg Inter/Max Inter MI的相关系数。
  - 消融实验（表3）：去跳过连接、替换变体相关解码器、两者皆改，在9个基准+8个合成数据上测试。
  - Z-score归一化消融（表4-5，附录表6-7）：4种模型在全部数据集上对比。
  - 医疗数据集验证（表5-7）：相关性分析加iTransformer变体测试。
  - 每个结果均报告均值与标准差（3次运行）。
- **充分性评价**：实验设计系统、全面。既覆盖主流基准，也通过合成数据控制变量，消融实验针对性强，且用真实医疗数据验证结论的局限性，客观性与公平性较高。

## 6. 论文的主要结论与发现
1. **Intra-variate依赖主导性能**：在基准数据集上，MAE与Intra MI高度负相关（r≈-0.7 ~ -0.94），而与Inter MI正相关或弱相关。说明模型成功的关键在于捕捉变量内部的时间模式，而非变量间关系。
2. **Point-wise Transformer不佳的原因**：由于其token包含所有变量同一时刻的值，注意力难以聚焦于单个变量的时间依赖，导致Intra MI低，Inter MI高但无助于预测。
3. **Intra-variate与Inter-variate注意力效果相似的原因**：在基准数据集中，变量间依赖很弱（即使采用inter-variate注意力的iTransformer，其Inter MI值也较低），因此两者实际上都在学习intra-variate模式，性能相近。
4. **关键架构组件**：
   - **跳过连接（skip connections）** 对捕捉intra-variate模式至关重要，去除后基准性能显著下降（尤其是Electricity和Traffic）。
   - **变体无关解码器** 有助于聚焦intra-variate依赖，但在合成数据中高inter-variate依赖时，变体相关解码器反而更好。
   - **Z-score归一化** 在平稳基准上大幅提升性能，但在非平稳合成数据（单调趋势）上会损害性能，说明其效果依赖数据平稳性。
5. **基准数据集的局限性**：常用基准数据集具有强自依赖、平稳、inter-variate依赖弱的特点，导致模型对比结果可能不能泛化到真实复杂场景。

## 7. 优点
- **创新性指标**：提出模型无关的互信息指标（Intra/Inter MI），可量化不同架构对依赖关系的捕捉，为分析Transformer行为提供了新工具。
- **系统合成数据控制**：通过自相关和变量间依赖两个维度生成合成数据，因果分析清晰，弥补了基准数据集的不足。
- **深入的消融实验**：逐个拆解iTransformer的关键组件（跳过连接、解码器设计、归一化），揭示各自作用，结论有说服力。
- **真实医疗数据验证**：在痴呆患者活动预测数据上验证发现，证明结论存在条件性，增强了实用性。
- **结果可复现**：代码公开，使用统一库，结果报告标准差（3次运行），保证可靠性。

## 8. 不足与局限
- **计算资源未报告**：未提及GPU型号、训练时长，不利于估算可复现成本。
- **基准数据集偏差**：如论文所述，基准数据集高度自依赖且平稳，导致结论可能不适用于具有强inter-variate依赖或非平稳的真实场景（如金融、事件序列）。
- **合成数据简化**：仅含2个变量，生成过程较简单（线性趋势+正弦季节），未能模拟更复杂的非线性依赖或高维多变量场景。
- **未覆盖所有前沿模型**：未包含LLM-based方法（如GPT4TS）、以及其他近期混合架构（如DLinear、N-BEATS），分析范围有限。
- **医疗数据集局限性**：仅两个数据集的少量参与者，可能代表性不足，且活动数据特性可能与通用时间序列有差异。
- **互信息指标近似性**：基于高斯假设和噪声扰动估计，可能无法精确捕捉非线性依赖，且需要多次推理，计算开销较大。

（完）
