---
title: "Deep Functional Factor Models: Forecasting High-Dimensional Functional Time Series via Bayesian Nonparametric Factorization"
title_zh: 深度函数因子模型：通过贝叶斯非参数分解预测高维函数时间序列
authors: "Yirui Liu, Xinghao Qiao, Yulong Pei, Liying Wang"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=dHXKCyaIkp"
tags: ["query:ai-finance"]
score: 7.0
evidence: 深度函数因子模型用于高维时间序列预测，可应用于金融
tldr: 高维函数时间序列预测面临建模困难，现有深度学习模型缺乏可解释性。本文提出深度函数因子模型（DF2M），结合印度自助餐过程与多任务高斯过程，融入深度核函数捕获非线性时序动态。在四个真实数据集上展示了优于黑盒模型的预测性能，同时保持良好的可解释性，适用于金融高频数据。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-dhxkcyaikp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1198, \"height\": 291, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-dhxkcyaikp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1575, \"height\": 870, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-dhxkcyaikp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1039, \"height\": 684, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-dhxkcyaikp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1171, \"height\": 1242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-dhxkcyaikp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 911, \"height\": 459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-dhxkcyaikp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1408, \"height\": 597, \"label\": \"Table\"}]"
motivation: 高维函数时间序列预测中，黑盒深度学习模型缺乏可解释性且难以捕获非线性动态。
method: 构建基于印度自助餐过程和多任务高斯过程的因子模型，在核函数中集成深度神经网络。
result: 在四个真实数据集上优于现有方法，并提供了可解释的因子结构。
conclusion: DF2M为金融等领域的高维时序预测提供了可解释的深度学习方案。
---

## Abstract
This paper introduces the Deep Functional Factor Model (DF2M), a Bayesian nonparametric model designed for analysis of high-dimensional functional time series. DF2M is built upon the Indian Buffet Process and the multi-task Gaussian Process, incorporating a deep kernel function that captures non-Markovian and nonlinear temporal dynamics. Unlike many black-box deep learning models, DF2M offers an explainable approach to utilizing neural networks by constructing a factor model and integrating deep neural networks within the kernel function. Additionally, we develop a computationally efficient variational inference algorithm to infer DF2M. Empirical results from four real-world datasets demonstrate that DF2M provides better explainability and superior predictive accuracy compared to conventional deep learning models for high-dimensional functional time series.

---

## 论文详细总结（自动生成）

# 深度函数因子模型（DF²M）论文详细总结

## 1. 核心问题与整体含义

- **研究动机**：高维函数时间序列（如多个国家的年龄别死亡率、多户家庭能耗曲线、多只股票日内回报轨迹）同时具有高维、函数型（无限维）和时序依赖三重挑战。传统统计方法（如VAR、功能性VAR）通常假设线性和马尔可夫动态，难以建模现实中的复杂非线性或非马尔可夫依赖。深度学习方法（如LSTM、GRU、注意力机制）虽能捕捉非线性，但本质是黑盒，缺乏可解释性，且在高维函数输入下参数过多、容易过拟合。
- **核心问题**：如何同时实现高维函数时间序列的高精度预测和模型可解释性？
- **整体含义**：本文提出**深度函数因子模型（DF²M）**，通过贝叶斯非参数因子模型实现降维和可解释性，并在隐因子动态中融入深度核函数以捕捉非线性和非马尔可夫依赖，从而在保持预测精度的同时提供清晰的跨截面与时间结构解释。

## 2. 方法论

### 核心思想
- 将观测到的高维函数时间序列表示为少数潜因子函数的时间序列的线性组合，其中因子负荷矩阵通过印度自助餐过程（IBP）诱导列稀疏性，使得每个因子只影响少数变量。
- 潜因子的时间演化由多任务高斯过程（MTGP）建模，其时间核函数由深度神经网络（LSTM/GRU/自注意力）构造，从而能够捕捉非线性、非马尔可夫动态。
- 整个模型是一个端到端的贝叶斯生成模型，通过变分推理进行后验推断。

### 关键技术细节
1. **稀疏函数因子模型**：
   - \( Y_t(\cdot) = (Z \odot A) X_t(\cdot) + \epsilon_t(\cdot) \)
   - \( Z \sim \text{IBP}(\alpha) \) 是无限列稀疏二进制矩阵；\( A \) 是负荷权重矩阵，每个元素独立正态先验。
   - 潜因子 \( X_t(\cdot) = [X_{t1}(\cdot), X_{t2}(\cdot), \dots]^\top \) 是无限维函数向量。

2. **函数型高斯过程动态模型**：
   - 对于每个因子 \( r \)，\( \{X_{tr}(\cdot)\}_{t=1}^n \) 构成一个多任务GP，协方差满足：
     \[
     \text{Cov}(X_{tr}(u), X_{sl}(v)) = \kappa_X(\mathcal{X}_{t-1}, \mathcal{X}_{s-1}) \cdot \kappa_U(u,v) \cdot I(r=l)
     \]
   - 时间核 \( \kappa_X \) 基于所有因子的历史信息（汇总后的特征）定义，空间核 \( \kappa_U \) 通常选择平方指数或Ornstein-Uhlenbeck核。

3. **深度时间核**：
   - 通过一个映射函数 \( F \)（例如取诱导点处的值）将函数 \( X_t(\cdot) \) 映射到低维向量。
   - 利用深度学习模块 \( H \)（LSTM, GRU, 自注意力等）处理该向量序列，输出隐表示 \( h_t \)。
   - 最终时间核为 \( \kappa_X(\mathcal{X}_{t-1}, \mathcal{X}_{s-1}) = \kappa(h_t, h_s) \)，其中 \( \kappa \) 是标准核函数。

4. **稀疏变分推理**：
   - 引入诱导点 \( v = (v_1,\dots,v_K) \)，所有因子共享相同的诱导点位置。
   - 变分分布 \( q(X_r(v)) = \mathcal{N}(\mu_r, \text{diag}(S_{1r},\dots,S_{nr})) \)。
   - ELBO推导见公式(8)，通过定理1-3实现了高效采样：后验均值仅依赖于同期的诱导点均值；后验方差分解为独立GP和公共MTGP两部分；ELBO中与独立GP无关的项可视为常数。
   - 训练时交替更新变分参数和深度学习模块参数，使用自动微分变分推断（ADVI）。

5. **预测**：
   - 一步预测均值由公式(12)给出：
     \[
     \bar{Y}_{n+1}(u) = (\bar{Z} \odot \bar{A}) \bar{X}_{n+1}(u), \quad \bar{X}_{n+1,r}(u) = \Sigma^{uv}_U (\Sigma^{vv}_U)^{-1} \mu_r \Sigma_X^{-1} (\Sigma^{n+1,1:n}_X)^\top
     \]

## 3. 实验设计

### 数据集（4个真实数据集）
| 数据集 | 变量数(p) | 时间点数(n) | 每曲线观测点数(K) | 描述 |
|--------|-----------|-------------|------------------|------|
| 日本死亡率 | 47 | 43 | 96 | 47个都道府县的年龄别死亡率（对数变换） |
| 能源消费 | 40 | 55 | 48 | 伦敦家庭半小时能耗（平均分组） |
| 全球死亡率 | 32 | 50 | 60 | 32个国家的年龄别死亡率（对数变换） |
| 股票日内回报 | 98 | 45 | 若干 | S&P 100成分股累积日内回报轨迹 |

### 基准方法
- 标准深度学习模型（无因子分解框架）：
  - LIN（全连接网络）
  - LSTM
  - GRU
  - ATTN（自注意力机制）
- 对比时保证相同的深度结构（隐藏层大小、层数等），DF²M中的深度模块与对应标准模型结构一致。

### 对比指标
- MAPE（平均绝对预测误差）和MSPE（均方预测误差）
- 滚动预测：训练窗口滚动，对h=1,2,3步预测进行评估。

### 额外对比
- 附录G中比较了多层深度学习和DF²M，显示DF²M在大多数情况下仍保持优势或持平。

## 4. 资源与算力

- 论文**未明确提及**所用的GPU型号、数量、训练时长等计算资源信息。仅描述了算法流程和变分推理的复杂度，未量化训练开销。
- 需要指出：这是常见情况，但缺少算力信息可能影响可复现性评估。

## 5. 实验数量与充分性

- **实验数量**：在4个数据集上，每个对比8种方法（4种DF²M变体 + 4种标准深度模型），针对h=1,2,3三个预测步长，共计4×8×3 = 96个点预测性能结果。此外，附录中还包含多层深度学习的对比实验（4个数据集，h=1,2,3），以及标准差的报告。可视化方面，展示了每个数据集的原始序列、潜因子动态、时间协方差矩阵。
- **充分性分析**：
  - 优点：覆盖了多种真实场景（死亡率、能耗、金融），数据维度从32到98，时间点数从43到55。对比了四种主流深度结构，确保了公平比较（相同隐藏层大小和层数）。
  - 不足：缺少消融实验，例如去掉IBP（固定因子数）、去掉深度核（使用简单核）、去掉多任务高斯过程（使用独立GP）等消融研究。未与其他贝叶斯非参数因子模型或深度高斯过程模型（如DeepGP）进行对比。缺乏对模型复杂度、训练时间、收敛性的系统分析。
- **客观性**：在给定的设置下，方法对比是公平的，但缺乏更广泛的基线（如VAR、FARIMA等传统时序方法）。结果展示了DF²M在大部分情况下的优越性，但也承认金融数据上DF²M-LIN更优，反映马尔可夫模型可能更合适。

## 6. 主要结论与发现

1. **预测精度**：DF²M的四种变体在绝大多数设定下（4数据集、3步长）都优于对应的标准深度学习模型，MSPE和MAPE相对降低10%~50%不等。例外：股票日内数据中DF²M-ATTN与标准ATTN精度接近；线性变体DF²M-LIN在股票上最优。
2. **可解释性**：DF²M提供了清晰的因子负荷稀疏结构，使得每个因子对应少数变量；时间协方差矩阵可直观展示自相关模式、周期性和突变点（如能源消费数据的周模式/圣诞节效应、死亡率数据的1980年代断点）。
3. **模型能力**：框架能够融合LSTM、GRU、注意力等任意序列深度模型，且在死亡率数据上注意力表现最佳，能源和全球死亡率上LSTM最优，股票上线性核更合适，表明模型具有适应不同时间依赖特性的灵活性。
4. **方法有效性**：通过因子分解降低输入维度，使得深度核能够在有限的训练样本（n<50）中有效学习，避免过拟合。

## 7. 优点

- **创新性结合**：首次将IBP稀疏因子模型与深度核高斯过程动态模型结合用于高维函数时间序列预测，保持了贝叶斯的概率结构和可解释性。
- **可解释性**：不同于纯粹黑盒深度学习，DF²M通过因子负荷、因子时间路径、时间协方差矩阵提供直观洞察，对金融、医疗等需要可解释性的应用尤为重要。
- **计算效率**：通过诱导点和定理1-3，在后验采样中将nL×nL矩阵运算简化为更小的K×K矩阵运算（K为诱导点个数），可实现高效变分推理。
- **灵活性**：支持多种深度序列架构（LIN、LSTM、GRU、自注意力），且允许用户根据数据特性选择合适的时间核。
- **实验稳健性**：在四个不同领域的数据集上验证，样本量较小（n<55），证明方法在小样本场景下的有效性。

## 8. 不足与局限

- **空间核简化**：论文依赖简单固定的空间核（如平方指数），未捕捉潜因子在函数域上的复杂结构（如非平稳性、多尺度模式）。作者在结论中承认这一点，并留作未来工作。
- **消融实验不足**：缺乏对模型各个组件的单独贡献分析，例如IBP的稀疏性、深度核 vs 简单核、多任务GP vs 独立GP等。这使得难以判断哪些部分最核心。
- **基线覆盖有限**：未与统计时序方法（如VAR、动态FPCA、因子模型+VAR）对比，也未见与深度高斯过程（Deep GP）或贝叶斯非参数时序模型对比。基准仅局限于标准深度学习，可能高估了相对优势。
- **预测范围**：仅做了点预测，未提供预测不确定性（如概率预测区间）。虽然高斯过程框架天然能给出不确定性，但文中未展示。
- **数据规模**：所有数据集时间点数小于55，虽然符合函数时序领域常见设定，但方法在更长序列上的适用性和可扩展性未检验。
- **博弈性**：训练需要交替更新变分参数和深度网络参数，收敛性保证未深入讨论（但变分推理通常收敛到局部最优）。
- **复现细节**：未提供GPU算力、训练时间等资源消耗，可能影响实际应用时的成本评估。

（完）
