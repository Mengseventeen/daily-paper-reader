---
title: A decoder-only foundation model for time-series forecasting
title_zh: 用于时间序列预测的解码器基础模型
authors: "Abhimanyu Das, Weihao Kong, Rajat Sen, Yichen Zhou"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=jn2iTJas6h"
tags: ["query:ai-finance"]
score: 8.0
evidence: 解码器基础模型用于时间序列预测，零样本泛化
tldr: 受大语言模型启发，本文设计了一个基于解码器注意力与输入分块的时间序列基础模型。通过在大规模真实与合成时序语料上预训练，该模型在多种未见数据集上的零样本预测精度接近各数据集专用监督模型。为金融等领域的快速部署提供了通用解决方案。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1317, \"height\": 783, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1779, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 690, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 608, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 609, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 689, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1780, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1758, \"height\": 907, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1764, \"height\": 902, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1754, \"height\": 1817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1769, \"height\": 1819, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-jn2itjas6h/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1755, \"height\": 1821, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-jn2itjas6h/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 855, \"height\": 664, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-jn2itjas6h/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1600, \"height\": 942, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-jn2itjas6h/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-jn2itjas6h/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1767, \"height\": 469, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-jn2itjas6h/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1767, \"height\": 505, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-jn2itjas6h/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1485, \"height\": 275, \"label\": \"Table\"}]"
motivation: 现有时间序列预测模型需要针对每个数据集重新训练，缺乏通用性。
method: 预训练一个解码器风格的注意力模型，使用输入分块和大规模时序语料（包括真实与合成数据）。
result: 在多个未见数据集上零样本预测准确度接近有监督的专用模型。
conclusion: 该基础模型为跨域零样本时序预测提供了新范式，在金融领域有巨大潜力。
---

## Abstract
Motivated by recent advances in large language models for Natural Language Processing (NLP), we design a time-series foundation model for forecasting whose out-of-the-box zero-shot performance on a variety of public datasets comes close to the accuracy of state-of-the-art supervised forecasting models for each individual dataset. Our model is based on pretraining a decoder style attention model with input patching, using a large time-series corpus comprising both real-world and synthetic datasets. Experiments on a diverse set of previously unseen forecasting datasets suggests that the model can yield accurate zero-shot forecasts across different domains, forecasting horizons and temporal granularities.

---

## 论文详细总结（自动生成）

# 论文《A decoder-only foundation model for time-series forecasting》详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：受大语言模型（LLM）在自然语言处理中零样本泛化能力的启发，作者探究是否可能构建一个**时间序列基础模型**，使其在未见过的新数据集上仅凭预训练就能达到接近顶尖监督模型的预测精度，从而免去针对每个数据集的单独训练。
- **背景挑战**：时间序列没有像语言那样的固定词汇和语法；数据规模远小于文本；模型需支持变长上下文、变长预测窗口和不同时间粒度。现有方法（如ARIMA、DeepAR、PatchTST）多为监督学习，缺乏通用基础模型。

## 2. 提出的方法论
### 核心思想
- 采用**纯解码器（decoder-only）Transformer架构**，结合输入分块（patching）与因果注意力，在大规模真实与合成时序数据上预训练，学习通用的时间模式。
- 设计关键：输入补丁长度（`input_patch_len`）与输出补丁长度（`output_patch_len`）解耦；通过随机掩码训练支持任意上下文长度；使用更长的输出补丁减少自回归步数。

### 关键技术细节
1. **输入处理**：将时间序列划分为连续的非重叠补丁（patch），每个补丁经残差块（Residual Block）映射为嵌入向量，加上位置编码作为Transformer输入。
2. **因果注意力**：每个输出token只能关注其之前的所有输入token（包括自身），符合作者设定的解码器训练方式。
3. **输出预测**：每个输出token经另一个残差块预测其对应补丁后的连续`output_patch_len`个时间点（而非仅一个点）。训练时同一输入序列的每个补丁位置都产生一个预测损失。
4. **损失函数**：均方误差（MSE），可扩展为分位数损失做概率预测。
5. **掩码策略**：训练时对第一块补丁随机掩码前`r`个时间点（`r ∈ [0, p-1]`），使模型能适应从1到最大上下文长度的任意输入长度。
6. **推理机制**：采用自回归解码，每次生成`output_patch_len`个未来时间点，并与历史拼接作为下一步输入，直到填满所需预测长度。

### 公式/算法文字说明
- 训练目标：对于每个时间步 `j`，用前 `p*j` 个时间点预测后 `h` 个时间点（`h = output_patch_len`），最小化MSE。
- 自回归推理：若输入长度不是补丁大小整数倍，则补零并标记掩码。

## 3. 实验设计
### 数据集
- **预训练数据**：Google Trends（22k查询，多种粒度约0.5B点）、Wiki Pageviews（约300B点）、合成数据（3M条，长度2048，含ARMA、季节、趋势等）、M4、Electricity、Traffic、Weather、Favorita Sales、LibCity等。总时间点数约100B。
- **零样本测试数据集**（均未参与预训练）：
  - **Monash Archive**：30选取18个无缺失数据集，覆盖分钟至年，包含统计与深度学习基线。
  - **Darts**：8个单变量数据集（如AirPassengers、Sunspots等）。
  - **Inform/ETT**：4个电力变压器温度数据集（ETTh1、ETTh2、ETTm1、ETTm2），预测步长96、192。

### 对比方法
- **Monash**：ETS、ARIMA、DeepAR、N-BEATS、WaveNet、llmtime（GPT-3零样本）等。
- **Darts**：ARIMA、TCN、N-BEATS、N-HiTS、llmtime等。
- **ETT**：PatchTST、FEDFormer、Autoformer、Informer、llmtime等。
- 所有基线均为监督训练（除llmtime和TimesFM为零样本）。

### 指标
- 使用**MAE**，跨数据集采用**缩放MAE**（除以Naive预测的MAE）以公平聚合；Monash中报告几何均值和算术均值。

## 4. 资源与算力
- **模型规模**：最大200M参数（也有17M和70M版本用于消融实验）。
- **训练配置**：TPUv5e，16个张量核心。
- **训练时长**：200M模型约**2天**完成1.5M步迭代（全局batch size 4096）。
- 文中明确给出了这些信息，表明资源消耗远小于当代LLM。

## 5. 实验数量与充分性
### 实验组数
1. **零样本主实验**：在3组数据集上（Monash 18个、Darts 8个、ETT 8个任务）与多个基线对比。
2. **消融实验**：
   - **缩放定律**：3个模型大小（17M/70M/200M）随FLOPs增长的性能曲线。
   - **输出补丁长度**：8、16、32、64、128，在ETT 512步预测上对比。
   - **输入补丁长度**：8、16、32、64、128，在Monash上对比。
   - **合成数据消融**：200M模型有/无合成数据，在Monash和ETT上对比。
   - **微调研究**：在ETT 10%训练集上微调，与GPT4TS等对比（4个数据集×4个预测长度=16个任务）。
   - **与预训练PatchTST对比**：将补丁编码器-解码器模型改为预训练版本，报告Monash和ETT结果。
3. **可视化示例**：在合成数据和真实数据上展示预测曲线。

### 充分性与公平性
- **正面**：使用了标准公开数据集、官方指标、与llmtime相同的归一化聚合方式；对比了多种代表性方法；消融实验覆盖关键设计决策；微调实验采用与GPT4TS相同的协议。
- **潜在不足**：
  - 零样本评估仅在3组数据集上，未涵盖更多领域（如金融高频、医疗等）。
  - Monash基准中部分数据集上下文长度调优基于验证集，可能略优于纯零样本。
  - 对比llmtime时，GPT-3.5细节有差异（OpenAI停止GPT-3后改用Turbo）。
  - 消融实验仅报告平均指标，未做统计显著性检验。

## 6. 主要结论与发现
- **零样本性能接近监督模型**：TimesFM在Monash上几何平均缩放MAE优于所有基线（包括N-BEATS、llmtime等）；在ETT上平均MAE与PatchTST相当，显著优于其他方法；在Darts上结果也在前两名内。
- **缩放规律成立**：更大模型/更多计算持续提升零样本性能。
- **长输出补丁关键**：输出补丁长度越大（如128），自回归步数越少，预测误差越低。
- **输入补丁长度32为最佳平衡**：过短训练慢，过长丢失灵活性。
- **合成数据重要**：缺乏合成数据时，模型在非主流粒度（如15分钟、季度）上性能显著下降。
- **微调有效**：仅用10%训练数据微调后，性能超越GPT4TS等微调LLM方法，甚至接近全监督模型。

## 7. 优点
- **架构创新**：解码器-only + 输入分块 + 输出长补丁，自然支持变长上下文与任意预测长度，训练高效（并行预测所有补丁）。
- **数据策略**：结合海量真实数据（Wiki、Trends）和合成数据，覆盖广泛模式，增强泛化。
- **零样本实用性强**：模型仅200M参数，可部署于资源受限场景；已开源权重（timesfm-1.0-200m）。
- **实验严谨**：跨数据集、多粒度、多基线对比；消融实验覆盖核心设计点；微调验证下游适配能力。
- **可拓展性**：架构可扩展至概率预测、协变量处理等，文中给出了可行方向。

## 8. 不足与局限
- **缺少概率预测**：当前仅输出点预测，未提供置信区间或分位数输出（虽指出可扩展，但未实现）。
- **协变量处理缺失**：模型无法接收静态/动态协变量（如节假日、天气），限制了在某些复杂场景的应用。
- **零样本评估覆盖有限**：只测试了3组公开数据集，未包含财经高频、传感器异常、长尾低频等场景。
- **数据偏见风险**：预训练数据主要来自Wiki和Google Trends，可能偏向特定语言/地区，导致对某些领域预测偏差。
- **可解释性差**：深度模型如同黑箱，不如ARIMA等统计方法可分解趋势、季节分量；文中仅提及SHAP等事后归因方法，未深入解决。
- **计算资源仍较高**：虽比LLM小，但200M模型仍需2天TPUv5e 16核训练，普通研究者难以复现。
- **实验统计性不够强**：部分结果（如Darts数据集仅8个）标准误差大，方法间差异不显著；消融实验未做重复运行推断。

（完）
