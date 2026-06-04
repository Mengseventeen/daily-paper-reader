---
title: "FIC-TSC: Learning Time Series Classification with Fisher Information Constraint"
title_zh: FIC-TSC：基于Fisher信息约束的时间序列分类
authors: "Xiwen Chen, Wenhui Zhu, Peijie Qiu, Hao Wang, Huayu Li, ZIHAN LI, Yalin Wang, Aristeidis Sotiras, Abolfazl Razi"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Dr8msCnFYw"
tags: ["query:ai-finance"]
score: 8.0
evidence: 时间序列分类用于股票市场阶段分割
tldr: 针对时间序列分类中的域偏移问题，提出基于Fisher信息约束的FIC-TSC方法。该方法在股票市场阶段分割、客户行为预测等金融相关任务上表现出色，有效提升了跨域分类的鲁棒性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 831, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1760, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 841, \"height\": 293, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 776, \"height\": 344, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 812, \"height\": 712, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 815, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 818, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 817, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 844, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dr8mscnfyw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1236, \"height\": 621, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 869, \"height\": 189, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1777, \"height\": 756, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1771, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 787, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 444, \"height\": 173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 618, \"height\": 574, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 868, \"height\": 543, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1074, \"height\": 1044, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 541, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 552, \"height\": 152, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 551, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1783, \"height\": 1095, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dr8mscnfyw/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1312, \"height\": 2028, \"label\": \"Table\"}]"
motivation: 时间序列分类面临训练和测试集域偏移问题，导致金融领域（如股票阶段分类）性能下降。
method: 在分类损失中加入Fisher信息约束，正则化特征表示以减轻域偏移。
result: 在包括股票数据集在内的多个基准上，FIC-TSC分类准确率显著高于现有域自适应方法。
conclusion: Fisher信息约束为时间序列分类提供了一种有效的域泛化手段，尤其适用于金融场景。
---

## Abstract
Analyzing time series data is crucial to a wide spectrum of applications, including economics, online marketplaces, and human healthcare. In particular, time series classification plays an indispensable role in segmenting different phases in stock markets, predicting customer behavior, and classifying worker actions and engagement levels. These aspects contribute significantly to the advancement of automated decision-making and system optimization in real-world applications. However, there is a large consensus that time series data often suffers from domain shifts between training and test sets, which dramatically degrades the classification performance. Despite the success of (reversible) instance normalization in handling the domain shifts for time series regression tasks, its performance in classification is unsatisfactory. In this paper, we propose $\textit{FIC-TSC}$, a training framework for time series classification that leverages Fisher information as the constraint. We theoretically and empirically show this is an efficient and effective solution to guide the model converges toward flatter minima, which enhances its generalizability to distribution shifts. We rigorously evaluate our method on 30 UEA multivariate and 85 UCR univariate datasets. Our empirical results demonstrate the superiority of the proposed method over 14 recent state-of-the-art methods.

---

## 论文详细总结（自动生成）

# FIC-TSC：基于 Fisher 信息约束的时间序列分类学习

## 1. 核心问题与整体含义

时间序列分类（TSC）在经济学、在线市场、医疗健康等领域具有广泛应用，例如股票市场阶段划分、客户行为预测、工人行为分类等。然而，时间序列数据普遍存在**训练集与测试集之间的域偏移（domain shift）** 问题（如传感器差异、环境变化、采集时间不同等），导致分类性能严重下降。现有方法如可逆实例归一化（RevIN）在回归任务中有效，但在分类任务中效果不佳，甚至会降低类间差异，抑制性能。该论文聚焦于解决 TSC 中的域偏移问题，提出一种基于 Fisher 信息约束的训练框架 FIC-TSC，旨在引导模型收敛到更平坦的极小值，从而增强对分布偏移的泛化能力。

## 2. 方法论

### 核心思想
利用 **Fisher 信息矩阵（FIM）** 作为优化约束。Fisher 信息衡量模型参数对数据微小变化的敏感程度；约束 Fisher 信息的大小可以促使模型收敛到平坦的极小值（flat minima），从而提升泛化性。

### 关键技术细节
- **Fisher 信息矩阵（FIM）定义**：对于参数 Θ 和数据 D，FIM 为 \( F(\Theta) = E_{p(D|\Theta)}[(\nabla_\Theta \log p(D|\Theta))(\nabla_\Theta \log p(D|\Theta))^\top] \)。在分类任务中，log-likelihood 对应负交叉熵损失。
- **对角近似**：为降低计算复杂度（全 FIM 为 O(n²)），采用对角近似，仅保留对角线元素，复杂度降为 O(n)。实际估计为 `diag(F(Θ)) = ∇L(Θ) ⊙ ∇L(Θ)`。
- **梯度重归一化**：计算 FIM 的 1-范数 `∥F∥₁`，若其超过预设上界 ϵ，则按比例缩放梯度：`∇L(Θ) ← sqrt(ϵ / ∥F∥₁) · ∇L(Θ)`。
- **优化问题**：`min_Θ L(D; Θ)  s.t.  ∥F(Θ)∥₁ ≤ ϵ`。该约束仅需一次反向传播，无需二次计算。
- **理论支持**：
  - 在局部最小值处，Hessian 矩阵与 FIM 渐近等价（Lemma 1）。
  - 利用泰勒展开，α-sharpness 的上界与 FIM 的 1-范数成正比（Corollary 1），因此约束 FIM 可降低 sharpness，促进平坦极小值（Proposition 1）。
  - 在 L-Lipschitz 条件下，选择合适的学习率和 ϵ，梯度下降收敛率为 O(1/T)（Theorem 4），与标准训练一致。

### 算法流程（文字描述）
1. 初始化网络参数 Θ。
2. 对于每次迭代，采样小批量数据，前向传播计算损失。
3. 反向传播得到梯度 ∇L。
4. 计算 FIM 的对角近似及其 1-范数。
5. 若该范数 ≥ ϵ，则缩放梯度（乘以 sqrt(ϵ/∥F∥₁)）。
6. 使用优化器（如 AdamW）更新参数。

## 3. 实验设计

### 数据集与场景
- **多元时间序列分类**：30 个 UEA 数据集（涵盖人行为识别、医疗、交通等，长度 2~1345，维度数 2~39，训练/测试样本数 15~30000）。
- **单变量时间序列分类**：85 个 UCR 数据集（长度 16~12709，类别数 2~60，训练/测试样本数 16~8926）。
- **医疗显式域偏移场景**：4 个医疗数据集（TDBrain、ADFTD、PTB-XL、SleepEDF），按患者划分，存在显式域偏移。

### Benchmark 与对比方法
- 对比 14 种 SOTA 方法，包括表示学习类（TsLaNet、GPT4TS、TimesNet、PatchTST、Crossformer、TS-TCC），分类专用类（ROCKET、InceptionTime、ConvTran、MILLET、TodyNet、HC2、Hydra-MR），以及简单线性模型。
- 消融实验：与基线（InceptionTime 标准训练）对比，与 RevIN 对比，与 SAM（Sharpness-Aware Minimization）对比。
- 案例研究：在 TimesNet 和 PatchTST 上应用 FIC 约束验证可迁移性。

## 4. 资源与算力

论文中未明确说明具体使用的 GPU 数量、训练时长或总计算量。仅提及实验在 NVIDIA A100（40GB）集群节点上实现，使用 PyTorch 1.13。未提供各数据集训练时间或总 GPU 小时数。

## 5. 实验数量与充分性

- **核心实验**：在 30 个 UEA 和 85 个 UCR 数据集上对比准确率，共涵盖 115 个数据集，实验规模大。
- **消融实验**：在 10 个代表性数据集上测试了不同超参数（ϵ ∈ {2,4,10,20}）和不同约束强度。
- **其他分析**：
  - 与 RevIN 对比（10 个数据集）。
  - 与 SAM 对比（10 个数据集，对比准确率和运行时间）。
  - 在 TimesNet 和 PatchTST 上的迁移实验（10 个数据集）。
  - 医疗显式域偏移实验（4 个数据集）。
  - 锐度（sharpness）降低量可视化（10 个数据集）。
  - 损失景观可视化（10 个数据集中选一个）。
- **统计检验**：使用 Wilcoxon 符号秩检验验证 FIC 与基线、与 SAM 的差异显著性（p 值均 <0.05）。
- **充分性**：实验范围广泛，覆盖多变量/单变量、通用分类和医疗专用场景，消融和对比充分。但未涉及跨领域（如工业、金融）的显式偏移测试，且仅使用单一骨干网络（InceptionTime）进行主要实验。

## 6. 主要结论与发现

1. **RevIN 在 TSC 中无效**：实例归一化降低类间差异，反而损害分类性能（平均准确率下降）。
2. **FIC-TSC 显著提升性能**：在 UEA 上平均准确率 76.9%（通用超参数），优于第二名 MILLET（74.8%）；在 UCR 上平均准确率 86.2%，优于 HC2（86.0%）。全超参数微调后分别达到 79.6% 和 87.3%。
3. **造成平坦极小值**：FIC 约束可将锐度降低约 40%（10 个数据集平均），损失景观更平坦，有利于泛化。
4. **计算效率优于 SAM**：相同 batch size 下，FIC 平均准确率 76.8% vs SAM 74.2%，且运行时间减半（0.070s vs 0.158s/iter）。
5. **可迁移性**：在 TimesNet 和 PatchTST 上应用均获得约 4% 的准确率提升。
6. **医疗显式域偏移场景有效**：在 4 个医疗数据集上均优于基线，且多数超过 Medformer SOTA。

## 7. 优点

- **理论扎实**：从 Fisher 信息与 Hessian 的关系出发，建立与 sharpness 的数学联系，并给出收敛性保证。
- **计算高效**：仅需一次反向传播，对角近似和梯度缩放开销极小，实际运行时间仅为 SAM 的一半。
- **超参数鲁棒**：通用超参数（ϵ=2, batch=64/16）已能超过多数 SOTA，说明方法对超参数不敏感。
- **广泛的实验验证**：在 115 个数据集、14 个对比方法上进行全面评估，涵盖多变量/单变量及医疗显式偏移场景。
- **可迁移性强**：可作为插件应用于不同骨干网络（InceptionTime、TimesNet、PatchTST）并一致提升性能。

## 8. 不足与局限

- **理论假设局限**：sharpness 与泛化性之间的关系仍有争议（论文参考文献中已有批评），论文仅声称潜在影响，未提供严格因果证明。非极小值处的分析缺失。
- **实验覆盖**：主要骨干为 InceptionTime，缺乏对其他架构（如 Transformer 原生）的广泛测试（虽有两例案例研究）。医疗场景数据集数量有限（仅 4 个），且未在其他域（如金融、工业）的显式偏移下验证。
- **对角近似精度**：仅使用 FIM 对角线元素可能丢失相关性信息，论文未评估近似误差对最终性能的影响。
- **超参数ϵ依赖**：虽然通用超参数有效，但全超参数微调仍带来 2~3% 的提升，提示不同数据集最佳值可能不同，需要用户自行搜索。
- **缺乏与其他域适应方法的直接对比**：论文指出 FIC 与域适应方法正交，但未实验对比如 DANN、CORAL 等经典域适应方法在相同场景下的性能。

（完）
