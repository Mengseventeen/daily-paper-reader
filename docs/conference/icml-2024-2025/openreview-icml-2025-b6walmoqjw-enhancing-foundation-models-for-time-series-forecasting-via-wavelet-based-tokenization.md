---
title: Enhancing Foundation Models for Time Series Forecasting via Wavelet-based Tokenization
title_zh: 通过小波标记化增强时间序列预测基础模型
authors: "Luca Masserano, Abdul Fatir Ansari, Boran Han, Xiyuan Zhang, Christos Faloutsos, Michael W. Mahoney, Andrew Gordon Wilson, Youngsuk Park, Syama Sundar Rangapuram, Danielle C. Maddix, Bernie Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=B6WalMoQJW"
tags: ["query:ai-finance"]
score: 4.0
evidence: 基于小波变换的标记化方法，可应用于金融时间序列预测
tldr: 为了构建有效的时间序列基础模型，提出小波标记化方法WaveToken，通过将时间序列分解为不同频率分量并量化，学习紧凑表示。该标记器在多个金融相关时间序列数据集上提升了预测性能。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1771, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1589, \"height\": 932, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1595, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1597, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1601, \"height\": 603, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1604, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1689, \"height\": 687, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1240, \"height\": 713, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1783, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1683, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1684, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1785, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1427, \"height\": 2176, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1432, \"height\": 2183, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1433, \"height\": 2187, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1557, \"height\": 2070, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1548, \"height\": 2072, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-b6walmoqjw/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1545, \"height\": 2070, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1765, \"height\": 557, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1764, \"height\": 509, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1763, \"height\": 505, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1767, \"height\": 812, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1764, \"height\": 734, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1765, \"height\": 735, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1779, \"height\": 370, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1773, \"height\": 443, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-b6walmoqjw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1416, \"height\": 2226, \"label\": \"Table\"}]"
motivation: 时间序列基础模型需要有效的离散标记化策略，现有方法未能充分利用多尺度结构。
method: 利用小波变换分解时间序列，阈值量化后作为词元，并预训练自回归模型预测系数。
result: 在多个标准基准（包括金融数据）上，WaveToken优于多种现有标记化方法。
conclusion: 小波标记化为时间序列基础模型提供了新的离散表示，有利金融时间序列分析。
---

## Abstract
How to best develop foundational models for time series forecasting remains an important open question. Tokenization is a crucial consideration in this effort: what is an effective discrete vocabulary for a real-valued sequential input? To address this question, we develop WaveToken, a wavelet-based tokenizer that allows models to learn complex representations directly in the space of time-localized frequencies. Our method first scales and decomposes the input time series, then thresholds and quantizes the wavelet coefficients, and finally pre-trains an autoregressive model to forecast coefficients for the forecast horizon. By decomposing coarse and fine structures in the inputs, wavelets provide an eloquent and compact language for time series forecasting that simplifies learning. Empirical results on a comprehensive benchmark, including 42 datasets for both in-domain and zero-shot settings, show that WaveToken: i) performs on par or better than recently proposed foundation models for forecasting while using a much smaller vocabulary (1024 tokens), and is competitive with modern deep learning models trained specifically on each dataset; ii) exhibits superior generalization capabilities, achieving the best average rank across all datasets for three complementary metrics; and iii) easily captures complex temporal patterns of practical relevance that are challenging for other recent pre-trained models, including trends, sparse spikes, and non-stationary time series with varying frequencies evolving over time.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究动机**：时间序列预测基础模型的关键在于**标记化（tokenization）**——如何为连续实值输入构建有效的离散词汇表，使模型能高效学习复杂依赖关系。现有方法（如 Chronos 的固定分箱、TimesFM 的补丁化）保留了自然时间顺序，但难以同时捕捉局部与全局模式（如趋势、尖峰、非平稳多频信号）。
- **整体含义**：提出基于**小波变换**的标记化方法 WaveToken，在**时间-频率联合空间**中学习紧凑、表达力强的词汇表，从而简化学习并提升泛化能力。

### 2. 论文提出的方法论

- **核心思想**：利用离散小波变换（DWT）将时间序列分解为**近似系数（低频）**和**细节系数（高频）**，通过缩放、阈值处理、量化转换为离散 tokens，再使用**T5 编码器-解码器**架构进行自回归预测（预测未来小波系数）。
- **关键技术流程**：
  1. **缩放**：对输入序列进行 z-score 归一化（减去均值，除以标准差）。
  2. **分解**：使用 Biorthogonal-2.2 小波基进行 J 层 DWT（最优为 1 层），得到近似系数 {a} 和细节系数 {d}，总数与输入长度相等。
  3. **阈值处理**（可选）：默认不使用阈值（No-thresholding），保留完整信息；备选有 CDF 阈值、VisuShrink、FDRC（基于假设检验）。消融实验显示，在大批量训练（8 GPU）下 No-thresholding 最优。
  4. **量化**：根据训练集联合经验分布，用 Freedman-Diaconis 规则确定最优箱数，将系数映射为离散 token，词汇表大小为 **1024**（含 PAD 和 EOS 特殊 token）。
  5. **序列构造**：将 tokens 按**从粗到细**顺序拼接（先近似，后各层细节），即 z = [a_J, d_J, ..., d_1]，使模型学习多尺度粗到细结构。
- **训练与推断**：
  - 损失函数：交叉熵，预测未来 tokens 的类别分布。
  - 推断时自回归采样，反量化得到连续系数，经逆 DWT（IDWT）和反缩放得到最终预测值。

### 3. 实验设计

- **数据集**：共 **42 个公开数据集**，涵盖能源、交通、金融、医疗、天气等多领域。分为三组：
  - **预训练集**（13 个，仅训练）
  - **领域内基准 Benchmark I**（15 个，训练 + 验证集评估）
  - **零样本基准 Benchmark II**（27 个，仅用于评估，从未用于训练）
- **对比基线**：
  - **任务特定模型**：DeepAR、PatchTST、TFT（均按每个数据集单独训练）
  - **其他基础模型**：TimesFM、Chronos（Mini–Large）、Moirai（Base & Large）、Lag-llama、Seasonal Naive
- **评估指标**：三个互补指标
  - **WQL**（加权分位数损失，评估概率预测）
  - **MASE**（均值绝对缩放误差，评估点预测）
  - **VRSE**（视觉相对平方误差，评估频率内容，避免传统指标对简单偏移的误判）
- **设置**：上下文长度 512，预测长度 64；使用 TSMixup 和合成数据做数据增强；所有实验结果均取 3 个随机种子平均。

### 4. 资源与算力

- **预训练**：使用 **8 张 A100 GPU**，训练 **200K 步**。
- **模型规模**：WaveToken 有四种尺寸 – Mini（19.2M）、Small（44.5M）、Base（199M）、Large（705.8M）。
- **消融实验**（图 5、图 7）使用 **1 张 A100 GPU** 训练 200K 步，用于超参数搜索（词汇大小、小波族、分解层数、阈值方法）。

### 5. 实验数量与充分性

- **实验数量**：
  - 两个基准共 42 个数据集 × 3 个指标 × 多种模型尺寸 × 3 个种子 → 大量实验。
  - 消融实验覆盖词汇大小（256~4096）、6 种小波族、分解层数（1~4）、4 种阈值方法。
  - 额外长时预测实验（预测长度 ×2、×3）。
  - 定性分析：合成数据边缘案例（指数趋势、尖峰、非平稳多频）及注意力图可视化。
- **充分性与公平性**：
  - 采用**几何平均相对得分**（除以 Seasonal Naive）聚合指标，避免异常值影响。
  - 所有基线使用各自官方实现和默认超参数。
  - 零样本设置严格防止数据泄漏。
  - 多次随机种子平均降低偶然性。
- **结论**：实验设计全面、客观，消融研究充分，证明各组件贡献。

### 6. 论文的主要结论与发现

- **性能优异**：WaveToken 在领域内和零样本基准上**达到或超越现有基础模型**，且与任务特定模型竞争，而词汇表仅 1024（Chronos 为 4096）。
- **泛化能力强**：在零样本基准（Benchmark II）上，WaveToken 在 WQL 和 MASE 上取得**最佳平均排名**；在所有基准上，VRSE 排名也很高。在长时预测（×2）中全面领先。
- **捕捉复杂模式**：能准确预测指数趋势、稀疏尖峰、时变多频非平稳信号，而 Chronos、TimesFM、Moirai 均失败。
- **小波分解提供了结构化学习**：注意力图显示模型**学会在粗到细的系数组间选择性关注**，尤其能聚焦于尖峰对应的细节系数。

### 7. 优点

- **紧凑且表达力强**：小波的稀疏性使得只需 1024 tokens 即可编码丰富信息，比同类模型更高效。
- **多尺度结构自然**：按粗到细拼接 tokens 显式提供了多尺度层级，模型能利用该结构简化学习。
- **零样本泛化突出**：在多领域从未见过的数据上表现出色，证明其作为通用基础模型的潜力。
- **误差分析全面**：引入 VRSE 指标弥补 WQL/MASE 对频率内容的忽略，更公正评估预测形状。
- **实验设计严谨**：充分消融、多种子平均、几何平均聚合、长时预测验证。

### 8. 不足与局限

- **解码速度慢**：自回归预测小波系数导致推理速度低于补丁模型（如 TimesFM），论文承认此局限。
- **固定上下文长度**：当前仅支持 512，未探索自动处理更长序列（小波本可自然扩展）。
- **阈值方法不稳定**：在单 GPU（小批量）与 8 GPU（大批量）下最佳阈值选择不一致，实际应用需调参。
- **词汇大小调优**：最优词汇 1024 是在固定分解层数下得到的，与分解深度可能有耦合，未详尽探索。
- **应用限制**：需要小波变换计算，极短序列可能不够充分；未涉及多变量或缺失值较多的场景。
- **数据集偏差**：虽然覆盖多领域，但网络流量、社交媒体等类型未包含，泛化边界待验证。

（完）
