---
title: Optimal Information Retention for Time-Series Explanations
title_zh: 时间序列解释的最优信息保留
authors: "Jinghang Yue, Jing Wang, Lu Zhang, Shuo Zhang, Da Li, Zhaoyang Ma, Youfang Lin"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=u6k5y3FDW1"
tags: ["query:ai-finance"]
score: 7.0
evidence: 解释金融时间序列深度学习模型，信息保留
tldr: 解释时间序列深度模型时，现有方法存在冗余与不完整。本文提出最优信息保留原则，以条件互信息定义最小化冗余与最大化完整性作为优化目标，并开发ORTE框架学习二元掩码。实验证明该方法能有效提取关键模式，适用于金融等敏感领域。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1684, \"height\": 542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1644, \"height\": 856, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1764, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1762, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 687, \"height\": 454, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1785, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1197, \"height\": 2245, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1210, \"height\": 2242, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1205, \"height\": 2249, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6k5y3fdw1/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1193, \"height\": 2245, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1780, \"height\": 952, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1774, \"height\": 429, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1776, \"height\": 479, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1774, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1777, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1085, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1075, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1077, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1780, \"height\": 402, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 900, \"height\": 361, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1780, \"height\": 403, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 898, \"height\": 360, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6k5y3fdw1/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1380, \"height\": 331, \"label\": \"Table\"}]"
motivation: 时间序列解释方法缺乏统一优化准则，导致解释冗余或遗漏关键模式。
method: 提出最优信息保留原则，通过条件互信息优化冗余与完整性，实现ORTE解释框架。
result: 在多个时间序列数据集上，ORTE生成的解释更简洁且更完整。
conclusion: 该原则为金融领域的模型可解释性提供了理论驱动的解决方案。
---

## Abstract
Explaining deep models for time-series data is crucial for identifying key patterns in sensitive domains, such as healthcare and finance. However, due to the lack of unified optimization criterion, existing explanation methods often suffer from redundancy and incompleteness, where irrelevant patterns are included or key patterns are missed in explanations. To address this challenge, we propose the Optimal Information Retention Principle, where conditional mutual information defines minimizing redundancy and maximizing completeness as optimization objectives. We then derive the corresponding objective function theoretically. As a practical framework, we introduce an explanation framework ORTE, learning a binary mask to eliminate redundant information while mining temporal patterns of explanations. We decouple the discrete mapping process to ensure the stability of gradient propagation, while employing contrastive learning to achieve precise filtering of explanatory patterns through the mask, thereby realizing a trade-off between low redundancy and high completeness. Extensive quantitative and qualitative experiments on synthetic and real-world datasets demonstrate that the proposed principle significantly improves the accuracy and completeness of explanations compared to baseline methods. The code is available at https://github.com/moon2yue/ORTE_public.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义

- **研究动机**：在医疗、金融等敏感领域中，对时间序列深度学习模型的解释至关重要，但现有解释方法（如 Integrated Gradients、Dynamask、TIMEX 等）缺乏统一的优化准则，导致生成的解释存在两个主要问题：
    - **冗余**：包含与任务无关的无关模式；
    - **不完整**：遗漏关键的判别性时间模式。
- **核心挑战**：由于时间序列的动态性和异质性，冗余与不完整往往代表不同的语义（如不同时间片段），启发式方法难以同时满足低冗余和高完整性的要求。
- **论文贡献**：提出**最优信息保留原则**（Optimal Information Retention Principle），从信息论角度统一优化解释目标；并基于该原则实现实际框架 **ORTE**（Optimal Information Retention for Time-Series Explanations），在多个数据集上取得 SOTA 性能。

## 2. 方法论

- **核心思想**：基于信息论，定义三个优化准则：
    1. **语义信息保留**：确保解释子特征 \(X_m\) 的预测分布与黑箱模型一致，通过最小化 Jensen-Shannon 散度实现。
    2. **最小冗余信息保留**：最小化输入 \(X\) 与解释 \(X_m\) 之间在给定标签 \(Y\) 下的条件互信息 \(I(X; X_m | Y)\)，推导出对二值掩码分布的 KL 散度损失 \(\mathcal{L}_{\text{mask}}\)，并加入连续性正则化 \(\mathcal{L}_{\text{con}}\) 以保证时间连续性。
    3. **最大有效信息保留**：最小化 \(I(X; Y | X_m)\)，等价于最大化 \(X\) 与重建正样本 \(\hat{X}\) 间的互信息，同时最小化与负样本 \(\hat{X}^-\) 的互信息；通过对比学习损失 \(\mathcal{L}_{\text{ct}}\) 和均方误差 \(\mathcal{L}_{\text{sim}}\) 实现。
- **关键技术细节**：
    - **自适应掩码生成器（AMG）**：
        - 使用自回归 Transformer 生成概率矩阵 \(P(M|X)\)。
        - 提出 **adapt-STE**（自适应直通估计器），在前向传播中用小温度参数 \(\tau_f\) 保持概率尖锐，反向传播中用大温度参数 \(\tau_b\) 保持梯度忠实性，缓解传统 ST-GS 中前向与反向不对称的问题。
    - **对比解释分离器（CES）**：
        - 正样本：\(\hat{X} = \text{MLP}(M, X)\)，保留掩码区域的有效信息并避免 OOD。
        - 负样本：\(\hat{X}^- = (1-M) \odot X + M \odot \text{pad}\)，用高斯噪声填充掩码区域，过滤有效信息。
    - **预测分布对齐器（PDA）**：最小化 JS 散度对齐预测分布。
    - **总目标函数**：\(\mathcal{L} = \mathcal{L}_{\text{JS}} + \mathcal{L}_{\text{mrir}} + \mathcal{L}_{\text{meir}} + \gamma \mathcal{L}_{\text{spr}}\)，其中 \(\mathcal{L}_{\text{spr}} = \|M\|_1\) 促进稀疏性。

## 3. 实验设计

- **数据集**：
    - **合成数据集**（4个，含 ground-truth 解释标注）：FreqShapes、SeqComb-UV（单变量）、SeqComb-MV（多变量）、LowVar。
    - **真实世界数据集**（4个，仅 ECG 有 ground-truth）：ECG（心律失常检测）、PAM（人类活动识别）、Epilepsy（癫痫发作检测）、Boiler（机械故障检测）。
- **基准模型**：统一使用 **Vanilla Transformer** 作为预训练黑箱分类器；额外在 CNN 和 LSTM 上验证迁移性。
- **对比方法**：
    - IG (Integrated Gradients)
    - Dynamask
    - WinIT
    - CoRTX
    - SGT+Grad
    - TIMEX
    - TIMEX++（最先进基线）
- **评估指标**：
    - 对有 ground-truth 的数据：AUP（精度曲线下面积）、AUR（召回曲线下面积）、AUPRC（精度-召回曲线下面积）。
    - 对无 ground-truth 的数据：遮挡实验（遮挡底部 \(p\%\) 特征后 AUROC 下降）和插入实验（从底部向顶部插入特征后 AUROC 上升）。

## 4. 资源与算力

- 文中在附录 D.5 明确说明：所有实验运行于 **Ubuntu 18.04.6 LTS** 系统，使用 **4 块 NVIDIA GeForce RTX 2080 GPU**。
- 训练周期：根据不同数据集，ORTE 训练轮次为 5～100 epochs（参见附录表 5）。
- 未提供总训练时长，但通过表 13 计算代价数据可以推测：在 PAM 数据集上 ORTE 的推理时间约 0.49 秒/样本，与 TIMEX/TIMEX++ 同量级。

## 5. 实验数量与充分性

- **核心实验**：表 1 给出在 4 个合成数据集上（3 个指标 × 4 = 12 项）与 7 个基线的对比，ORTE 在 10/12 项上取得最优。
- **真实世界数据集**：表 2 给出 ECG 上的对比（3 指标 × 8 方法），以及消融实验（6 种变体）；图 3、图 4 分别展示 PAM、Epilepsy、Boiler 上的遮挡/插入实验曲线。
- **跨架构验证**：附录 E 在 CNN 和 LSTM 黑箱上进一步对比（表 9–12），同样验证 ORTE 优势。
- **适配性对比**：图 5、图 6 专门比较 adapt-STE 与标准 STE 的效果。
- **计算代价**：表 13 比较了参数、FLOPs 和推理时间。
- **复杂性充分性**：覆盖了单变量/多变量、合成/真实、不同分类任务、不同模型架构、消融控制和超参数敏感性（附录中给出各组件贡献），实验设计全面、对比公平（统一使用 Transformer 分类器，基准方法复现一致）。

## 6. 主要结论与发现

- ORTE 在有 ground-truth 的合成数据上显著优于所有基线：相比最强基线 TIMEX++，AUPRC 平均提升 7.48%，AUR 提升 22.27%，实现低冗余与高完整性的平衡。
- 在真实 ECG 数据上，ORTE 的 AUPRC 比 TIMEX++ 提升 8.85%，AUP 提升 13.25%，AUR 提升 11.71%。
- 遮挡/插入实验表明，ORTE 定位的关键特征最为精准，且性能稳定（误差带窄）。
- **adapt-STE** 相比标准 STE，在 AUP 上显著改进（图 5、图 6），有效缓解了离散映射梯度不稳定的问题。
- 消融实验证明，各组件（adapt-STE、\(\mathcal{L}_{\text{JS}}\)、\(\mathcal{L}_{\text{ct}}\)、\(\mathcal{L}_{\text{con}}\)、\(\mathcal{L}_{\text{sim}}\)、\(\mathcal{L}_{\text{spr}}\)）均对最终性能有贡献，缺一不可。
- 最优信息保留原则为时间序列解释提供了统一的理论框架，可推广至其他解释方法。

## 7. 优点

- **理论驱动**：从信息论条件互信息出发，严谨推导三个优化目标，而非启发式设计。
- **统一框架**：同时解决冗余和不完整两大问题，实现可解释性的 Pareto 最优。
- **稳定训练**：提出 adapt-STE 巧妙解决二值掩码学习中的前向-反向不对称问题，提升解释准确性。
- **全面实验**：涵盖多种数据集、模型架构、评估协议（遮挡/插入/精确匹配），消融和对比充分，结果具有说服力。
- **开源代码**：提供完整代码仓库，便于复现和推广。

## 8. 不足与局限

- **超参数敏感**：文中承认 \(\tau_f\)、\(\tau_b\)、\(r\)、\(\alpha\)、\(\beta\)、\(\gamma\) 等多个超参数需要基于数据和任务类型进行调整，增加了实际应用中的调参成本。
- **泛化性验证有限**：虽然原则具有通用性，但仅实现了 ORTE 一个具体框架；文中提到“将最优信息保留原则扩展到梯度或掩码等其他解释方法需要进一步研究”。
- **计算开销**：与 TIMEX/TIMEX++ 相比，ORTE 推理时间略长（约 2 倍），且训练过程中使用 4 块 2080 GPU，在资源受限场景下可能不够高效。
- **假设局限**：推导中假设 \(p(m | x)\) 为伯努利分布且每个时间步独立，可能无法捕获长程时序依赖的复杂结构。
- **未覆盖所有领域**：实验集中在医疗（ECG、Epilepsy）和活动识别（PAM）、工业（Boiler），金融等其他敏感领域缺乏直接验证，其适用性有待进一步确认。

（完）
