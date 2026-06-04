---
title: "WATCH: Adaptive Monitoring for AI Deployments via Weighted-Conformal Martingales"
title_zh: WATCH：通过加权共形鞅实现AI部署的自适应监控
authors: "Drew Prinster, Xing Han, Anqi Liu, Suchi Saria"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=GMjkK2CKx5"
tags: ["query:ai-finance"]
score: 5.0
evidence: 基于共形鞅的自适应监控方法，适用于金融AI系统监控
tldr: 针对AI系统部署后持续监测需求，提出加权共形鞅非参数顺序检验方法，能在线自适应检测数据漂移和性能退化，突破传统假设限制，并诊断异常原因。该方法对金融等高可靠性场景的AI监控具有重要价值。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1740, \"height\": 691, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1775, \"height\": 999, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1795, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1761, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1587, \"height\": 1061, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1766, \"height\": 686, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1764, \"height\": 959, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1804, \"height\": 2089, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gmjkk2ckx5/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1850, \"height\": 939, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1762, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1796, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 907, \"height\": 253, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1555, \"height\": 1129, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1556, \"height\": 1251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1552, \"height\": 1173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gmjkk2ckx5/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1566, \"height\": 1134, \"label\": \"Table\"}]"
motivation: AI系统部署后需持续监测安全行为，现有方法缺乏自适应性和诊断能力。
method: 提出基于加权共形鞅的非参数顺序检验方法，支持在线适应性监测。
result: 方法可在多种漂移场景下及时告警并定位原因。
conclusion: 为AI安全监测提供自适应诊断工具，适用于金融等高风险领域。
---

## Abstract
Responsibly deploying artificial intelligence (AI) / machine learning (ML) systems in high-stakes settings arguably requires not only proof of system reliability, but also continual, post-deployment monitoring to quickly detect and address any unsafe behavior. Methods for nonparametric sequential testing---especially conformal test martingales (CTMs) and anytime-valid inference---offer promising tools for this monitoring task. However, existing approaches are restricted to monitoring limited hypothesis classes or ``alarm criteria'' (e.g., detecting data shifts that violate certain exchangeability or IID assumptions), do not allow for online adaptation in response to shifts, and/or cannot diagnose the cause of degradation or alarm. In this paper, we address these limitations by proposing a weighted generalization of conformal test martingales (WCTMs), which lay a theoretical foundation for online monitoring for any unexpected changepoints in the data distribution while controlling false-alarms. For practical applications, we propose specific WCTM algorithms that adapt online to mild covariate shifts (in the marginal input distribution), quickly detect harmful shifts, and diagnose those harmful shifts as concept shifts (in the conditional label distribution) or extreme (out-of-support) covariate shifts that cannot be easily adapted to. On real-world datasets, we demonstrate improved performance relative to state-of-the-art baselines.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：在高风险场景（如医疗、自动驾驶）中部署 AI/ML 系统，不仅需要初始可靠性验证，更需要在部署后持续监测，以便快速发现并应对不安全行为（如数据分布漂移、模型性能退化）。现有方法（如标准共形检验鞅 CTM）存在三大局限：只能监测有限假设类（如交换性/IID 假设），无法在线自适应响应漂移，以及不能诊断性能下降的根本原因（是协变量漂移还是概念漂移）。
- **核心问题**：如何设计一种监测方法，同时满足：① 对温和/良性漂移在线自适应以避免误报；② 快速检测有害漂移；③ 诊断漂移类型以指导恢复措施。
- **整体含义**：论文提出的 WATCH 框架通过加权共形检验鞅（WCTM）扩展了传统 CTM 的能力，为 AI 安全监测提供了理论扎实、实践有效的工具，尤其适用于金融、医疗等对可靠性要求极高的领域。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：
  - 将标准共形检验鞅（CTM）推广为**加权共形检验鞅（WCTM）**，允许使用**加权共形 p 值**替换标准共形 p 值，从而对更广义的零假设进行在线检验。
  - 通过**在线密度比估计**学习协变量漂移的权重函数 \( \hat{w}(x) \)，实现对温和漂移的自适应，同时保持对有害漂移（概念漂移或极端协变量漂移）的检测能力。
  - 结合**双鞅结构**（主 WCTM + 辅助 X-CTM）实现根因分析：若只有 X-CTM 触发警告，则诊断为协变量漂移；若 WCTM 触发但 X-CTM 无反应，则为概念漂移。

- **关键技术细节**：
  - **加权共形 p 值**：定义见公式 (9)，通过权重向量 \( \tilde{w} \) 对校准集和测试点的非一致性分数进行加权求和得到 p 值。
  - **零假设**：对抗协变量漂移假设 \( H_0^{(cs)} \)，假设条件标签分布 \( Y|X \) 不变，且密度比估计 \( \hat{w}(x) \) 准确。
  - **定理 3.1**：若零假设成立，在线加权共形 p 值序列独立同分布于均匀分布 \( U[0,1] \)。
  - **WCTM 构造**：将上述 p 值序列输入到赌博函数 \( h(p)=1+\epsilon(p-0.5) \) 中，通过复合跳跃策略累积财富得到鞅值 \( \tilde{M}_t \)。利用 Ville 不等式控制误报率（命题 3.2），并用 Shiyaev-Roberts 过程控制平均运行长度（命题 3.3）。
  - **自适应初始化**：辅助 X-CTM 用于自动检测何时启动自适应阶段（当 X 分布发生显著变化时）。自适应阶段使用在线训练的密度比分类器（MLP 或逻辑回归）更新权重。

- **算法流程（文字说明）**：
  1. 初始阶段：主 WCTM 使用均匀权重（即标准 CTM），辅助 X-CTM 监控输入 \( X \) 的漂移。
  2. 当 X-CTM 超过预设自适应阈值（如时间 \( t_{ad} \)），启动自适应模式：固定校准集（前 \( n+t_{ad}-1 \) 个点），对后续每个测试点用当前密度比估计计算加权 p 值。
  3. 主 WCTM 根据 p 值序列更新鞅值；若鞅值超过告警阈值，则触发告警。
  4. 同时比较主 WCTM 和 X-CTM 的行为进行根因分析。

### 3. 实验设计：数据集/场景、benchmark、对比方法

- **数据集**：
  - **表格数据（回归任务）**：MEPS（医疗支出，~33k 样本，107 特征）、Superconductivity（超导，~21k 样本，81 特征）、Bike Sharing（自行车共享，~17k 样本，12 特征）。
  - **图像数据（分类任务）**：MNIST-C 和 CIFAR-10-C（含多种损坏类型，如亮度、对比度、模糊、噪声等）。
- **场景**：
  - 良性协变量漂移（温和老化或采样偏倚，不影响覆盖性能）。
  - 有害概念漂移（\( Y|X \) 关系改变）。
  - 极端协变量漂移（超出训练范围）。
  - 多种图像损坏级别（从无损坏到严重损坏）。
- **Benchmark 与对比方法**：
  - 主要对比：标准 CTM (Vovk et al., 2021)。
  - 对有害概念漂移检测速度，还对比了 Podkopaev & Ramdas (2021b) 的序列检验（PR-ST）和变更点检测（PR-CD-online 和 PR-CD-50）。
  - 所有方法使用相同的神经网络预测器（对表格数据为 MLPRegressor，对 MNIST 为 3 层 MLP，对 CIFAR-10 为 ResNet-32）。

### 4. 资源与算力（若有说明）

论文附录中未明确说明使用的具体 GPU 型号、数量和训练时长。只在模型实现中描述了使用 PyTorch 框架和常见配置（如批量大小 64、学习率 0.001、训练 30 个 epoch）。未提供训练耗时或硬件资源细节。研究团队可能使用了标准单 GPU（如 V100或 A100）进行实验，但论文未明确报告。

### 5. 实验数量与充分性

- **实验数量**：
  - 表格数据上的良性漂移实验：每个数据集 200 个随机种子，运行 3000 个测试点，结果取平均。
  - 图像损坏实验：5 个随机种子，展示不同损坏级别和类型的 WCTM 轨迹。
  - 有害概念漂移检测延迟实验：200 个随机种子，计算平均检测延迟（ADD）和标准误差。
  - 根因分析实验：200 个随机种子，展示 WCTM 和 X-CTM 的响应。
  - 消融实验：包括密度比估计器类型（逻辑回归 vs MLP）、赌博函数类型（复合 vs 简单）、漂移强度等。
- **充分性与公平性**：
  - 实验覆盖了常见漂移类型（协变量漂移、概念漂移、混合漂移），且在不同数据集上验证了泛化性。
  - 对比方法均为公开基线，实现可靠。
  - 随机种子重复多次，报告均值与标准误差，统计严谨。
  - 消融实验充分探讨了关键组件的影响。
  - 但在计算效率对比中只提供了单一数据集下的运行时间，未分析大规模数据或复杂模型下的扩展性。

### 6. 论文的主要结论与发现

- **自适应能力**：WCTM 能有效适应良性协变量漂移，维持目标覆盖（0.9），避免误报，而标准 CTM 会在类似情况下产生大量误报。
- **检测速度**：WCTM 在检测有害概念漂移时远快于 PR-ST 和 PR-CD 方法，平均检测延迟（ADD）降低 3 倍以上；与 CTM 相比，检测速度相当或略快（尤其是在图像损坏下）。
- **根因诊断**：通过并行运行 WCTM 和 X-CTM，能够区分概念漂移和极端协变量漂移，为恢复提供指导。
- **理论贡献**：建立了加权共形 p 值序列的 IID 均匀性定理（定理 3.1），为任意零假设下的顺序检验奠定基础。

### 7. 优点

- **创新性强**：首次提出加权共形检验鞅（WCTM），将标准 CTM 推广到更广泛的非参数零假设，理论贡献显著。
- **实用性高**：WATCH 框架同时实现自适应、快速检测和根因分析，满足实际 AI 运维需求。实验场景覆盖多种漂移类型和真实数据集。
- **统计保证**：保留 CTM 的任意有效误报控制（Ville 不等式）和平均运行长度控制（Shiryaev-Roberts）。
- **可解释性**：双鞅结构提供清晰的诊断信号。
- **消融实验丰富**：分析了密度比估计器、赌博函数等影响，验证了设计选择。

### 8. 不足与局限

- **实验覆盖有限**：未包括多分类、时间序列、自然语言等更复杂任务；未测试大规模模型（如大语言模型）部署场景。
- **计算开销**：在线密度比估计需要持续重新训练分类器，可能带来额外计算成本，论文未详细分析扩展性（尤其在高频流数据下）。
- **理论假设**：加权共形 p 值的独立性依赖于近似相等分布假设（如 \( \hat{F}_V = F_V \)），现实中可能不完全满足，导致轻微偏差；零假设中对密度比估计准确性的依赖可能在实际中难以严格验证。
- **对比基线不足**：仅与 CTM 和 Podkopaev & Ramdas 的方法对比，缺少与其他在线异常检测或 MAB 方法的比较；也未对比基于深度学习的端到端监测方法。
- **未公开代码**：论文脚注提供了 GitHub 仓库，但分析时未验证代码可复现性（按陈述应可用）。
- **缺少安全性讨论**：虽然声称适用于高风险场景，但未分析当密度比估计被对抗性攻击时 WCTM 的鲁棒性。

（完）
