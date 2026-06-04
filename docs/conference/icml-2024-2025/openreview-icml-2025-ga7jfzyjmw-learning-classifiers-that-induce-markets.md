---
title: Learning Classifiers That Induce Markets
title_zh: 学习诱导市场的分类器
authors: "Yonatan Sommer, Ivri Hikri, Lotan Amit, Nir Rosenfeld"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=GA7JfZyJMw"
tags: ["query:ai-finance"]
score: 6.0
evidence: 面向贷款决策的竞争性分类，市场驱动特征成本
tldr: 该论文挑战机器学习部署中成本外生的假设，提出分类器可以诱导特征市场。在贷款等金融决策场景中，用户为提高预测结果会购买重要特征，从而形成市场。论文扩展了竞争分类框架，实验表明方法对提供商和消费者都有利。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 777, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1745, \"height\": 259, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1769, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 867, \"height\": 600, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 862, \"height\": 423, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 865, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1256, \"height\": 1084, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 711, \"height\": 535, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 792, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 795, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 957, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1788, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 960, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1786, \"height\": 1103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 798, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ga7jfzyjmw/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 791, \"height\": 407, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ga7jfzyjmw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 851, \"height\": 592, \"label\": \"Table\"}]"
motivation: 传统战略分类假设成本固定，但实际中分类器部署会创造特征需求市场。
method: 扩展战略分类框架，将特征市场引入决策过程，提出学习竞争环境下最大化市场份额的分类方法。
result: 新方法在模拟贷款等场景中使提供商和消费者双赢。
conclusion: 揭示了分类器部署的市场效应，为金融等领域的战略分类提供了新视角。
---

## Abstract
When learning is used to inform decisions about humans, such as for loans, hiring, or admissions, this can incentivize users to strategically modify their features, at a cost, to obtain positive predictions. The common assumption is that the function governing costs is exogenous, fixed, and predetermined. We challenge this assumption, and assert that costs emerge as a *result* of deploying a classifier. Our idea is simple: when users seek positive predictions, this creates demand for important features; and if features are available for purchase, then a market will form, and competition will give rise to prices. We extend the strategic classification framework to support this notion, and study learning in a setting where a classifier can induce a market for features. We present an analysis of the learning task, devise an algorithm for computing market prices, propose a differentiable learning framework, and conduct experiments to explore our novel setting and approach.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：在战略分类（strategic classification）中，传统假设用户修改特征的成本是外生、固定且预先确定的。论文质疑这一假设，指出成本实际上是分类器部署后**内生的**：当用户追求正面预测时，会对重要特征产生需求；如果特征可以购买，则会形成市场，竞争产生价格。因此，学习算法必须能够预测并适应它所诱导的市场。
- **整体含义**：该研究将战略分类框架扩展到市场驱动的场景，揭示了分类器选择不仅影响个体用户行为，还会通过市场机制影响整体的特征价格、用户移动模式和社会福利。这对于贷款审批、招聘、大学录取等涉及人类决策的领域具有重要启示。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：用户为获得正面预测而购买特征，每个特征由独立卖家定价（无限供应）。用户有预算约束，选择最经济有效的特征组合。卖家以最大化收入为目标设定价格，达到纳什均衡。分类器通过影响用户的需求分布进而影响均衡价格。
- **关键假设**：特征向量非负（x[i]≥0），用户只能购买不能出售（δ≥0）；使用线性成本函数 \(c_p(\delta) = \delta^\top p\)，p为价格向量。
- **均衡价格性质**：对于线性分类器 \(h(x)=\text{sign}(w^\top x + \tau)\)，均衡价格与权重向量成比例：\(p^* = \rho^* \cdot w\)，其中标量 \(\rho^*\) 由需求分布决定。这一简化使得计算价格转化为求解一维优化问题。
- **价格计算算法（ Empirical Market Prices）**：
  - 对每个负类用户，计算到决策边界的**单位距离** \(u = \text{dist}_+(x;h)\)。
  - 归一化得到 \(\bar{u} = u/b\)（b为用户预算）。
  - 按 \(\bar{u}\) 排序，遍历每个样本作为潜在的“价格设定者”，收入 \(r = \rho \cdot U\)，其中 \(U\) 是累计需求。最优价格是使收入最大的 \(\rho = 1/\bar{u}_{(i)}\)。
  - 时间复杂度 \(O(m \log m)\)。
- **可微分价格近似**：使用 soft sort 和 softmax 替换排序和 argmax，得到平滑价格 \(\tilde{\rho}\)，使整个目标可端到端优化。
- **市场铰链损失（Market Hinge Loss）**：基于用户个性化移动能力，提出 \( \ell_{\text{m-hinge}} = \max\{0, 1 - y(w^\top x + \tau + \frac{b}{\rho}\|w\|)\} \)，避免显式计算最佳响应。

## 3. 实验设计：数据集、场景、benchmark、对比方法

- **数据集**：
  - **合成数据**：用于探索市场基本力学（如Beta分布、高斯混合等）以及阈值、预算不平等程度的影响。
  - **真实数据**：
    - **Adult数据集**：取自1994年人口普查，二分类标签（收入是否>50k），使用 `capital_gain` 特征作为预算的代理，通过随机森林填补缺失值。
    - **Folktables数据集**：二分类标签为就业状态，预算使用总收入特征。
- **场景**：模拟不同预算不平等程度（\(b_{\max}/b_{\min} = 2^2\) 到 \(2^{10}\)），观察准确率、福利、社会负担等指标。
- **对比方法**：
  - **Naïve**：非战略分类器（忽略用户反应）。
  - **Strat (short)**：战略分类器，基于当前固定价格优化，但未考虑市场适应（短期表现）。
  - **Strat (long)**：上述分类器在实际市场再平衡后的长期表现。
  - **Benchmark**：Naïve在非战略数据上的准确率（作为上限参考）。
- **本文方法**：MASC（Market-Aware Strategic Classification），使用可微分市场铰链损失和端到端优化。

## 4. 资源与算力

- 论文**未明确说明**所使用的GPU型号、数量、训练时长等算力信息。仅提到使用PyTorch实现、Adam优化器、小批量训练等。因此无法给出具体算力消耗数据。

## 5. 实验数量与充分性

- **实验数量**：
  - 大量合成实验：多种Beta分布下的价格设定者百分位分析；阈值变化实验；预算相关性与交叉比例的实验；两类高斯混合的“簇假说”验证等。
  - 两个真实数据集（Adult、Folktables）上的主实验，每个实验包含10个随机数据划分，报告均值和标准误。
  - 消融/分析：不同预算不平等尺度下的准确率、交叉比例、福利、社会负担；以及短期vs长期性能对比。
- **充分性**：实验设计较为全面，覆盖了理论分析、合成数据和真实数据，对比基线合理。但仅限于线性分类器，未涉及非线性模型；仅考虑单一价格均衡机制，未探索多卖家竞争或容量限制等更复杂市场结构。

## 6. 主要结论与发现

- **市场导致复杂行为模式**：在固定成本下，用户移动仅取决于与决策边界的距离；而在市场成本下，移动决策依赖于整体需求分布，导致“提高门槛”反而可能使更多负类用户跨越。
- **市场可创造可分性**：当预算与标签相关时，市场定价能够使原本线性不可分的数据变得可分（例如使用无信息特征x2，但利用预算差异达到高准确率）。
- **高准确率要求预算不平等**：多数负类用户不被允许跨越需要预算极度不平等（Gini接近1）的状态；在均匀预算下几乎所有负类用户都会移动，导致准确率降至约50%。
- **MASC方法优于基线**：在Adult和Folktables数据集上，MASC在长期准确率上显著超过Naïve和Strat（尤其是大预算不平等尺度），且短期-长期差距较小。
- **预算不平等影响社会福利**：随着预算差距增大，福利（归一化后）先下降后部分恢复，社会负担在中等不平等时上升，但整体保持较低水平。

## 7. 优点

- **新颖的问题定义**：首次系统地将市场机制引入战略分类，挑战了成本外生的传统假设，具有理论创新性。
- **简洁的理论分析**：证明了均衡价格与分类器权重成比例，将多维价格优化简化为单变量优化，算法高效（O(m log m)）。
- **可微分的端到端学习框架**：通过soft sort和softmax实现平滑价格计算，使得学习过程可微分，并能与标准梯度优化结合。
- **丰富的实验验证**：既有理论分析（如价格设定者极端性），也有合成和真实数据实验，展示了市场行为的反直觉现象（如负相关预算下的可分性）。

## 8. 不足与局限

- **模型假设较强**：假设线性分类器、无限供应、每个卖家专营一种特征、无外部性、用户完全理性等，距离现实市场有差距。
- **实验覆盖不足**：仅使用线性模型，未探索非线性分类器（如神经网络）在市场情境下的表现；数据集仅两个，且都是美国公开数据集，领域有限。
- **偏差风险**：预算的构造（如用`capital_gain`代理预算）可能引入噪声；缺失值插值使用随机森林，但其准确性未详细报道。
- **可重复性细节缺失**：算力信息、超参数搜索细节、代码公开情况（论文提到代码在GitHub，但未在文中说明）。
- **消融实验不够深入**：虽然分析了预算不平等的效果，但未系统研究温度超参数（softsort、softmax）对平滑价格和最终性能的影响。

（完）
