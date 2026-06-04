---
title: "Learning to Stop: Deep Learning for Mean Field Optimal Stopping"
title_zh: 学会停止：均值场最优停止的深度学习方法
authors: "Lorenzo Magnino, Yuchen Zhu, Mathieu Lauriere"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=LJvtuXhcIs"
tags: ["query:ai-finance"]
score: 8.0
evidence: 深度学习方法解决金融中的最优停止问题
tldr: 针对多智能体最优停止问题，提出均值场近似框架，并设计两类深度学习方法求解。理论证明了动态规划原理，实验验证了方法的有效性。该工作为金融风险管理中的最优决策提供了可扩展的深度解决方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 614, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 686, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1112, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1257, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1417, \"height\": 331, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 870, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1639, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1393, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 855, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 856, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 843, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 844, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 858, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 855, \"height\": 537, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 841, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 840, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 892, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1701, \"height\": 767, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1738, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1068, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1605, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1792, \"height\": 1641, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1790, \"height\": 2070, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1791, \"height\": 1640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1755, \"height\": 2173, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1784, \"height\": 2031, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1784, \"height\": 2029, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1753, \"height\": 1975, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1754, \"height\": 1976, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 975, \"height\": 2261, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ljvtuxhcis/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 974, \"height\": 2262, \"label\": \"Figure\"}]"
motivation: 最优停止在金融风险管理中重要，但多智能体环境计算复杂。
method: 构建均值场最优停止问题，推导动态规划原理，提出两类深度学习方法。
result: 理论证明均值场近似有效，实验表明深度方法能高效求解。
conclusion: 为多智能体最优停止提供可扩展的深度方案，促进金融应用。
---

## Abstract
Optimal stopping is a fundamental problem in optimization with applications in risk management, finance, robotics, and machine learning. We extend the standard framework to a multi-agent setting, named multi-agent optimal stopping (MAOS), where agents cooperate to make optimal stopping decisions in a finite-space, discrete-time environment. Since solving MAOS becomes computationally prohibitive as the number of agents is very large, we study the mean-field optimal stopping (MFOS) problem, obtained as the number of agents tends to infinity. We establish that MFOS provides a good approximation to MAOS and prove a dynamic programming principle (DPP) based on mean-field control theory. We then propose two deep learning approaches: one that learns optimal stopping decisions by simulating full trajectories and another that leverages the DPP to compute the value function and to learn the optimal stopping rule using backward induction. Both methods train neural networks to approximate optimal stopping policies. We demonstrate the effectiveness and the scalability of our work through numerical experiments on 6 different problems in spatial dimension up to 300. To the best of our knowledge, this is the first work to formalize and computationally solve MFOS in discrete time and finite space, opening new directions for scalable MAOS methods. Code is available at https://github.com/yuchen-zhu-zyc/Learning-to-Stop

---

## 论文详细总结（自动生成）

### 论文详细中文总结

#### 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：最优停止（Optimal Stopping）是优化中的基础问题，广泛应用于风险管理、金融、机器人等领域。当系统涉及多个相互作用的智能体时（多智能体最优停止，MAOS），随着智能体数量增加，求解变得计算上不可行。现有单智能体方法无法直接处理智能体间的分布依赖。
- **核心问题**：如何高效求解大规模多智能体最优停止问题，并保证近似最优性。
- **整体含义**：本文首次在离散时间、有限状态空间下形式化并数值求解均值场最优停止（MFOS）问题，为大规模MAOS问题提供可扩展的深度学习方法，并建立理论近似保证。

#### 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：通过均值场近似，将N个智能体的MAOS问题转化为代表性智能体的MFOS问题，利用智能体数量趋于无穷时的“传播混沌”（propagation of chaos）性质，使问题简化。
- **关键技术细节**：
  - **模型定义**：每个智能体状态为 \(X_n\)，决策为停止概率 \(p_n(x)\)（随机停止）。引入扩展状态 \(Y_n = (X_n, A_n)\)，其中 \(A_n\) 表示是否“存活”（未停止），以保证马尔可夫性。
  - **动态规划原理（DPP）**：证明值函数满足递归关系：
    \[
    V_n(\nu) = \inf_{h \in H} \left[ \sum_{(x,a)\in S} \nu(x,a)\Phi(x,\nu^X)a h(x) + V_{n+1}(\bar{F}(\nu, h)) \right]
    \]
    其中 \(\bar{F}\) 是均值场动态算子。
  - **理论近似保证**：证明MFOS的最优策略应用于N智能体问题的最优性差距为 \(O(1/\sqrt{N})\)（定理3.2），并给出显式边界。
- **算法流程**：
  - **直接方法（DA，算法2）**：学习一个时间相关的神经网络 \( \psi_\theta(n, x, \nu) \) 直接输出停止概率，通过模拟完整轨迹并最小化总成本 \(J(p)\)。
  - **动态规划方法（DP，算法1）**：从最后时刻 \(T\) 反向递推，对每个时间步 \(n\) 学习一个神经网络 \( \psi_n^\theta(x, \nu) \)，通过单步优化求解DPP递归。

#### 3. 实验设计：数据集/场景、基准、对比方法
- **场景**：6个不同复杂度的环境：
  1. `Towards the Uniform`（1D网格，确定性移动，局部成本）
  2. `Rolling a Die`（1D，随机均匀噪声，线性成本）
  3. `Crowd Motion with Congestion`（1D，随机移动+拥堵因子）
  4. `Distributional Cost`（1D，目标分布匹配成本）
  5. `Towards Uniform in 2D`（5×5网格，确定性移动）
  6. `Matching a Target with a Fleet of Drones`（10×10网格，常见噪声+终端成本）
- **基准**：对于简单场景（如Example 1、2），计算了解析最优值作为比较基准；对于更复杂场景，比较了异步停止（asynchronous）与同步停止（synchronous）两类策略。
- **对比方法**：文中主要对比了DA和DP两种方法本身的性能（训练损失、测试损失），并与理论最优值比较。未与其他现有方法对比（因为是首个求解MFOS的工作）。

#### 4. 资源与算力
- **硬件**：实验在单块 **NVIDIA RTX 4090 GPU** 和一台 **MacBook Pro with M2 Chip** 上运行。
- **时间**：每个单独的实验运行时间最多 **3分钟（GPU）** 或 **7分钟（CPU）**。
- **说明**：论文明确给出了硬件和运行时间的细节，但未提及多卡或分布式训练，也未给出总GPU小时数。

#### 5. 实验数量与充分性
- **实验数量**：6个不同场景，每个场景均使用DA和DP两种方法（以及异步/同步停止）进行训练和测试，共产生大量结果图（约30+子图）。此外，还对学习率进行了消融扫描（附录F）。
- **充分性**：
  - **充分**：覆盖了从一维到二维、确定性到随机、无交互到有交互（拥堵、常见噪声）的多种设定，验证了方法的可扩展性（直至300维输入）。
  - **客观公平**：对于有解析解的场景，均与最优值比较；对于无解析解的场景，通过可视化分布演化展示合理性。不同方法在同一设定下公平比较。
  - **缺憾**：未提供与现有单智能体或多智能体方法的直接对比（因无现有MFOS求解器），但已充分证明自身有效性。

#### 6. 论文的主要结论与发现
- **理论结论**：MFOS问题满足动态规划原理（定理4.1），且其最优解能以 \(O(1/\sqrt{N})\) 的速率近似有限N智能体问题的最优解（定理3.2）。
- **算法结论**：
  - DA方法在计算量不受限时收敛更快，但需要储存整个轨迹，内存随 \(T\) 增大而增加。
  - DP方法内存恒定（独立于 \(T\)），适合长时域问题，但每步需要单独训练。
  - 异步停止通常优于同步停止，尤其当智能体需要差异化决策时（如Example 2、3）。
- **实验结论**：两种方法均能在6个场景中成功学习到有效的停止策略，分布演变符合预期，且能泛化到不同初始分布（如Example 6的字母匹配任务）。

#### 7. 优点
- **理论贡献**：首次在离散时间、有限状态空间下建立MFOS的DPP，并给出有限智能体近似误差的显式 \(O(1/\sqrt{N})\) 上界。
- **方法创新**：将MFOS转化为均值场控制问题，从而利用成熟的马尔可夫决策过程（MDP）框架；提出两种互补的深度学习方法。
- **实践优势**：算法可扩展到高达300维的输入（10×10网格），且训练时间仅需数分钟；DP方法内存高效。
- **实验设计的全面性**：覆盖多种动态和成本类型，并包含同步/异步停止对比、学习率消融、泛化能力测试等，充分展示鲁棒性。

#### 8. 不足与局限
- **收敛证明缺失**：论文未提供所提深度算法的收敛性分析（由于深层网络的复杂性）。
- **停止类别未深入分析**：文中提到了异步和同步两类停止时间，但未详细探究不同类别的理论性质或更一般化的类别。
- **连续空间扩展**：方法和理论仅限于离散状态空间，向连续空间的扩展留作未来工作。
- **实际应用验证**：虽以无人机编队为例，但均为仿真环境，未在真实机器人或金融系统上验证。
- **对比局限**：由于是首次工作，缺乏与其他基准方法的定量对比（如单智能体方法扩展到多智能体的简单基线），可能影响对绝对性能的判断。

（完）
