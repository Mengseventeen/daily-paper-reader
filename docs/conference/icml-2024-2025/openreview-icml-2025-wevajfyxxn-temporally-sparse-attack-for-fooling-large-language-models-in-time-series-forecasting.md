---
title: Temporally Sparse Attack for Fooling Large Language Models in Time Series Forecasting
title_zh: 用于欺骗时间序列预测中大语言模型的时间稀疏攻击
authors: "Fuqiang Liu, Sicong Jiang"
date: 2025-01-24
pdf: "https://openreview.net/pdf?id=wEvAJFYXXN"
tags: ["query:ai-finance"]
score: 4.0
evidence: 对LLM时间序列预测的攻击，与股市分析相关
tldr: 现有攻击方法需修改整个时间序列，不切实际。本文提出时间稀疏攻击（TSA），通过子空间追踪将扰动限制在少量时间步，实现对LLM时间序列预测模型的高效攻击。实验表明该方法在多种模型上有效，为金融等领域的时序模型安全性评估提供了新工具。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-wevajfyxxn/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1326, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-wevajfyxxn/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1515, \"height\": 913, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-wevajfyxxn/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1621, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-wevajfyxxn/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1651, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-wevajfyxxn/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1642, \"height\": 321, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-wevajfyxxn/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1771, \"height\": 676, \"label\": \"Table\"}]"
motivation: 现有攻击方法需要修改整个时间序列，在真实场景中不切实际。
method: 将攻击建模为基数约束优化问题，采用子空间追踪方法限制扰动到少量时间步。
result: 在先进LLM时间序列模型上验证了攻击的有效性和高效性。
conclusion: 提出的稀疏攻击为时间序列预测模型的安全性评估提供了实用方法。
---

## Abstract
Large Language Models (LLMs) have shown great potential in time series forecasting by capturing complex temporal patterns. Recent research reveals that LLM-based forecasters are highly sensitive to small input perturbations. However, existing attack methods often require modifying the entire time series, which is impractical in real-world scenarios. To address this, we propose a Temporally Sparse Attack (TSA) for LLM-based time series forecasting. By modeling the attack process as a Cardinality-Constrained Optimization Problem (CCOP), we develop a Subspace Pursuit (SP)--based method that restricts perturbations to a limited number of time steps, enabling efficient attacks. Experiments on advanced LLM-based time series models, including LLMTime (GPT-3.5, GPT-4, LLaMa, and Mistral), TimeGPT, and TimeLLM, show that modifying just 10\% of the input can significantly degrade forecasting performance across diverse datasets. This finding reveals a critical vulnerability in current LLM-based forecasters to low-dimensional adversarial attacks.   Furthermore, our study underscores the practical application of CCOP and SP techniques in trustworthy AI, demonstrating their effectiveness in generating sparse, high-impact attacks and providing valuable insights into improving the robustness of AI systems.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机与背景）
- **动机**：大语言模型（LLM）在时间序列预测中表现优异，但现有研究表明其对输入扰动高度敏感。然而，已有攻击方法通常需要修改整个输入时间序列，这在真实场景（如金融、交通）中不切实际。
- **问题**：能否仅通过修改输入序列的**少量时间步**（稀疏扰动）来有效欺骗基于LLM的预测模型？
- **研究意义**：揭示LLM在时间序列预测中的关键脆弱性，为构建鲁棒可信的AI系统提供新视角。

## 2. 方法论：核心思想、关键技术细节、算法流程
- **核心思想**：将攻击建模为**基数约束优化问题**，限制扰动仅作用于少量时间步；采用**子空间追踪**算法高效求解。
- **关键技术细节**：
  - 使用**乘性扰动** `w`（扰动值 `ρ_i = w_i · X_i`）保证每个被扰动时间步的幅度受限（ℓ₁范数约束 `ϵ`）。
  - **零优化技巧**：在黑盒设定下，通过两侧查询估计梯度 `ĝ = (F(X, w+Δ) - F(X, w-Δ)) / (2Δ)`。
  - 结合**FGSM**思想：`w_i = ϵ · sign(ĝ)`。
- **算法流程**（Adapted SP）：
  1. 初始化扰动向量 `w=0`，支持集 `S=∅`，损失 `r=0`。
  2. 循环直到收敛：
     - 对当前不在S中的每个时间步 `j`，计算候选扰动 `w_j`（使用零优化+FGSM），评估损失。
     - 选取损失最大的 `τ` 个时间步索引 `ℓ`，更新 `S = S ∪ {ℓ}`。
     - 对S内所有时间步重新计算扰动 `w_S`。
     - 从S中保留损失最大的 `τ` 个索引，其余置零。
     - 更新当前损失 `r`。
  3. 返回 `τ`-稀疏乘性扰动 `w`。
- **计算复杂度**：`O(T × τ)`，优于贪心算法的 `O(T^τ)`。

## 3. 实验设计
- **数据集**（4个真实世界数据集）：
  - ETTh1（电力变压器温度与负荷，逐小时）
  - IstanbulTraffic（伊斯坦布尔交通流量，逐小时）
  - Weather（气象数据，逐小时）
  - Exchange Rates（8国每日汇率，1990-2016）
  - 数据划分：60%训练，20%验证，20%测试；攻击者无法访问训练/验证集。
- **目标模型**（7个）：
  - LLMTime：基于GPT-3.5、GPT-4、LLaMa 2、Mistral
  - TimeGPT（2024）
  - TimeLLM（基于GPT-2，2024）
  - TimesNet（非LLM基准，2023）
- **对比方法**：
  - 无攻击（clean）
  - 高斯白噪声（GWN）：标准差设为数据集均值的2%
  - 完整系列攻击（full series attack，来自Liu et al. 2024b）
- **评估指标**：MSE和MAE，固定输入窗口96步，预测48步。

## 4. 资源与算力
- **硬件**：Tesla V100 GPU（单卡）
- **软件**：Ubuntu 18.04 LTS, PyTorch 1.7.1, Python 3.7.4
- **算力量化**：论文**未明确说明**训练/攻击的具体时长或GPU数量，但提到计算时间随稀疏度 `τ` 线性增长（见图5b）。

## 5. 实验数量与充分性
- **主实验结果**（表1）：7个模型 × 4个数据集 × 3种条件（clean, GWN, TSA）= 84个MAE/MSE值，覆盖全面。
- **附加实验**：
  - 对抗防御实验（图4）：3个防御方法×3个模型×2种攻击类型（full vs sparse），共18条结果。
  - 超参数分析（图5）：考察 `ϵ` 对误差的影响、`τ` 对计算时间和误差的影响。
  - 可视化分析（图2-3）：展示预测偏差、输入/输出分布、误差相关性。
- **充分性评估**：实验设计较全面，对比了无攻击、随机噪声、完整系列攻击；防御实验验证了稀疏攻击的难防御性；超参数分析提供了调优指导。但缺少与最新黑盒稀疏攻击方法（如遗传算法、基于贝叶斯优化）的直接对比，且未讨论多变量预测场景。

## 6. 主要结论与发现
- **TSA显著降低预测性能**：仅扰动10%的时间步（τ=9/96）就能大幅提升MSE和MAE，效果优于全面噪声。
- **最大降幅案例**：IstanbulTraffic数据集上，TSA使LLMTime w/ Mistral的误差增加80.75%，LLMTime w/ GPT-4误差增加46.45%。
- **传统过滤防御无效**：高斯、均值、分位数滤波器难以恢复TSA带来的误差，因为它们依赖统计均匀性假设。
- **超参数影响**：扰动幅度 `ϵ` 越大，误差指数级增长；计算时间与稀疏度 `τ` 线性正相关。
- **TSA引起系统性偏差**：输出分布分散，误差相关性增强（图3）。

## 7. 优点
- **新颖性**：首次将基数约束优化问题（CCOP）和子空间追踪（SP）引入时间序列对抗攻击，实现高效的稀疏扰动。
- **实用性**：黑盒设定，无需未来真实值、无需模型内部参数、无需完整训练数据，仅需查询能力。
- **有效性**：在多种主流LLM预测模型（GPT-3.5/4、LLaMa、Mistral、TimeGPT、TimeLLM）上均有效，且远超随机噪声。
- **可解释性**：通过分布、相关性分析展示了扰动机制，增强了可信度。
- **防御启发**：揭示了传统过滤防御的盲点，为未来鲁棒模型设计提供方向。

## 8. 不足与局限
- **多变量场景缺失**：论文仅报告单变量预测结果，未讨论多变量（高维）情况下稀疏攻击的效果和挑战。
- **攻击预算分析不足**：未给出实际查询次数或时间，仅给出复杂度阶数，实际应用中查询成本可能较高。
- **对比基线不完整**：未与现有黑盒稀疏攻击方法（如基于进化策略或贝叶斯优化的方法）进行比较，公平性有待加强。
- **防御方案未充分验证**：仅提出一个设想（自相关检测+高斯滤波），未进行实验验证，实用性存疑。
- **数据集局限**：仅涵盖交通、气象、汇率、电力四个领域，未涉及金融高频、医疗等场景，泛化性有待拓展。
- **假设前提限制**：攻击者必须能查询模型，且假设预测值可替代未来真实值（存在近似误差）。

（完）
