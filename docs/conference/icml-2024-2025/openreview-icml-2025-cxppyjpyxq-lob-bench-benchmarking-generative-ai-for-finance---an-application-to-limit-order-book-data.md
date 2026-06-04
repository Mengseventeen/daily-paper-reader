---
title: "LOB-Bench: Benchmarking Generative AI for Finance - an Application to Limit Order Book Data"
title_zh: LOB-Bench：金融生成式AI基准——应用于限价订单簿数据
authors: "Peer Nagy, Sascha Yves Frey, Kang Li, Bidipta Sarkar, Svitlana Vyetrenko, Stefan Zohren, Ani Calinescu, Jakob Nicolaus Foerster"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=CXPpYJpYXQ"
tags: ["query:ai-finance"]
score: 10.0
evidence: 金融中生成式AI的基准，限价订单簿数据
tldr: 金融数据因高噪声、重尾和策略互动而极具挑战，但缺乏统一评估范式。本文提出LOB-Bench基准，用于评估限价订单簿数据生成的质量与真实性，通过条件与非条件统计量比较生成与真实数据分布。该基准支持灵活的多元统计评估，为金融生成式AI研究提供了标准化工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 861, \"height\": 354, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 588, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 865, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1772, \"height\": 293, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1760, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 855, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 862, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 852, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 839, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1657, \"height\": 582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 706, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1717, \"height\": 991, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1773, \"height\": 2005, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1764, \"height\": 1992, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1771, \"height\": 1998, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1772, \"height\": 1998, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 887, \"height\": 1977, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1777, \"height\": 1990, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 792, \"height\": 1371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 787, \"height\": 1914, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 657, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 648, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 672, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cxppyjpyxq/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1433, \"height\": 693, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-cxppyjpyxq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1734, \"height\": 719, \"label\": \"Table\"}]"
motivation: 金融数据生成缺乏定量评估标准，阻碍进展。
method: 构建基于Python的基准框架，通过分布差异统计评估生成数据的质量。
result: 支持包括常见LOB统计量在内的灵活多变量评估。
conclusion: LOB-Bench为金融生成式AI提供了可靠的评估平台，促进该领域发展。
---

## Abstract
While financial data presents one of the most challenging and interesting sequence modelling tasks due to high noise, heavy tails, and strategic interactions, progress in this area has been hindered by the lack of consensus on quantitative evaluation paradigms. 
To address this, we present **LOB-Bench**, a benchmark, implemented in python, designed to evaluate the quality and realism of generative message-by-order data for limit order books (LOB) in the LOBSTER format. 
Our framework  measures distributional differences in conditional and unconditional statistics between generated and real LOB data, supporting flexible multivariate statistical evaluation. 
The benchmark also includes features commonly used LOB statistics such as spread, order book volumes, order imbalance, and message inter-arrival times, along with scores from a trained discriminator network. Lastly, LOB-Bench contains "market impact metrics", i.e. the cross-correlations and price response functions for specific events in the data. 
We benchmark generative autoregressive state-space models, a (C)GAN, as well as a parametric LOB model and find that the autoregressive GenAI approach beats traditional model classes.

---

## 论文详细总结（自动生成）

# LOB-Bench：金融生成式AI基准——应用于限价订单簿数据 中文总结

## 1. 论文的核心问题与整体含义
- **研究动机**：金融时间序列数据（特别是高频限价订单簿 LOB 数据）具有高噪声、重尾分布和策略性交互的特点，是极具挑战性的序列建模任务。然而，该领域一直缺乏统一的定量评估标准，导致模型之间的比较往往依赖于定性分析（如“stylized facts”），难以客观衡量生成数据的真实性与质量。
- **整体含义**：论文提出了 **LOB-Bench**，一个基于 Python 的通用评估基准，旨在系统量化生成式 LOB 数据与真实数据之间的分布差异，为金融生成式 AI 提供标准化、可重复的评估工具，从而推动该领域的研究进展。

## 2. 论文提出的方法论
- **核心思想**：通过定义一系列“聚合函数”（scoring functions），将高维 LOB 时间序列映射到一维子空间，然后比较真实数据与生成数据在这些子空间上的分布相似性。支持**无条件评估**和**条件评估**（例如，基于时间或市场状态的条件分布），并引入**误差累积分析**（评估生成序列长度增加时分布漂移的程度）。
- **关键技术细节**：
  - **聚合函数**：包括常见 LOB 统计量（如买卖价差、订单簿不平衡、消息到达间隔时间、撤销时间、成交量等）以及训练好的判别器网络（作为最坏情况下的聚合函数）。
  - **距离度量**：使用 L1 范数（总变差距离，归一化到 [0,1]）和 Wasserstein-1 距离（对分布间距离敏感）。
  - **条件评估**：将条件变量分为 10 个分位数桶，对每个桶内的目标分布计算距离，并按桶的概率加权平均，得到条件损失。
  - **市场影响响应函数**：基于 Eisler et al. (2012) 的方法，计算六种事件类型（市场订单、限价订单、撤销订单，各分影响/不影响中间价）的价格响应曲线，并计算曲线间的平均 L1 距离。
  - **对抗性测量**：训练一个基于 1D-CNN + Attention 的判别器（分类器），以区分真实与生成轨迹，判别器的 AUC 分数作为额外指标。
- **算法流程（文字描述）**：
  1. 给定真实 LOB 数据和生成模型采样数据。
  2. 对每条序列，计算一系列聚合函数（如 spread、volume 等）。
  3. 用直方图估计这些聚合函数的分布（真实 vs 生成）。
  4. 计算分布间的 L1 或 Wasserstein-1 距离。
  5. 对于条件评估，先根据条件变量分桶，再对每个桶重复步骤 3-4，最终加权平均。
  6. 评估误差累积：将生成序列按时间步分段，比较不同段落的分布与真实对应段落分布的差异。
  7. 计算市场影响响应函数并求平均 L1 差异。
  8. 训练判别器，计算 AUC 分数。

## 3. 实验设计
- **数据集**：使用 LOBSTER 格式的 Alphabet Inc (GOOG) 和 Intel Corporation (INTC) 股票数据。LOBS5、RWKV、baseline 模型使用 2022 年全年训练数据，测试集为 2023 年子样本。Coletta 模型由于计算成本高，使用 2019 年 1 月三天训练、后三天测试。
- **基准方法**：对比了五种生成模型：
  - **LOBS5**：基于 S5 状态空间层的自回归模型（35M 参数），来自 Nagy et al. (2023) 的扩展版本。
  - **RWKV-4** 和 **RWKV-6**：基于 Peng et al. (2023, 2024) 的循环神经网络架构（170M 参数），直接对令牌化消息进行自回归预测，不包含订单簿状态。
  - **Coletta**：条件生成对抗网络（C-GAN），由 Coletta et al. (2022) 提出，仅适用于小 tick 股票（对 INTC 无效）。
  - **Baseline**：参数化 LOB 模型（Cont et al., 2010），使用经验到达率替代幂律拟合。
- **评估指标**：包括无条件分布距离（L1 和 Wasserstein-1）、条件分布距离、误差累积曲线、市场影响响应函数差异、判别器 AUC、以及下游任务（中间价趋势预测 MLP 的 F1 分数）。

## 4. 资源与算力
- **LOBS5 模型**：训练使用约 35M 参数，100 个 epoch，训练数据为 2022 年全年序列。总 GPU 时间为 **30.4 L40 天**（等价于 8 块 GPU 下 3.8 天）。所使用的 GPU 型号为 NVIDIA L40。
- **RWKV 模型**：训练了 2 种架构（RWKV-4 和 RWKV-6）× 2 个数据集（GOOG、INTC），总共使用 **10 L40S 天**（未明确说明 GPU 数量，提及使用 8 块 GPU？原文只说“在 8 块 GPU 上”？需确认：文中提到“training all 4 of our RWKV models ... took 10 L40S days”。未明确说明是否多卡并行，通常指单卡等效时间）。使用的优化器为 DAdapt-AdamW。
- **Coletta 模型**：由于计算成本高，训练周期短（3 天训练），本文未提供具体 GPU 时长。
- **Baseline 模型**：无需 GPU 训练，仅基于统计拟合。
- **说明**：论文在算力描述上较为透明，但部分模型（如 Coletta、RWKV）的训练细节不如 LOBS5 详细。

## 5. 实验数量与充分性
- **实验数量**：涵盖两个股票（GOOG 和 INTC），共比较了 5 种生成模型。主要实验结果包括：
  - 无条件分布距离（图 4、图 12、附录 E 多图）。
  - 误差累积分析（图 5、图 18）。
  - 市场影响响应函数比较（图 7、图 23）。
  - 判别器 ROC 曲线（图 21）。
  - 下游任务 F1 分数（图 8）。
  - 条件分布评估示例（图 19、图 20）。
  - 消融实验：探讨了 bin 大小对 L1 距离的影响（附录 D，图 11），验证了 Freedman-Diaconis 规则的稳定性。
- **充分性与公平性**：
  - 实验覆盖了不同 tick 大小（GOOG 为小 tick，INTC 为大 tick）、不同模型复杂度（从参数化模型到大规模自回归模型）。
  - 公平性：所有模型使用统一的数据格式和评估代码（开源），基准方法均忠实复现。但 Coletta 模型在 INTC 上失败，已明确说明原因（设计局限）。
  - 不足：未对 RWKV 模型进行消融实验（如不同 tokenizer 影响），也未探索模型规模的影响。判别器仅用于 LOBS5，未在其他模型上系统比较（但附录给出了 baseline 的 AUC 接近 1，说明判别器能轻易区分，间接表明其他模型质量较差）。

## 6. 论文的主要结论与发现
- **LOBS5 模型在整体上优于所有对比模型**：在 L1 和 Wasserstein-1 距离上均取得最低平均误差，能更好地重现市场影响曲线及条件分布。
- **自回归 GenAI 方法优于传统参数模型**：基线（Cont 模型）在离散统计量（如深度、层级）上表现尚可，但在时间相关和成交量指标上差距明显。
- **发现了“模型脱轨”问题**：随着生成序列增长（unroll steps），所有模型的分布误差逐渐增大（图 5、图 18），RWKV 模型误差累积最快，显示出“自回归陷阱”现象。
- **判别器分数仍是挑战**：即使 LOBS5 在多数指标上表现良好，判别器仍能以 0.83 的 AUC 区分真实与生成数据，说明存在未被传统统计量捕捉的细节差异。
- **下游任务表现**：使用生成数据辅助训练中间价预测模型并未提升 F1 分数（甚至有小幅下降），表明当前生成模型尚未能提供有益下游任务的数据增强。

## 7. 优点
- **评估框架全面**：同时支持无条件、条件、误差累积和市场影响响应评估，从多个角度衡量生成数据质量。
- **量化且可重复**：所有指标基于分布距离计算，避免了传统定性“stylized facts”比较的主观性；代码和预处理数据完全开源。
- **灵活可扩展**：用户可轻松添加自定义聚合函数或距离度量，适用于其他高维时间序列（如外汇、加密货币订单簿）。
- **引入了“对抗性测量”**：训练判别器作为最坏情况聚合函数，为模型改进提供了高难度标尺。
- **关注实际应用**：包括下游预测任务评估，验证了生成数据的实用性。
- **论文形式规范**：给出了详细的附录（训练细节、额外图、敏感度分析），增强了可复现性。

## 8. 不足与局限
- **模型覆盖有限**：仅评估了五种模型，未包括近期流行的扩散模型、基于 Transformer 的大型金融模型（如 FinGPT）等。RWKV 模型未经过精细调参（使用默认 byte-pair tokenizer 和预训练权重）。
- **分母规模可能影响结果**：LOBS5 模型参数为 35M，RWKV 为 170M，直接比较不公平（模型容量非常不同），但作者未进行同参数规模的消融。
- **判别器评估的局限性**：判别器仅在 LOBS5 上进行了完整分析（ROC 0.83），其他模型仅提及其 AUC 接近 1 但未给出精确值，缺少系统对比。
- **计算资源消耗大**：训练 LOBS5 和 RWKV 需要多 GPU 天数，可能限制可复现性（尽管代码开源）。
- **实验仅限两只股票**：GOOG 和 INTC 虽覆盖大小 tick，但无法代表整个市场（如低流动性股票、外汇等），泛化性未验证。
- **下游任务过于简单**：仅使用一个简单的 MLP 进行中间价三分类预测，未测试更复杂的 RL 交易策略或市场模拟等更贴近实际应用的场景。
- **市场影响响应函数忽略多级价格位移**：方法只考虑影响 best bid/ask 的事件（“touch orders”），忽略了更复杂的价格层次变化。
- **未进行统计显著性检验**：虽然给出了 bootstrap 置信区间，但未做正式假设检验来严格区分模型性能差异。

（完）
