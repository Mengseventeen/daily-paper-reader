---
title: "MF-CLR: Multi-Frequency Contrastive Learning Representation for Time Series"
title_zh: "MF-CLR: 多频率对比学习表示用于时间序列"
authors: "Jufang Duan, Wei Zheng, Yangzhou Du, Wenfa Wu, Haipeng Jiang, Hongsheng Qi"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=ecO7WOIlMD"
tags: ["query:ai-finance"]
score: 8.0
evidence: 金融领域多频率时间序列表示学习
tldr: 针对金融领域常见多频率时间序列（如日度股指、月度失业率、季度收入），提出MF-CLR自监督对比学习框架，通过层次化机制学习跨频率的表示，无需标注即可提取有效特征，为后续预测任务提供高质量输入。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1692, \"height\": 692, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 815, \"height\": 376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 832, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 764, \"height\": 842, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 754, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1572, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-eco7woilmd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1706, \"height\": 495, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 851, \"height\": 627, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 870, \"height\": 745, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 862, \"height\": 803, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 866, \"height\": 767, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 855, \"height\": 653, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1756, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1525, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1773, \"height\": 2269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1754, \"height\": 829, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1758, \"height\": 1214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1761, \"height\": 1091, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1761, \"height\": 738, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-eco7woilmd/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1760, \"height\": 1020, \"label\": \"Table\"}]"
motivation: 金融数据常包含不同采样率的稀疏标记协变量，现有方法难以统一表示。
method: 提出MF-CLR，利用对比学习在前馈层次结构中融合多频率时间序列。
result: 在金融时间序列表示任务上取得优于现有方法的性能。
conclusion: MF-CLR能有效学习多频率时间序列的通用表示，促进下游金融预测。
---

## Abstract
Learning a decent representation from unlabeled time series is a challenging task, especially when the time series data is derived from diverse channels at different sampling rates. Our motivation stems from the financial domain, where sparsely labeled covariates are commonly collected at different frequencies, *e.g.*, daily stock market index, monthly unemployment rate and quarterly net revenue of a certain listed corporation. This paper presents **M**ulti-**F**requency **C**ontrastive **L**earning **R**epresentation (MF-CLR), aimed at learning a good representation of multi-frequency time series in a self-supervised paradigm by leveraging the ability of contrastive learning. MF-CLR introduces a hierarchical mechanism that spans across different frequencies along the feature dimension. Within each contrastive block, two groups of subseries with adjacent frequencies are embedded based on our proposed cross-frequency consistency. To validate the effectiveness of MF-CLR, we conduct extensive experiments on five downstream tasks, including long-term and short-term forecasting, classification, anomaly detection and imputation. Experimental evidence shows that MF-CLR delivers a leading performance in all the downstream tasks and keeps consistent performance across different target dataset scales in the transfer learning scenario.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：金融领域的真实数据通常来自不同采样率（频率）的稀疏标记协变量，例如日度股指、月度失业率、季度公司净收入。现有自监督时间序列表示学习方法大多假设数据是单频率的，直接将多频率输入视为单频率的多维序列，忽略了频率间的结构关系，导致在真实多频率场景下性能不佳。
- **核心问题**：如何从无标签的多频率时间序列中学习高质量的联合表示，以支持下游任务（预测、分类、异常检测、缺失值填补等）。
- **整体含义**：提出 MF-CLR，一种专为多频率时间序列设计的自监督对比学习框架，通过层次化机制和跨频率一致性，学习从高频到低频的通用表示，无需人工标注即可提取有效特征，为金融等领域的预测和决策提供更好的基础。

### 2. 论文提出的方法论
- **核心思想**：沿特征维度按频率从高到低分层处理，每层通过“跨频率对比块”学习相邻频率子序列的联合表示。利用实例级对比（Instance-wise Contrast）维持同频率内不变性，并引入跨频率一致性（Cross-frequency Consistency）将低频信息融入高频表示，最终递归汇总所有频率信息。
- **关键技术细节**：
  - **双扭曲（Dual Twister）**：一种新颖的数据增强方法，在时间维度和数值维度同时扰动原始序列，保持语义相似性且不破坏频率结构。通过概率对齐策略生成扭曲视图，并保证总偏差不超过动态时间规整（DTW）距离的上界。
  - **跨频率一致性**：两个性质：
    1. 高频子序列的表示应满足实例间一致性（正负样本对区分）。
    2. 低频子序列越相似，对应的高频表示在潜空间中应越接近。
  - **层次化训练**：从最高频率块开始，依次训练每个块的编码器，块输出由本层编码后的高频表示与经非线性投影的低频子序列拼接而成，作为下一块的输入。
- **损失函数**：每个块由实例损失 \( \mathcal{L}_{\text{inst}} \) 和跨频率损失 \( \mathcal{L}_{\text{freq}} \) 组成，二者加权平均（超参数 \( \alpha \)）。实例损失为标准对比损失；跨频率损失使用改进的二次对比损失，拉近低频距离相近的样本的高频表示。
- **算法流程**（文字说明）：
  1. 输入多频率时间序列，按频率分组（从高到低）。
  2. 对第 \( j \) 个块，用 Dual Twister 增强当前高频子序列 \( z_j \) 得到 \( \tilde{z}_j \)。
  3. 使用共享编码器分别编码 \( z_j \) 和 \( \tilde{z}_j \)，得到 \( h_j \) 和 \( \tilde{h}_j \)。
  4. 计算实例损失和跨频率损失（利用 \( h_j \) 与低频序列 \( x^{j+1} \) 的距离）。
  5. 更新编码器参数，将 \( h_j \) 与投影后的 \( x^{j+1} \) 拼接作为下一块输入。
  6. 重复直到所有频率处理完成。

### 3. 实验设计
- **数据集与场景**：
  - **分类**：30个 UEA 多变量时间序列数据集，预处理为多频率版本。
  - **异常检测**：SMD、SMAP、MSL、SWaT 四个公开数据集。
  - **短期/长期预测**：Traffic、ETTm1、ETTm2、Weather。
  - **缺失值填补**：同预测数据集，掩码比例 12.5%、25%、37.5%、50%。
  - **真实金融案例**：美国和中国各25只股票的股价预测与季度净收入预测，涵盖稳定和波动市场。
- **基准方法**：
  - **自监督方法**：T-Loss、TS-TCC、TNC、CPC、TS2Vec、CoST、TF-C。
  - **监督方法**：DeepAR、TCN、DLinear、PatchTST、TimesNet、Autoformer、Informer、FEDformer。
- **评价指标**：分类用准确率、精确率、召回率、F1、AUC；异常检测用准确率、精确率、召回率、F1；预测和填补用 MSE、MAE；金融案例用 MAPE。

### 4. 资源与算力
- 论文中**未明确说明**使用的 GPU 型号、数量、训练时长或总能耗。仅提及超参数设置（batch size=32，学习率1e-3，编码器为4层膨胀卷积等），但未给出具体算力细节。

### 5. 实验数量与充分性
- **实验数量**：覆盖5个下游任务，包含多个数据集（UEA 30个、SMD/SMAP/MSL/SWaT 共4个、Traffic/ETTm1/ETTm2/Weather 共4个），以及2个真实金融案例（各25只股票，两种市场状态）。消融实验验证了每个组件（Dual Twister、跨频率对比、低频投影器、层次化结构）的效果，并探索了编码器选择、参数规模等。转移学习实验（ETTm1→ETTm2 和反向）在5种目标数据规模下进行了对比。总计上百组对比实验结果。
- **充分性与公平性**：
  - 对比方法包括现有最先进的自监督和监督方法，覆盖全面。
  - 所有自监督方法采用相同的下游评估流程（SVM/岭回归），避免下游模型差异带来的偏差。
  - 数据集均为公开或合理构建，但需注意：为了适应多频率设定，作者对部分单频率数据集进行了人为重采样（如将部分维度降采样），这虽然体现了方法的设计目标，但仍与真实多频率场景存在一定差距。整体实验设计较为充分客观。

### 6. 论文的主要结论与发现
- **核心结论**：MF-CLR 在所有五个下游任务上均取得领先或竞争力强的性能，特别是在分类、异常检测、短期/长期预测中超越所有自监督方法，并在部分任务上超越监督方法。
- **发现**：
  - 层次化跨频率学习比简单拼接或单频率对比更有效。
  - Dual Twister 增强策略优于传统 jittering、scaling 等。
  - 跨频率一致性损失显著提升多频率表示质量。
  - 在转移学习场景下，MF-CLR 在小目标数据集（25%~50%）上稳定性远优于监督方法，展示了自监督预训练的优势。
  - 真实金融案例中，MF-CLR 在股价和净收入预测上平均 MAPE 最低或次低，验证了实际应用价值。

### 7. 优点
- **方法创新**：专门针对多频率时间序列设计，打破了现有方法对单频率的隐含假设；层次化结构和跨频率对比是原创性贡献。
- **数据增强**：Dual Twister 提供了一种保持频率结构的可控增强方式，理论上界清晰（DTW距离上界）。
- **实验全面**：覆盖多种下游任务、多个领域（交通、天气、金融），消融实验充分，转移学习评估了数据规模敏感性。
- **实际验证**：包含真实金融案例，证明方法在工业场景的可用性。

### 8. 不足与局限
- **计算资源未报告**：没有提供训练时间、GPU型号等信息，不利于复现和效率对比。
- **数据集预处理的人为性**：为构建多频率数据集，对原本单频率的数据进行了重采样（如将部分维度降采样），这可能改变了原始数据的时间结构，实验结果是否能完全推广到自然多频率数据有待进一步验证。
- **对比方法覆盖局限**：未与最新的时间序列基础模型（如 TimeGPT）或更先进的预训练方法比较（虽讨论中提到，但实验中未纳入）。此外，部分自监督方法（如 TNC）在原论文中表现不佳，可能是多频率设定导致的不适应。
- **依赖频率划分**：实验要求输入按频率分组，实际应用中若频率信息不明确或特征维度无法清晰划分，则方法需要额外预处理。
- **未讨论噪声或缺失频率的情况**：真实场景中可能存在频率未知或特征完全缺失，论文未涉及。

（完）
