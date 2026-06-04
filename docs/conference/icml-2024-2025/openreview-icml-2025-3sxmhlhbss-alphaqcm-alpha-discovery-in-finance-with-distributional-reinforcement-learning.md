---
title: "AlphaQCM: Alpha Discovery in Finance with Distributional Reinforcement Learning"
title_zh: "AlphaQCM: 使用分布式强化学习进行金融Alpha发现"
authors: "Zhoufan Zhu, Ke Zhu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=3sXMHlhBSs"
tags: ["query:ai-finance"]
score: 10.0
evidence: 使用深度强化学习进行alpha发现
tldr: 针对金融中寻找协同公式化Alpha的挑战，将Alpha发现建模为非平稳、稀疏奖励的序贯决策问题，提出AlphaQCM方法，通过分位数网络学习Q函数和分位数，高效搜索Alpha，实验验证其有效性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-3sxmhlhbss/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 854, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3sxmhlhbss/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 861, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3sxmhlhbss/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1730, \"height\": 531, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 851, \"height\": 1061, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 539, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 872, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 704, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 807, \"height\": 523, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1801, \"height\": 1144, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1149, \"height\": 878, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1177, \"height\": 477, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1113, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3sxmhlhbss/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1194, \"height\": 560, \"label\": \"Table\"}]"
motivation: 金融中寻找协同公式化Alpha非常关键但具有挑战性。
method: 将Alpha发现建模为马尔可夫决策过程，提出基于分位数网络的分布式强化学习方法AlphaQCM。
result: AlphaQCM能够高效搜索到协同Alpha，验证了方法的有效性。
conclusion: 为金融Alpha发现提供了新的强化学习视角和高效算法。
---

## Abstract
For researchers and practitioners in finance, finding synergistic formulaic alphas is very important but challenging. In this paper, we reconsider the discovery of synergistic formulaic alphas from the viewpoint of sequential decision-making, and conceptualize the entire alpha discovery process as a non-stationary and reward-sparse Markov decision process. To overcome the challenges of non-stationarity and reward-sparsity, we propose the AlphaQCM method, a novel distributional reinforcement learning method designed to search for synergistic formulaic alphas efficiently. The AlphaQCM method first learns the Q function and quantiles via a Q network and a quantile network, respectively. Then, the AlphaQCM method applies the quantiled conditional moment method to learn unbiased variance from the potentially biased quantiles. Guided by the learned Q function and variance, the AlphaQCM method navigates the non-stationarity and reward-sparsity to explore the vast search space of formulaic alphas with high efficacy. Empirical applications to real-world datasets demonstrate that our AlphaQCM method significantly outperforms its competitors, particularly when dealing with large datasets comprising numerous stocks.

---

## 论文详细总结（自动生成）

以下是基于论文《AlphaQCM: Alpha Discovery in Finance with Distributional Reinforcement Learning》的详细中文总结。

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：在量化金融中，寻找一组具有协同效应的**公式化Alpha**（可解释的数学表达式）对于预测股票收益至关重要。然而，传统遗传编程（GP）方法搜索空间呈指数增长，且现有强化学习方法（如AlphaGen）忽视了马尔可夫决策过程（MDP）中存在的**非平稳性**（reward函数随发现的新Alpha动态变化）和**奖励稀疏性**（绝大多数生成表达式无效或贡献微小），导致探索效率低、训练不稳定。

- **整体含义**：本文首次从**序列决策**视角重新审视Alpha发现，将其建模为一个**非平稳、奖励稀疏的MDP**，并提出一种新颖的**分布强化学习（Distributional RL）方法——AlphaQCM**，以有效应对这两大挑战，从而高效搜索协同公式化Alpha。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用分布强化学习学习累积折扣奖励的完整分布（特别是分位数），然后借助**分位数条件矩（Quantiled Conditional Moments, QCM）方法**从**可能有偏**的分位数估计中**无偏地**估计方差。该方差作为自然的探索奖励（exploration bonus），引导智能体优先探索不确定性高的状态-动作对，从而缓解非平稳性和奖励稀疏性问题。

- **关键技术细节**：
  1. **MDP构建**：状态为当前生成的令牌序列（基于RPN表示），动作为选择下一个令牌（算子/特征/常数），转移为确定性追加令牌，奖励由新Alpha对Alpha池的边际IC提升给出（详见算法1）。
  2. **分位数学习**：采用**IQN算法（Implicit Quantile Networks）**，输入状态和随机采样的分位水平τ，通过LSTM提取状态特征，输出各动作的分位数估计 \(\hat{\theta}_k(x,a)\)。
  3. **Q函数学习**：采用**DQN算法**估计期望Q值 \(\hat{Q}(x,a)\)。
  4. **方差估计**：对每个状态-动作对，利用Cornish-Fisher展开和QCM方法，从K个分位数估计中通过OLS回归得到方差估计 \(\hat{h}(x,a)\)，该估计在非平稳环境下仍保持一致。
  5. **动作选择**：使用探索策略 \(a_t = \arg\max_a \left[ \hat{Q}(x,a) + \lambda \sqrt{\hat{h}(x,a)} \right]\)，其中\(\lambda\)控制偏好程度。

- **算法流程文字说明**：
  - 初始化Q网络、分位数网络及对应的目标网络。
  - 在每个episode：智能体从BEG令牌开始，循环选择动作（令牌）直到结束，获得奖励。
  - 每次与环境交互后，将transition存入经验回放缓冲池（采用优先经验回放）。
  - 每步从缓冲池采样一个batch，分别更新Q网络（平方TD误差）和分位数网络（分位Huber损失）。
  - 定期同步目标网络。

### 3. 实验设计：数据集、场景、Benchmark与对比方法

- **数据集与场景**：
  - **主要实验**：中国A股三个股票池：CSI 300（大盘）、CSI 500（中盘）、全市场（Market）。预测未来20日收益率。
  - 时间分割：训练集2010-2019，验证集2020，测试集2021-2022。
  - **额外实验**：美国S&P 500（最大500只股票），用于验证跨市场泛化性。

- **Benchmark与对比方法**：
  - **人类设计公式化Alpha**：Alpha101（Kakushadze提出的101个因子）。
  - **机器学习非公式化Alpha**：MLP、XGBoost、LightGBM（基于Qlib实现）。
  - **遗传编程公式化Alpha**：GP w/o filter（无IC互相关筛选）、GP w/ filter（有筛选）。
  - **强化学习公式化Alpha**：PPO w/ filter、AlphaGen（最密切的RL baseline）。

- **评估指标**：信息系数（IC，即预测信号与未来收益的截面相关系数的时间均值）。

### 4. 资源与算力

- **文中未明确说明GPU型号、数量、具体训练时长**。
- 仅给出**总交互步数**：Alpha池大小P=10/20/50/100时分别对应250k、300k、350k、400k步。
- 网络参数：LSTM隐层128维，全连接头64维，分位网络含τ-embedding。
- 超参数列表详见附录E.3（学习率5e-5，batch size 128等）。

### 5. 实验数量与充分性

- **主要实验（表1）**：在3个中国数据集上，每个方法使用10个不同随机种子，报告均值与标准差。
- **消融实验（表2）**：探究不同方差估计（无方差、Vanilla方差、QCM方差）和不同DRL骨干（QRDQN vs IQN），共3×2=6种组合，各10种子。
- **领域知识影响（表3）**：对比使用/不使用专家预填充回放，分4个训练阶段，各10种子。
- **跨市场泛化（表4）**：CSI 500 vs S&P 500，各10种子。
- **附加消融（附录G）**：参数规模（小/大）、模型架构（LSTM vs MAMBA）、扩展测试集（至2024年末）等。
- **充分性评价**：实验设计较全面，覆盖多种对比方法、不同数据规模、消融关键组件、随机种子重复实验，统计结果客观。不足之处在于缺少更大规模（如美股全市场）或不同回测周期（如更长持有期）的验证。

### 6. 论文的主要结论与发现

- **AlphaQCM在全部三个中国数据集上取得了最高的测试IC**（8.49%、9.55%、9.16%），显著优于所有baseline，且优势随着股票数量增加（系统复杂性升高）而增大。
- 使用**QCM方差作为探索奖励**比不使用方差或使用朴素量化方差效果更好，且IQN骨干略优于QRDQN。
- 引入专家知识（领域知识）可加速初期学习，但**最终性能反而不如纯数据驱动方式**，可能是由于过早陷入局部最优。
- 在美国S&P 500数据集上，AlphaQCM同样优于所有对比方法，但所有方法的IC值均低于A股，表明美国市场更有效、更难捕捉。
- 扩展测试集至2024年12月后，优势依然保持，但所有方法IC下降，提示需要持续重新训练。

### 7. 优点

- **方法创新性强**：首次将分布RL与QCM方差估计结合，针对性地解决非平稳性与奖励稀疏性，具有通用性。
- **理论保障**：QCM方法在非平稳环境下仍能获得无偏方差估计（Proposition 3.1）。
- **实验全面**：多数据集、多对比方法、多随机种子、多角度消融，结果可靠。
- **实现透明**：开源自代码与数据，可重复。

### 8. 不足与局限

- **计算资源未披露**：缺乏GPU型号、训练时长、能耗等信息，不利于能耗对比和复现。
- **市场局限性**：仅测试了A股和S&P 500，未涉及其他新兴市场或期货、加密货币等。
- **时间跨度有限**：测试集仅涵盖2年（2021-2022），且扩展后IC下降，表明模型可能对市场状态变化敏感，未进行滚动更新实验。
- **参数规模控制**：虽然做了参数规模实验，但未评估更大批量化或并行探索对性能的影响。
- **奖励设计单一**：依赖线性模型和IC，未探索其他更复杂的收益/风险惩罚机制。
- **可解释性**：虽说是“公式化Alpha”，但通过RL搜索出的表达式可能仍较复杂，实际可解释性受限。

（完）
