---
title: "Auctionformer: A Unified Deep Learning Algorithm for Solving Equilibrium Strategies in Auction Games"
title_zh: Auctionformer：求解拍卖博弈均衡策略的统一深度学习算法
authors: "Kexin Huang, Ziqian Chen, Xue Wang, Chongming Gao, Jinyang Gao, Bolin Ding, Xiang Wang"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=VnI9200eeL"
tags: ["query:ai-finance"]
score: 6.0
evidence: 深度学习方法求解拍卖均衡，可应用于交易和金融市场
tldr: 拍卖游戏在在线广告和房地产等交易场景广泛，但求解均衡面临多样性高和计算复杂挑战。提出Auctionformer，基于Transformer的通用框架，通过灵活令牌化将不同拍卖转换为标准序列，统一求解。方法高效且泛化，适用于金融交易场景。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1412, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1261, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 712, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 853, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 597, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 557, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1555, \"height\": 1197, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1201, \"height\": 453, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1059, \"height\": 521, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1570, \"height\": 1819, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 706, \"height\": 554, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1056, \"height\": 521, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-vni9200eel/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1055, \"height\": 522, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 775, \"height\": 275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 734, \"height\": 826, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 854, \"height\": 250, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 938, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1770, \"height\": 188, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 735, \"height\": 444, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1098, \"height\": 186, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1774, \"height\": 345, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-vni9200eel/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 930, \"height\": 527, \"label\": \"Table\"}]"
motivation: 现有方法对特定拍卖设定依赖，资源需求高。
method: 提出Auctionformer，利用Transformer和令牌化统一表示拍卖游戏。
result: 高效求解多种拍卖均衡，泛化性强。
conclusion: 为拍卖博弈提供统一深度求解方案，可扩展至金融交易。
---

## Abstract
Auction games have been widely used in plenty of trading environments such as online advertising and real estate. The complexity of real-world scenarios, characterized by diverse auction mechanisms and bidder asymmetries, poses significant challenges in efficiently solving for equilibria. Traditional learning approaches often face limitations due to their specificity to certain settings and high resource demands. Addressing this, we introduce *Auctionformer*, an efficient transformer-based method to solve equilibria of diverse auctions in a unified framework. Leveraging the flexible tokenization schemes, Auctionformer translates varying auction games into a standard token series, making use of renowned Transformer architectures. Moreover, we employ Nash error as the loss term, sidestepping the need for underlying equilibrium solutions and enabling efficient training and inference. Furthermore, a few-shot framework supports adaptability to new mechanisms, reinforced by a self-supervised fine-tuning approach. Extensive experimental results affirm the superior performance of Auctionformer over contemporary methods, heralding its potential for broad real-world applications.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究问题**：拍卖博弈（如在线广告、房地产）中求解贝叶斯纳什均衡（BNE）的计算复杂度高，且现有方法针对特定拍卖设定（固定机制、固定竞拍人数）设计，缺乏泛化性，需要大量重训练。
- **背景**：传统方法包括专用数值求解器、无遗憾学习算法（如MWU）和多智能体强化学习，但在处理多种机制、竞拍人数变化、不对称价值分布时效率低下，难以统一求解。
- **整体含义**：提出一个统一的深度学习框架Auctionformer，旨在无需重训练即可高效求解多种拍卖博弈的近似均衡策略，降低计算资源需求，提升泛化能力。

## 2. 方法论
- **核心思想**：利用Transformer架构处理序列化输入，将拍卖博弈（机制、竞拍者价值分布）通过灵活的词元化（tokenization）转换为标准令牌序列，由预训练语言模型（如BERT）编码，再通过注意力解码器输出每个竞拍者的出价策略。
- **关键技术细节**：
  - **词元化机制**：拍卖机制标识符及配置（如入场费）映射为令牌；竞拍者价值分布以离散概率直方图形式表示，并嵌入为向量。
  - **编码器**：使用预训练Transformer（BERT、GPT2、LLaMA2等）生成联合出价策略表示。
  - **策略解码器**：基于注意力机制，通过“值查询”向量与编码器输出的键/值对进行交叉注意力，确保价值实现在解码过程中不泄露（保持隐私），最后通过MLP输出离散出价概率。
  - **损失函数**：使用**Nash误差**（即最大可剥削性）代替传统MSE/CE损失。无需真实均衡解，可通过封闭形式高效计算（Proposition 3.3证明了在一价、二价拍卖中最大值可解析计算）。
  - **少样本学习（Few-shot）**：针对新机制，保留预训练模型在旧数据上的性能（preservation loss），同时在新机制少量样本上优化Nash误差，防止灾难性遗忘。
- **算法流程**（文字描述）：
  1. 输入：机制标识符及配置、所有竞拍者的价值分布。
  2. 词元化并嵌入，送入预训练Transformer编码器得到联合表示。
  3. 对每个竞拍者，结合其值查询（当前价值）与联合表示，通过交叉注意力解码器计算其出价分布。
  4. 输出：每个竞拍者每个可能价值的出价概率向量。
  5. 训练：根据预测策略计算Nash误差，反向传播更新模型参数。

## 3. 实验设计
- **数据集/场景**：
  - 四种标准机制：一价拍卖（FP）、二价拍卖（SP）、带入场费的一价拍卖（FP+Ent）、带入场费的二价拍卖（SP+Ent）。
  - 价值分布：均匀分布（U）和高斯分布（G）；分为起始为0（U0、G0）和起始非零（U-0、G-0）两类。
  - 竞拍人数：训练集2–10人，测试集包含0-shot（11–15人）和few-shot（15、20人）场景。
  - 训练样本：每种分布随机生成100,000个游戏实例，验证集500个，测试集额外2000个。
- **Benchmark与对比方法**：
  - 无遗憾学习：MWU算法（100,000迭代）。
  - 基于MLP的求解器：MLPNet（固定3人一价拍卖）。
  - 其他学习型算法：NPGA、SODA、SM（从文献中引用结果）。
  - 随机策略作为基线。
- **评估指标**：Nash误差（最大可剥削性）或L2距离（在有理论解时）。

## 4. 资源与算力
- 文中明确说明：实验使用Intel Xeon Platinum 8163 CPU @ 2.50GHz 或 **单张Nvidia Tesla V100-SXM2 16GB GPU**。
- 训练：300个epoch，批量大小1024，学习率1e-4，每50个epoch减半。
- 未说明总的训练时间，但推理时间在GPU上约0.006秒/样本，CPU上约0.03秒/样本（图5）。

## 5. 实验数量与充分性
- **实验数量**：
  - 主表（Table 2）：涵盖4种机制 × 5种分布类型 × 3组人数范围（2–4, 5–7, 8–10），共60个子场景。
  - 小样本学习（Table 3）：在人数15和20上测试，包括直接预训练、仅Nash损失、保真+损失三种设置。
  - 消融实验：
    - 不同语言模型规模对比（BERT-small, BERT, BERT-large, GPT2, LLaMA2-7B）与训练epoch（图6）。
    - 运行时间随竞拍人数的变化（图5）。
    - 固定BERT参数训练的效果（Appendix F.3）。
    - MLPNet对比（Appendix F.2）。
    - 零样本对称案例（Appendix F.5）。
    - 机制迁移的少样本学习（Appendix F.6）。
- **充分性评价**：
  - 实验覆盖了多机制、多分布、多人数、零样本、少样本、消融、对比等，较为全面。
  - 对比方法包括主流无遗憾学习和学习型求解器，且复现了公平的离散化条件。
  - 消融实验验证了Nash损失、预训练LM、注意力架构等组件的有效性。
- **客观性评价**：实验设计合理，对比方法在同类文献中被广泛使用，但部分对比结果（如与NPGA、SODA）直接引用原论文数据而非复现，可能存在实现细节差异；不过作者在Table 5中给出了L2距离和时间对比，解释较清晰。

## 6. 主要结论与发现
- Auctionformer能在一个统一框架内高效求解多种拍卖博弈的近似均衡，Nash误差普遍在1e-4量级，远低于随机策略（1.59e-1）。
- 对比无遗憾学习（MWU），Auctionformer显著缩短推理时间（0.006s vs 20–30s），且能处理MWU零值附近效果差的问题。
- 少样本学习可有效迁移到新机制或竞拍人数场景，保持原有域性能（保留损失）。
- 语言模型规模越大，收敛所需epoch越少（LLaMA2-7B仅需约19个epoch达到收敛），证明大规模预训练模型在博弈求解中的潜力。
- 运行时间几乎不受竞拍人数影响，具有良好的可扩展性。

## 7. 优点
- **统一性**：首次提出可同时处理多种机制、多种竞拍人数、不对称价值分布的深度学习求解器，显著降低工程成本。
- **无需真实标签**：使用Nash误差作为损失，避免收集或计算均衡解，训练数据仅需游戏参数。
- **框架灵活**：采用预训练Transformer骨干，可轻易扩展至更大模型或新机制（通过少样本）。
- **隐私保护**：解码器设计确保每个竞拍者的价值实现在计算中不泄露给他人。
- **推理高效**：单次前向传播即可输出所有竞拍者的策略，实时性强。

## 8. 不足与局限
- **实验覆盖有限**：仅验证了四种基本拍卖机制，未涉及更复杂机制（如组合拍卖、多物品拍卖、保留价）。
- **离散化近似**：价值和出价空间需离散化（H=20），定理3.2说明近似误差为O(1/H)，但高精度场景可能需要更细网格，增加计算量。
- **与SOTA对比不充分**：部分对比结果（如NPGA、SM）直接引用原文献数字，未在统一软硬件环境下复现，可能引入偏差。
- **计算资源**：训练完整Auctionformer（含BERT所有参数）需要GPU（单V100），对于资源受限团队可能门槛较高；但消融实验显示固定BERT也可达到较好效果。
- **零样本泛化能力弱**：在竞拍人数远超出训练范围（如15人）时，零样本性能显著下降（Nash误差达5.67e-2），需要少样本微调才能恢复。
- **实际应用风险**：拍卖博弈中均衡的唯一性和存在性假设较强，模型输出的近似均衡在真实现场中可能被对手利用，存在博弈风险。

（完）
