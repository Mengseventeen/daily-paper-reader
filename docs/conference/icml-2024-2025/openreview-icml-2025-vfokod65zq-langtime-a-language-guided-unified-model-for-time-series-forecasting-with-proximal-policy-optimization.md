---
title: "LangTime: A Language-Guided Unified Model for Time Series Forecasting with Proximal Policy Optimization"
title_zh: LangTime：基于语言引导和近端策略优化的统一时间序列预测模型
authors: "Wenzhe Niu, Zongxia Xie, Yanru Sun, Wei He, Man Xu, Chao Hao"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=VfoKOD65Zq"
tags: ["query:ai-finance"]
score: 4.0
evidence: 语言引导的时间序列预测模型，使用LLM和强化学习，可应用于金融
tldr: 利用预训练大语言模型进行时间序列预测时面临跨域泛化、跨模态对齐和误差累积等挑战。本文提出LangTime模型，通过构建时间理解提示（TCP）和强化学习微调，在包含金融序列的多个数据集上实现了更好的零样本泛化性能。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 799, \"height\": 248, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 780, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 800, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1759, \"height\": 723, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 820, \"height\": 613, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 790, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 790, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 787, \"height\": 300, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 780, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 767, \"height\": 287, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1395, \"height\": 890, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vfokod65zq/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1394, \"height\": 895, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1771, \"height\": 1136, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 869, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 857, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 868, \"height\": 551, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 869, \"height\": 555, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 854, \"height\": 568, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 868, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1781, \"height\": 2222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 641, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1356, \"height\": 340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1560, \"height\": 308, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1081, \"height\": 663, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1334, \"height\": 668, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1552, \"height\": 664, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1304, \"height\": 669, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1238, \"height\": 920, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1783, \"height\": 1275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1780, \"height\": 991, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 984, \"height\": 1472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1519, \"height\": 940, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vfokod65zq/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1674, \"height\": 946, \"label\": \"Table\"}]"
motivation: LLM用于时间序列预测存在跨域泛化差、模态对齐难和自回归误差累积问题。
method: 设计数据集和通道级文本提示，结合PPO强化学习微调LLM进行预测。
result: 在多个跨域基准（包括金融数据）上，LangTime的预测误差低于现有方法。
conclusion: 语言提示和强化学习为提升时间序列预测泛化性提供了有效框架，适用于金融场景。
---

## Abstract
Recent research has shown an increasing interest in utilizing pre-trained large language models (LLMs) for a variety of time series applications. However, there are three main challenges when using LLMs as foundational models for time series forecasting: (1) Cross-domain generalization. (2) Cross-modality alignment. (3) Error accumulation in autoregressive frameworks. To address these challenges, we proposed **LangTime**, a **lan**guage-**g**uided unified model for **time** series forecasting that incorporates cross-domain pre-training with reinforcement learning-based fine-tuning. Specifically, LangTime constructs Temporal Comprehension Prompts (TCPs), which include dataset-wise and channel-wise instructions, to facilitate domain adaptation and condense time series into a single token, enabling LLMs to understand better and align temporal data. To improve autoregressive forecasting, we introduce TimePPO, a reinforcement learning-based fine-tuning algorithm. TimePPO mitigates error accumulation by leveraging a multidimensional rewards function tailored for time series and a repeat-based value estimation strategy. Extensive experiments demonstrate that LangTime achieves state-of-the-art cross-domain forecasting performance, while TimePPO fine-tuning effectively enhances the stability and accuracy of autoregressive forecasting.

---

## 论文详细总结（自动生成）

以下是对论文《LangTime: A Language-Guided Unified Model for Time Series Forecasting with Proximal Policy Optimization》的详细中文总结，按照要求的要点展开。

---

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：近年来，预训练大语言模型（LLM）在时间序列预测领域展现出潜力，但直接应用面临三大核心挑战：
  1. **跨域泛化**：不同领域的时间序列统计特性差异大，相同数值在不同域含义不同，难以统一建模。
  2. **跨模态对齐**：LLM 基于文本语料训练，难以直接理解数值型时间序列，模态差异导致对齐困难。
  3. **误差累积**：自回归预测框架中，前一步输出作为下一步输入，误差会随步长逐步放大，损害长程预测性能。

- **论文目标**：提出一种统一的、语言引导的时间序列预测模型 **LangTime**，通过结合跨域预训练和基于近端策略优化（PPO）的微调算法 **TimePPO**，同时缓解以上三个问题，实现更准确、稳定的长期预测。

---

## 2. 方法论

### 核心思想
- 利用语言提示（Prompt）桥接时间序列与 LLM，使模型理解不同域和通道的语义信息；引入强化学习微调，优化自回归生成过程中的整体回报，抑制误差累积。

### 关键技术细节

1. **Temporal Comprehension Prompts (TCPs)**  
   - 包含四部分信息：**域描述**（数据集特性）、**时间戳**、**通道描述**（具体变量含义）、**时间序列表示**（由 Temporal Encoder 提取的嵌入）。
   - 通过特殊标记 `<|EMB|>` 和 `<|OUT|>` 分别压缩时间序列为单个 token 并引导预测，使 LLM 能够聚焦关键时序模式。

2. **Temporal Encoder (TE)**  
   - 轻量级通道独立编码器，将输入序列分片（patch）后线性变换为固定维度的表示，并随机掩码（mask rate \( r_m \)）以增强泛化。

3. **多任务预训练**  
   - 联合优化**重建任务**（通过被掩码的 token 恢复原始序列）和**预测任务**（自回归预测未来值）。
   - 损失函数：加权 Huber 损失，\(\mathcal{L}_{\text{pre-train}} = \alpha \mathcal{L}_{\text{recon}} + (1-\alpha) \mathcal{L}_{\text{pred}}\)，其中 \(\alpha\) 平衡两项。

4. **TimePPO 微调算法**  
   - **奖励函数**：从 MSE、MAE、KL 散度三个维度评估预测质量，并加入 MSE 惩罚项（参考新旧模型差异）以稳定更新。  
     \[
     R(\hat{y}_t) = \tanh\left(\tau \sum_i w_i R_i(\hat{y}_t, y_t)\right) - \beta \text{MSE}(\hat{y}_t, \hat{y}_t^{\text{ref}})
     \]
   - **值函数**：假设模型从当前步开始重复上一步输出直到序列结束，计算累积奖励作为期望回报。
   - **优势估计**：采用 GAE（Generalized Advantage Estimation）计算优势函数 \(\hat{A}_t\)。
   - **策略更新**：含 clip 机制和校正项（alignment tax）的 PPO 目标函数：  
     \[
     \mathcal{L}_{\text{TimePPO}} = \mathbb{E}\left[ \min\left( r(\theta)\hat{A}, \text{clip}(r(\theta), 1-\epsilon,1+\epsilon)\hat{A} \right) \right] - \eta \mathcal{L}_{\text{pred}}
     \]
   - 整体流程：运行策略收集轨迹 → 计算奖励和值 → 计算优势 → 更新策略（详见 Algorithm 1）。

---

## 3. 实验设计

### 数据集与场景
- **预训练与微调**：7 个主流时间序列数据集：ETTh1、ETTh2、ETTm1、ETTm2（电力变压器监测）、Electricity（电力消费）、Exchange（汇率）、Weather（气象）。
- **零样本测试**：Traffic（交通占用率）和 Illness（流感发病率），用于评估跨域迁移能力。
- **评估协议**：lookback 窗口固定 96，预测长度 {96, 192, 336, 720}（零样本中 Illness 为 {24,36,48,60}，Traffic 为 {96,192,336,720}）。
- **指标**：MSE 和 MAE。

### Benchmark 及对比方法
- **LLM-based 方法**：UniTime（官方代码跨域训练）、AutoTimes、S\(^2\)IP-LLM、Time-LLM、GPT4TS。
- **专用时间序列模型**：PatchTST、TimesNet。
- **骨干网络**：Qwen2-0.5B-Instruction（同时将 GPT-2 和线性层作为 backbone 消融）。
- **公平性**：对比方法使用官方代码，并在相同输入/输出设置下重新训练或调整。

---

## 4. 资源与算力

- 文中明确提及：**8 块 NVIDIA A100 80GB GPU**。
- 框架使用 PyTorch，优化器 AdamW。
- **训练耗时**：论文未报告具体训练时长（如几天或小时），仅说明使用了上述硬件配置。

---

## 5. 实验数量与充分性

- **主要实验结果**（表 1）：涵盖 7 个数据集 × 4 个预测长度 = 28 个设置 × 多种方法对比，LangTime 在 “跨数据集训练” 类别中取得 58/70 最优，TimePPO 微调后在 “单数据集微调” 类别中取得 45/70 最优。
- **消融实验**：
  - TCPs 组件（语言引导、时间戳、域信息、通道信息）的贡献（表 3）。
  - 奖励函数维度（MSE、MAE、KL）的贡献（表 4）。
  - 不同 backbone（Qwen2、GPT-2、线性层）对比（表 5）。
  - 提示修改（指令/背景变化）对性能的影响（表 6）。
- **零样本迁移**：Traffic 和 Illness 上的零样本结果（表 7）。
- **参数敏感性**：\(\alpha\)（预训练损失权重）、\(\tau\)（奖励函数缩放）、\(\beta\)（MSE 惩罚）、\(\eta\)（校正项）的敏感性分析（图 4-6）。
- **深度分析**：
  - 误差累积分析（最后一步预测性能，表 8）。
  - T-SNE 可视化（嵌入空间分离度，图 7）。
  - 注意力图可视化（预测 token 关注的模式，图 8）。
- **额外**：附录包含更多结果（表 18-22）、Zero-shot 跨域迁移（表 13）、与基础模型 TimesFM 对比（表 14）、微调数据量和组件冻结的影响（表 15-16）。

**充分性评价**：实验覆盖面广，含主结果、消融、零样本、参数分析、可视化，对比方法多为官方重跑，公平性较好。但零样本仅测试两个数据集，泛化广度可进一步拓展。

---

## 6. 主要结论与发现

1. **跨域预训练有效**：LangTime 在跨域预训练后，在 7 个数据集的多数预测长度上超越其他跨域训练方法（UniTime、AutoTimes），证明 TCPs 能帮助 LLM 区分不同域并学习通用时序模式。
2. **TimePPO 提升自回归稳定性**：相比标准监督微调（SFT），TimePPO 在长程预测的末尾步（误差累积最严重）上表现更优，有效缓解了累积误差。
3. **零样本迁移能力强**：在未见过的 Traffic 和 Illness 数据上，LangTime 性能领先，表明语言引导提升了模型对全新分布的适应能力。
4. **组件贡献明确**：TCPs 中域信息和通道信息贡献最大，时间戳作用较小；奖励函数中所有维度（MSE、MAE、KL）均有收益，其中 MSE 维度最关键。
5. **骨干选择影响**：Qwen2-0.5B-Instruct 优于 GPT-2，替换为线性层性能大幅下降，说明 LLM 的序列建模能力被成功迁移至时间序列。

---

## 7. 优点

- **创新性**：首次将语言引导的细粒度提示（包含域和通道语义）与基于 PPO 的强化学习微调相结合，同时解决跨域对齐和误差累积问题。
- **统一框架**：一个模型即可处理不同域、不同通道数、不同长度的时序数据，无需为每个域单独训练。
- **算法适配**：TimePPO 针对连续动作空间（时间序列）重新设计了奖励函数（多维评价 + MSE 惩罚）和值函数（重复策略），使 PPO 在时序任务上稳定有效。
- **实验全面**：覆盖多数据集、多预测长度、多种对比方法、多种消融和可视化，代码开源，可复现性强。
- **实用价值**：零样本迁移能力降低了在新领域部署的成本；少量微调数据（5% 数据量）也能带来增益，适合资源受限场景。

---

## 8. 不足与局限

- **计算成本**：使用 8×A100 GPU，预训练和微调资源需求较高；TimePPO 需维护参考模型和多次前向传播，推理阶段仍为自回归，时间开销较大。
- **骨干依赖**：主要实验基于 Qwen2-0.5B-Instruct，虽验证了 GPT-2 也有效，但在更大参数量或不同架构上的适应性未系统研究。
- **零样本覆盖面窄**：零样本仅测试 Traffic 和 Illness，且 Illness 预测长度较短；未在更多异构领域（如金融高频、物联网、医疗等）验证泛化性。
- **域与通道描述依赖先验知识**：TCPs 需要人工提供的域描述和通道描述，对于完全未知的新数据集，自动生成或缺失描述会限制性能。
- **未与最新时序基础模型（如 Chronos、TimesFM）在同等规模下全面对比**：文中仅与 TimesFM 做了部分对比（表 14），且 TimesFM 在部分数据集上略优，LangTime 优势不完全压倒。
- **奖励函数维度选择**：虽多维评价有效，但权重 \(w_i\) 为超参数，未提供自动调优方法，不同数据集可能需要不同权重。

---

（完）
