---
title: Loss Shaping Constraints for Long-Term Time Series Forecasting
title_zh: 长期时间序列预测的损失形状约束
authors: "Ignacio Hounie, Javier Porras-Valenzuela, Alejandro Ribeiro"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=9CCoVyFuEp"
tags: ["query:ai-finance"]
score: 4.0
evidence: 长期时间序列预测，可应用于金融领域
tldr: 针对长期时间序列预测中各步误差分布不均的问题，提出一种约束学习框架，在保持平均性能的同时对特定步的误差设置上限。该方法在金融等领域有潜在应用价值。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 764, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1757, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1471, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1526, \"height\": 481, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 805, \"height\": 821, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 821, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 820, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 819, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 760, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1692, \"height\": 1235, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1680, \"height\": 1315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 805, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 880, \"height\": 1805, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9ccovyfuep/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1600, \"height\": 2163, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1462, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1464, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1326, \"height\": 443, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1625, \"height\": 2136, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1602, \"height\": 2064, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1624, \"height\": 2138, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1509, \"height\": 2142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 803, \"height\": 542, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9ccovyfuep/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1612, \"height\": 452, \"label\": \"Table\"}]"
motivation: 现有模型优化平均性能，导致预测窗口内某些时间步的误差过大，在金融预测中风险很高。
method: 在优化目标中增加用户定义的上界约束，通过约束优化调整误差分布。
result: 在多个公共基准上，该约束方法有效降低了指定步的误差，同时不损害平均性能。
conclusion: 该工作为提高长期预测的鲁棒性提供了新思路，可适应金融等对特定步误差敏感的应用。
---

## Abstract
Several applications in time series forecasting require predicting multiple steps ahead. Despite the vast amount of literature in the topic, both classical and recent deep learning based approaches have mostly focused on minimising performance averaged over the predicted window. We observe that this can lead to disparate distributions of errors across forecasting steps, especially for recent transformer architectures trained on popular forecasting benchmarks. That is, optimising performance on average can lead to undesirably large errors at specific time-steps. In this work, we present a Constrained Learning approach for long-term time series forecasting that aims to find the best model in terms of average performance that respects a user-defined upper bound on the loss at each time-step. We call our approach loss shaping constraints because it imposes constraints on the loss at each time step, and leverage recent duality results to show that despite its non-convexity, the resulting problem has a bounded duality gap. We propose a practical primal-dual algorithm to tackle it, and demonstrate that the proposed approach exhibits competitive average performance in time series forecasting benchmarks, while shaping the distribution of errors across the predicted window.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：在长期多步时间序列预测中，传统模型（包括经典方法和近期Transformer架构）通常仅优化整个预测窗口的平均损失（如MSE），导致各时间步的误差分布极不均匀。图1展示了一个典型例子：Autoformer在外汇数据集上，部分步骤的测试MSE远高于其他步骤。这种不均匀性在金融风险评估、模型预测控制等场景中是危险的——仅关注平均性能可能掩盖某些步骤的严重偏差。
- **研究动机**：需要一种方法能在保持平均性能的同时，对每个时间步的损失施加显式控制，避免训练出的模型在特定步产生不可接受的误差。
- **整体含义**：论文提出一种**约束学习（Constrained Learning）**框架，称为“损失形状约束”（Loss Shaping Constraints），通过引入上界约束自动调整误差在预测窗口内的分布，实现“既要平均好，又要各步稳”。

### 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

- **核心思想**：将多步预测转化为约束优化问题——最小化整个窗口的平均损失，同时要求每个时间步的期望损失不超过用户指定的阈值ϵ_i。这形如 (P-LS) 问题：
  - min_θ E[1/T_p Σ ℓ_i]   s.t.  E[ℓ_i] ≤ ϵ_i, i=1,…,T_p。
- **关键技术细节**：
  1. **约束的自适应松弛——弹性约束学习（Resilient Constrained Learning）**：当用户设定的ϵ_i太紧导致无可行解时，引入非负松弛变量ζ_i，将约束放松为 E[ℓ_i] ≤ ϵ_i + ζ_i，并最小化松弛代价 h(ζ)（如L2范数）。通过联合优化找到最优松弛，使得问题始终可行。
  2. **对偶理论与近似保证**：尽管模型（如Transformer）是非凸的，但论文利用最近对偶性结果证明该约束问题的对偶间隙有界，因此通过求解经验对偶问题能获得近似最优解。
  3. **原始-对偶算法（Algorithm 1）**：交替进行：
     - 对模型参数θ做梯度下降（更新 Lagrangian 中加权损失项）；
     - 对松弛变量ζ做梯度投影：ζ ← [ζ - η_ζ(∇h(ζ)-λ)]_+；
     - 对偶变量λ做次梯度上升：λ ← [λ + η_d (batch上的约束违反度)]_+。
  最终返回θ、λ、ζ。
- **算法文字说明**：训练时，每个batch先计算当前模型下各步损失与约束的差值，据此更新松弛变量和拉格朗日乘子，再更新模型参数。乘子λ_i刻画该步约束满足的“难度”。

### 3. 实验设计：数据集、基准、对比方法

- **数据集**：9个流行公共数据集，覆盖电力（ECL）、天气（Weather）、汇率（Exchange Rate）、交通（Traffic）、变压器温度（ETTh1/ETTh2/ETTm1/ETTm2）、流感类疾病（ILI）。每个数据集测试4种预测窗口长度（96/192/336/720，ILI为24/36/48/60）。
- **基准（Baseline）**：未约束的ERM（标准训练）。
- **对比方法**：论文对比了三种训练策略——ERM、带硬约束的“Ours”（Constant）、带弹性约束的“Ours+R”。模型包含8种架构：Autoformer、Informer、Reformer、Pyraformer、Transformer（vanilla）、Nonstationary Transformer、iTransformer、FiLM（非Transformer）。
- **实验结果**：报告了每个设置的测试MSE和窗口标准差（Window STD），并相对ERM归一化展示。

### 4. 资源与算力

- 论文未明确说明使用的GPU型号、数量、训练时长等具体算力信息。仅提到“follow the same setup, including preprocessing, hyperparameters and implementation, as described in”各原始模型论文（如Kitaev et al., 2019; Wu et al., 2021等），因此可推断实验是在类似环境下进行，但无法确认具体资源。

### 5. 实验数量与充分性

- **实验数量**：总计 8种模型 × 9个数据集 × 4种长度 = 288 个实验设置，每个设置下还进行了超参数网格搜索（6个ϵ值）以及ERM、Ours、Ours+R三种方法的比较，保守估计至少上千个训练运行。附录还包含了消融分析（不同ϵ值的影响）、弹性与硬约束的对比、单调递增约束的测试。
- **充分性与公平性**：
  - 覆盖了主流Transformer变体及一个非Transformer模型，数据集多样性高（金融、气象、交通、医疗）。
  - 使用相同的预处理、数据拆分（7:1:2）、滚动窗口，并且修复了此前工作中的bug（最后Tp样本丢弃问题），确保基线公平。
  - 但存在潜在偏差：超参数ϵ的网格搜索基于训练/验证误差的百分位数，可能过度调优；部分模型（如Reformer在某些设置下）约束后反而劣化，但论文分析了原因（泛化间隙或不可行）。
  - 总体实验设计充分，结果详实，结论可信。

### 6. 论文的主要结论与发现

- 约束学习能有效“塑形”损失分布：平均而言，与ERM相比，约束后窗口标准差降低约3.47%，MSE也降低约4.47%。
- 灵活优先：恒值约束（Constant）和弹性约束（Resilient）各有优势，弹性约束在解决不可行问题时尤其有效，甚至可提升泛化（如iTransformer在多个数据集上获得最低MSE或最低标准差）。
- 约束效果因模型和数据集而异：例如Autoformer在天气数据上通过约束实现更平坦的损失曲线，而Informer在外汇数据上约束后同时提升平均性能。
- 约束水平选择需谨慎：过紧的约束可能导致训练不可行，过松则无效果；弹性约束提供了自动松弛机制，降低调参难度。

### 7. 优点：方法或实验设计上的亮点

- **方法创新**：将约束学习引入时序预测，直接对预测窗口内各步损失独立约束，而非简单加权；提出的弹性约束机制无需手动调松弛系数。
- **理论贡献**：证明非凸参数化下的对偶间隙有界，为算法提供理论支撑。
- **实验广度**：288个主实验 + 多种消融，结果以归一化形式清晰呈现，便于跨设置比较。
- **可解释性**：拉格朗日乘子λ_i直接反映各步约束的满足难度，为模型调试提供洞察。
- **实用性**：算法简单（原-对偶梯度更新），易于集成到现有训练流程中。

### 8. 不足与局限

- **调参敏感性**：方法仍需对约束水平ϵ进行网格搜索（虽仅6个值），在大型模型上开销较高。
- **泛化间隙问题**：存在训练时约束可行但测试时失效的情况（如图5所示），论文归因于统计泛化误差，但未提出针对性缓解措施。
- **常数约束的假设**：论文主要实验采用各步相同ϵ，而实际应用中各步可容忍误差可能不同（如长期预测更宽松），虽探索了指数增长约束，但未系统比较最优约束类型。
- **计算资源未提及**：无法直接评估方法的训练成本（可能比ERM略高，因为需维护对偶变量和松弛变量）。
- **模型覆盖有限**：虽然包括了8种架构，但未覆盖最新的大规模时序基础模型（如TimeGPT、Lag-Llama），且未与加权损失、直接优化分位数等方法充分对比。
- **应用场景讨论不足**：虽提及金融、模型预测控制，但未在真实下游任务中验证约束带来的收益（如风险度量、控制稳定性）。

（完）
