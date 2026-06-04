---
title: Graph-based Time Series Clustering for End-to-End Hierarchical Forecasting
title_zh: 基于图的时序聚类用于端到端层次预测
authors: "Andrea Cini, Danilo Mandic, Cesare Alippi"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=nd47Za5jk5"
tags: ["query:ai-finance"]
score: 5.0
evidence: 基于图的时序预测方法，可迁移至股票市场分析
tldr: 时间序列预测中利用关系归纳偏置可提升效果。提出基于图的端到端层次预测方法，将关系性和层次性归纳偏置统一到金字塔图结构中，通过可训练图池化算子学习层次。该方法无需预设层次，可用于金融市场的多尺度预测。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-nd47za5jk5/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 850, \"height\": 273, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nd47za5jk5/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1773, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nd47za5jk5/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1592, \"height\": 1191, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nd47za5jk5/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1197, \"height\": 770, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-nd47za5jk5/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1602, \"height\": 482, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nd47za5jk5/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 730, \"height\": 677, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nd47za5jk5/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 830, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nd47za5jk5/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 757, \"height\": 417, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nd47za5jk5/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 598, \"height\": 223, \"label\": \"Table\"}]"
motivation: 现有预测方法未能统一利用关系性和层次性归纳偏置。
method: 构建金字塔图结构，使用可训练图池化算子学习层次，端到端预测。
result: 在多个时序数据集上表现优异，自动学习层次结构。
conclusion: 提供可迁移的时序预测框架，适用于金融市场分析。
---

## Abstract
Relationships among time series can be exploited as inductive biases in learning effective forecasting models. In hierarchical time series, relationships among subsets of sequences induce hard constraints (hierarchical inductive biases) on the predicted values. In this paper, we propose a graph-based methodology to unify relational and hierarchical inductive biases in the context of deep learning for time series forecasting. In particular, we model both types of relationships as dependencies in a pyramidal graph structure, with each pyramidal layer corresponding to a level of the hierarchy. By exploiting modern - trainable - graph pooling operators we show that the hierarchical structure, if not available as a prior, can be learned directly from data, thus obtaining cluster assignments aligned with the forecasting objective. A differentiable reconciliation stage is incorporated into the processing architecture, allowing hierarchical constraints to act both as an architectural bias as well as a regularization element for predictions. Simulation results on representative datasets show that the proposed method compares favorably against the state of the art.

---

## 论文详细总结（自动生成）

## 论文中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：时间序列预测中，利用序列间的关系（关系归纳偏置）和层次结构（层次归纳偏置）可以提升预测精度。然而，现有方法通常分别处理这两种偏置，缺乏统一的框架。特别地，在层次时间序列中，不同层次的聚合约束（如“相加等于总和”）是硬约束，但传统方法往往先独立预测再事后协调，没有完全嵌入到端到端学习中。
- **核心问题**：如何将关系性归纳偏置（图结构）和层次性归纳偏置（聚合约束）统一到一个可学习的深度预测框架中，并且当层次结构未知时，能直接从数据中学习出有意义的层次聚类，同时保证预测的协调性。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：构建金字塔图结构（pyramidal graph），每个层级对应层次结构的一层，层内通过图神经网络（GNN）传播信息，层间通过图池化（graph pooling）算子（选择、缩减、连接）实现信息向上聚合和向下传递。如果层次结构先验未知，则使用可训练的图池化（如Gumbel Softmax + 直通估计器）学习硬聚类分配，使得聚类优化直接服务于预测目标（自监督）。最后，在架构中嵌入可微的预测协调（reconciliation）层，强制预测满足协调性约束。
- **关键技术细节**：
  - **Select（选择）**：学习一个选择矩阵 \( S^{(k)} \in \{0,1\}^{N_{k-1} \times N_k} \)，将下层节点映射到上层超节点。参数化方式：通过可训练函数 \( F_\psi \) 输出分数矩阵 \( \Phi^{(k)} \)，再经Gumbel Softmax采样得到离散分配。
  - **Reduce（缩减）**：通过 \( S^{(k)T} H^{(k-1)} \) 聚合节点特征到上层。
  - **Connect（连接）**：重新连接上层图的边权重（\( S^{(k)T} A^{(k-1)} S^{(k)} \)）。
  - **Lift（提升）**：将上层表示投影回下层（\( S^{(k)} H^{(k+1)} \)）。
  - **层次化消息传递**：每个层级先进行GNN消息传递，再通过缩减和提升操作与相邻层级交互，更新节点表示。
  - **预测协调**：利用投影矩阵 \( P = I - Q^T(QQ^T)^{-1}Q \) 将原始预测投影到协调子空间（\( Q \) 由选择矩阵构建）。训练时同时最小化原始预测误差、协调后预测误差以及两者间的正则项。
  - **正则化**：引入基于归一化割的图聚类正则项 \( L_c \)，鼓励聚类保留图连通性并避免退化。
- **训练流程**：整体端到端训练，损失函数包含各层级预测误差、协调正则项和图聚类正则项。

### 3. 实验设计：数据集、基准、对比方法
- **数据集**：
  - 交通预测：Metr-LA（207节点，34,272时间步）、PeMS-Bay（325节点，52,128时间步）。
  - 空气质量：AQI（437节点，8,760时间步）。
  - 能源消耗：CER-E（485节点，25,728时间步）。
  - 所有数据集均有图结构（邻接矩阵），但无预定义的层次结构。
- **基准与对比方法**：
  - 参考架构（TTS）：RNN、FC-RNN（多变量）、GConv-TTS（图卷积）、Diff-TTS（扩散卷积）、Gated-TTS（门控消息传递）、GUNet-TTS（图U-Net）。
  - 消融变体：HiGP-TTS（C/D/G）分别对应不同消息传递算子；HiGP (T)（调优版含残差连接）。
  - 额外对比交通数据集上的SOTA：DCRNN、GWNet、Gated-GN、SGP。
- **评估指标**：平均绝对误差（MAE）、平均相对误差（MRE）。预测步长：Metr-LA/PeMS-Bay为12步，CER-E为6步，AQI为3步。

### 4. 资源与算力
- **明确提到**：实验运行在配备AMD EPYC 7513 CPU和NVIDIA RTX A5000 GPU的服务器上。未提供具体训练时长或GPU数量。代码已开源（https://github.com/andreacini/higp）。

### 5. 实验数量与充分性
- **主要实验结果**（表1）：在4个数据集上，对比9种方法（含HiGP三种变体），每个实验5次运行取均值和标准差。结果充分覆盖不同数据集和模型变体。
- **额外实验**（表2）：在2个交通数据集上对比4种SOTA方法，并进行了消融（移除消息传递、移除层次传播）。
- **敏感性分析**（附录表4、表5）：测试不同层级数量、聚类数量、协调策略的影响。
- **定性分析**（图3、图4）：展示了CER-E和AQI数据集上学到的聚类模式及空间分布。
- **充分性评价**：实验覆盖了多个领域、多种图卷积算子、设计消融、敏感性分析，并提供了定性评估。整体较充分，公平性良好（代码开源，超参数与基线按原论文设置或调优）。

### 6. 论文的主要结论与发现
- HiGP在多个基准上达到或超越SOTA，尤其在交通预测数据集上表现最佳。
- 层次归纳偏置（通过预测多个聚合层级）本身就能提升预测精度，即使层次结构是学习得到的。
- 端到端学习聚类分配可以产生有意义的层次结构（如能源消费模式聚类、空气质量区域聚类）。
- 协调正则化和消息传播对最终精度均有显著贡献（消融实验证实）。

### 7. 优点
- **统一框架**：首次将关系性和层次性归纳偏置统一在端到端图神经网络中，既适用于已知层次也适用于未知层次。
- **自监督聚类**：通过预测误差自动学习聚类，无需额外标签，且能结合图拓扑正则化。
- **可微协调**：将协调步骤嵌入网络，使约束成为架构的一部分，同时作为正则化项。
- **广泛验证**：在交通、能源、空气质量多个领域验证，并进行了充分的消融和敏感性分析。
- **代码开源**：促进可复现性。

### 8. 不足与局限
- **扩展性**：协调投影需要求逆矩阵 \( (QQ^T)^{-1} \)，复杂度 \( O(M^3) \)，论文指出仅适用于数千节点场景。虽然提供正则化替代方案，但硬投影在大规模系统中可能不可行。
- **聚类参数需手动设定**：层次数量、每层簇数等超参数需根据任务调优（附录敏感性显示对性能有影响）。
- **实验覆盖**：仅测试了中等规模数据集（数百节点），未在更大规模（如数万时间序列）或异构/不规则采样数据上评估。
- **未考虑概率预测**：仅做点预测，未扩展到概率层次预测。
- **应用限制**：主要针对静态图拓扑和同质传感器，扩展至动态图、多元时间序列或异质数据需额外研究。
- **偏差风险**：实验中超参数（如正则系数λ）通过在单个数据集上调优后按比例缩放至其他数据集，可能引入偏差；但总体调优过程公平。

（完）
