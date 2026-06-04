---
title: "$S^2$IP-LLM: Semantic Space Informed Prompt Learning with LLM for Time Series Forecasting"
title_zh: "S²IP-LLM: 基于语义空间提示学习与LLM的时间序列预测"
authors: "Zijie Pan, Yushan Jiang, Sahil Garg, Anderson Schneider, Yuriy Nevmyvaka, Dongjin Song"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=qwQVV5R8Y7"
tags: ["query:ai-finance"]
score: 7.0
evidence: 基于LLM的时间序列预测方法，适用于股票市场分析
tldr: 针对时间序列预测，该论文提出S²IP-LLM方法，通过将LLM预训练语义空间与时间序列嵌入空间对齐，利用联合空间中的提示进行预测。设计跨模态标记化模块，分解时间序列组件并拼接，在预测任务上取得更好性能，可应用于金融股票市场等场景。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 842, \"height\": 694, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1632, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1742, \"height\": 967, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 808, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 846, \"height\": 288, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1732, \"height\": 1001, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qwqvv5r8y7/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1620, \"height\": 1954, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 1378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1770, \"height\": 184, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1753, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1753, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1732, \"height\": 685, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1684, \"height\": 1111, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1718, \"height\": 498, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1774, \"height\": 1108, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1773, \"height\": 1109, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qwqvv5r8y7/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1478, \"height\": 213, \"label\": \"Table\"}]"
motivation: LLM的语义空间在时间序列应用中未被充分利用。
method: 设计跨模态对齐的标记化模块，将分解时间序列组件与LLM语义空间对齐，学习联合空间中的提示进行预测。
result: 在时间序列预测任务上取得更好性能，验证了语义空间对齐的有效性。
conclusion: 本方法为利用LLM进行时间序列预测提供了新范式，可推广到金融分析领域。
---

## Abstract
Recently, there has been a growing interest in leveraging pre-trained large language models (LLMs) for various time series applications. However, the semantic space of LLMs, established through the pre-training, is still underexplored and may help yield more distinctive and informative representations to facilitate time series forecasting. To this end, we propose Semantic Space Informed Prompt learning with LLM ($S^2$IP-LLM) to align the pre-trained semantic space with time series embedding space and perform time series forecasting based on learned prompts from the joint space. We first design a tokenization module tailored for cross-modality alignment, which explicitly concatenates patches of decomposed time series components to create embeddings that effectively encode the temporal dynamics. Next, we leverage the pre-trained word token embeddings to derive semantic anchors and align selected anchors with time series embeddings by maximizing the cosine similarity in the joint space. This way, $S^2$IP-LLM can retrieve relevant semantic anchors as prompts to provide strong indicators (context) for time series that exhibit different temporal dynamics. With thorough empirical studies on multiple benchmark datasets, we demonstrate that the proposed $S^2$IP-LLM can achieve superior forecasting performance over state-of-the-art baselines. Furthermore, our ablation studies and visualizations verify the necessity of prompt learning informed by semantic space.

---

## 论文详细总结（自动生成）

# 论文总结：《S2IP-LLM: 基于语义空间提示学习与LLM的时间序列预测》

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：预训练大语言模型（LLM）在时间序列分析中已显示出潜力，但其预训练建立的**语义空间**尚未被充分挖掘。现有方法（如Time-LLM）多采用文本描述或随机软提示，未能利用LLM本身具有的区分性与信息性的语义表示。
- **背景**：时间序列数据存在**非平稳性**、**概念漂移**和**多域差异性**，传统模型泛化能力有限。LLM凭借其强大的序列模式识别和推理能力，有望作为通用知识库，但如何有效对齐时间序列嵌入与语义空间仍是个挑战。
- **核心动机**：通过将LLM的预训练语义空间与时间序列嵌入空间对齐，学习联合空间中的提示（prompt），从而为时间序列预测提供更强、更有区分度的上下文信息。

## 2. 方法论

### 核心思想
提出 **S²IP-LLM**（Semantic Space Informed Prompt Learning with LLM），包含三个关键模块：

1. **时间序列标记化（Tokenization）**：
   - 对输入时间序列进行**可逆实例归一化**缓解分布偏移。
   - 采用**加法季节-趋势分解**（STL或经典方法），将归一化序列分解为趋势、季节、残差三部分。
   - 对每个分量进行**分块（patching）**（重叠滑动窗口），然后将三个分量的块**拼接**成一个元标记（meta-token），再通过投影层映射到LLM的嵌入维度D。

2. **语义空间引导的提示（Semantic Space Informed Prompting）**：
   - 利用预训练LLM的词元嵌入矩阵 \( E \in \mathbb{R}^{V \times D} \)，通过一个映射函数 \( f(\cdot) \) 降维得到语义锚点集合 \( E' \in \mathbb{R}^{V' \times D} \)（\( V' \ll V \)）。
   - 使用**余弦相似度**作为评分函数 \( \gamma(\cdot) \)，计算时间序列嵌入与每个语义锚点的相似度。
   - 选取**Top-K最相关**的语义锚点作为前缀提示（prefix-prompt），与时间序列嵌入拼接后输入LLM骨干网络（GPT-2）。

3. **优化目标**：
   - 总损失 = **均方误差（MSE）**（预测值与真实值） − \(\lambda\) × **对齐分数**（计算选中语义锚点与时间序列嵌入的余弦相似度之和）。
   - 其中 \(\lambda\) 控制对齐强度。

### 关键技术细节
- 骨干网络：**GPT-2**（仅微调位置嵌入和层归一化层，其余参数冻结）。
- 输入长度512，输出长度96/192/336/720等。
- 分块参数：块长LP=16，步长S=8。
- 语义空间大小V'通过网格搜索（1000, 2000, 5000）确定。

## 3. 实验设计

### 数据集
- **长期预测**：7个数据集（Weather, Electricity, Traffic, ETTh1, ETTh2, ETTm1, ETTm2），预测长度{96,192,336,720}。
- **短期预测**：M4数据集（年度、季度、月度、周度、日度、小时度子集）。
- **少样本预测**：上述长期预测数据集仅使用10%和5%训练数据。

### 基准方法与对比
- **Transformer类**：iTransformer, PatchTST, FEDformer, Autoformer, Non-Stationary Transformer, ETSformer, Informer。
- **非Transformer类**：DLinear, TimesNet, LightTS。
- **LLM类**：Time-LLM（含LlaMA和GPT-2两种骨干），OFA（One Fits All）。
- 所有模型在**统一评测管道**（Time-Series-Library）下复现，保证公平。

## 4. 资源与算力

- 论文未明确报告**精确的GPU数量和训练时长**。
- 实现框架：PyTorch。
- 硬件：NVIDIA RTX A6000 和 NVIDIA A100 GPU。
- 每个实验重复3次取平均。
- 超参数通过网格搜索确定，提示长度、对齐系数λ、语义空间大小V'等。

## 5. 实验数量与充分性

- **实验种类丰富**：
  - 长期预测：7数据集 × 4个预测长度 = 28组实验（表1及附录表6）。
  - 短期预测：M4全部子集，汇总SMAPE、MASE、OWA（表2及附录表7）。
  - 少样本预测：7数据集 × 2种数据比例（10%和5%），共14组实验（表3、4及附录表8、9）。
  - 消融研究：3个参数（提示长度、λ、V'）在各2个数据集上的影响（图3）。
  - 可视化：t-SNE/PCA分析嵌入空间（图4、5），定性验证对齐效果。
  - 模块消融：增加提示&对齐、分解的逐步效果（附录表10）。
- **充分性**：实验覆盖了主流基准、不同预测尺度、数据稀缺场景，并进行了全面的消融和可视化，客观公正。
- **潜在不足**：未在所有数据集上测试所有基线（部分附录表有缺失），但主要结果完整。

## 6. 主要结论与发现

1. **S²IP-LLM在长期、短期、少样本预测中**均取得**最佳或次优性能**，尤其在长期预测中显著优于Time-LLM和OFA等LLM基线。
2. **语义空间对齐和分解分块标记化是关键贡献**：消融实验显示依次添加分解和对齐组件可提升性能。
3. **可视化分析**：对齐后的时间序列嵌入形成更清晰簇，说明语义空间引导的提示增强了表示区分性。
4. 提示长度和λ存在最优区间，过大或过小均会降低性能；语义空间大小V'越大通常效果越好。

## 7. 优点

- **创新性**：首次系统利用LLM预训练语义空间（词元嵌入）作为时间序列提示的来源，而非随机软提示或文本描述。
- **模块设计精美**：时间序列分解+分块拼接的标记化方式保留了多成分动态信息，与语义空间对齐自然。
- **实验全面且公平**：使用统一评测管道，重复多次，消融充分，可视化直观。
- **实用性**：骨干网络GPT-2大部分参数冻结，仅微调少量参数，计算高效。

## 8. 不足与局限

- **实验覆盖范围有限**：
  - 仅验证了GPT-2作为骨干（附录提到GPT-2 small），未比较其他LLM（如LLaMA变体）在同一框架下的效果。
  - 少样本场景下部分数据集（如ETTh1、Traffic）的5%数据不足，结果缺失，说明方法对极端数据稀疏的鲁棒性未充分验证。
- **计算资源未量化**：未报告训练时间和GPU数量，难以评估方法实际效率。
- **应用限制**：
  - 依赖预训练LLM的词嵌入空间，可能对词汇表大小敏感（GPT-2有50k词元），降维映射可能丢失信息。
  - 方法假定语义空间与时间序列动态存在可对齐性，但解释性不强（什么语义锚点对应什么时间模式？）。
- **对比局限**：未与最新的时间序列基础模型（如Lag-Llama、TimeGPT）比较。
- **潜在偏差**：所有实验在公开基准上，未在真实金融等非静态领域验证。

（完）
