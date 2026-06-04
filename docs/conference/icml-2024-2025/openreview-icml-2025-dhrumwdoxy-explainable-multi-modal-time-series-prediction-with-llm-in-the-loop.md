---
title: Explainable Multi-modal Time Series Prediction with LLM-in-the-Loop
title_zh: 具有LLM在环的可解释多模态时间序列预测
authors: "Yushan Jiang, Wenchao Yu, Geon Lee, Dongjin Song, Kijung Shin, Wei Cheng, Yanchi Liu, Haifeng Chen"
date: 2025-01-24
pdf: "https://openreview.net/pdf?id=DHRUMwDOXy"
tags: ["query:ai-finance"]
score: 8.0
evidence: 融合金融新闻文本的多模态时间序列预测
tldr: 针对现有时间序列预测忽视辅助文本模态（如金融新闻）的问题，提出TimeXL框架，结合原型时间序列编码器和多个协作大语言模型，实现融合文本与时间序列的精准预测与可解释性。在金融数据上展示出改善性能。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 675, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1569, \"height\": 751, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 774, \"height\": 837, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 717, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 373, \"height\": 856, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1687, \"height\": 1025, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1303, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1661, \"height\": 1066, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1768, \"height\": 981, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1602, \"height\": 1901, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1571, \"height\": 778, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1401, \"height\": 949, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1325, \"height\": 708, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1320, \"height\": 446, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1498, \"height\": 744, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1137, \"height\": 740, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1240, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dhrumwdoxy/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1663, \"height\": 842, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-dhrumwdoxy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1434, \"height\": 735, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dhrumwdoxy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 844, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dhrumwdoxy/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1787, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dhrumwdoxy/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1580, \"height\": 409, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dhrumwdoxy/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 896, \"height\": 228, \"label\": \"Table\"}]"
motivation: 时间序列预测常忽略金融新闻等上下文信号。
method: 采用原型编码器和三个LLM协作，融合时间序列与文本生成预测与解释。
result: 在包含金融新闻的多模态数据上取得更优预测和可解释性。
conclusion: TimeXL有效利用LLM提升多模态时间序列预测的准确性和可解释性。
---

## Abstract
Time series analysis provides essential insights for real-world system dynamics and informs downstream decision-making, yet most existing methods often overlook the rich contextual signals present in auxiliary modalities (e.g., financial news or domain-specific documents). To bridge this gap, we introduce TimeXL, a multi-modal prediction framework that integrates a prototype-based time series encoder with three collaborating Large Language Models (LLMs) to deliver more accurate predictions and interpretable explanations. First, a multi-modal prototype-based encoder processes both time series and textual inputs to generate preliminary forecasts alongside case-based rationales. These outputs then feed into a prediction LLM, which refines the forecasts by reasoning over the encoder’s predictions and explanations. Next, a reflection LLM compares the predicted values against the ground truth, identifying textual inconsistencies or noise. Guided by this feedback, a refinement LLM iteratively enhances text quality and triggers encoder retraining. This closed-loop workflow—prediction, critique (reflect), and refinement—continuously boosts the framework’s performance and interpretability. Empirical evaluations on four real-world datasets demonstrate that TimeXL achieves up to 8.9 \% improvement in AUC and produces human-centric, multi-modal explanations, highlighting the power of LLM-driven reasoning for time series prediction.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：现有时间序列预测方法大多仅依赖纯数值时序数据，忽略了辅助模态（如金融新闻、医疗报告等文本）中蕴含的丰富上下文信号，导致预测精度不足且缺乏可解释性。
- **背景**：深度学习模型虽能捕捉复杂时序依赖，但难以利用外部叙事信息；而大语言模型（LLM）在文本推理方面表现优异，但直接用于时序预测时无法处理数值信号且缺乏可解释机制。
- **目标**：构建一个融合时间序列与文本模态、兼具高预测精度和可解释性的框架，尤其针对金融、医疗等高风险场景。

## 2. 方法论
### 2.1 核心思想
- 提出**TimeXL**框架，采用**闭环工作流**：预测（Prediction）→ 反思（Reflection）→ 精炼（Refinement），将原型（Prototype）学习与三个LLM代理结合，实现多模态时序预测与可解释性。

### 2.2 关键技术细节
- **多模态原型编码器（Multi-modal Prototype-based Encoder）**：
  - 分别用卷积编码器对时间序列（`E_θ`）和文本（`E_ϕ`）提取段级表示。
  - 为每类学习时间序列原型 `P_time` 和文本原型 `P_text`，通过相似度（基于L2距离的指数变换）匹配输入段与原型。
  - 融合跨模态相似度分数，经非负全连接网络得到类别概率 `ŷ_enc`。
  - 正则化目标：聚类损失 `L_c`（段靠近最近原型）、证据损失 `L_e`（原型靠近段）、多样性损失 `L_d`（原型间距离≥阈值）。
- **LLM代理**：
  - **预测LLM（M_pred）**：基于原始文本及编码器选出的Top-ω原型-段对（作为可解释性证据），输出概率 `ŷ_LLM`。
  - **反思LLM（M_refl）**：对比预测与真实标签，生成反思报告（指出文本噪声或歧义）。
  - **精炼LLM（M_refine）**：根据反思报告精炼原始文本，生成更高质量的输入供下一轮迭代。
- **融合预测**：线性组合 `ŷ = α * ŷ_enc + (1-α) * ŷ_LLM`，α在验证集上选择。
- **迭代流程**：训练编码器→推理预测→LLM反思→文本精炼→重新训练编码器，重复至收敛或最大迭代次数。

## 3. 实验设计
### 3.1 数据集
- **Weather**：纽约市5年逐时气象数据，预测未来24小时是否下雨（二分类）。
- **Finance**：2017–2024年原材料价格与14个相关指数，融合新闻文本，预测下一交易日价格趋势（上涨/下跌/中性，三分类）。
- **Healthcare (TP)**：流感检测阳性率周数据，预测下周是否超过均值（二分类）。
- **Healthcare (MT)**：流感与肺炎死亡率周数据，预测是否超过均值（二分类）。

### 3.2 Benchmark与对比方法
- **时序基线**：DLinear, Autoformer, Crossformer, TimesNet, iTransformer, TSMixer, FreTS, PatchTST。
- **LLM时序方法**：LLMTime, PromptCast, OFA, Time-LLM, TimeCMA。
- **多模态时序方法**：MM-iTransformer, MM-PatchTST, TimeCAP。
- 评估指标：F1分数和AUROC（AUC），侧重处理类别不平衡。

### 3.3 实验设置
- 训练/验证/测试按6:2:2划分。
- 文本嵌入：Weather/Healthcare用BERT，Finance用Sentence-BERT。

## 4. 资源与算力
- **未明确说明**：论文在附录A.4中仅提及实验在“TensorEX服务器，2×Intel Xeon Gold 5218R CPU（20核）、512GB内存、4×RTX A6000 GPU（48GB显存）”上完成，但未给出具体训练时长或GPU数量使用细节。

## 5. 实验数量与充分性
- **主要实验**：在主表（表1）中对比了15种基线方法在4个数据集上的F1和AUC，共120个性能数据点。
- **消融实验**：
  - 表2（主文）：消融编码器、预测LLM、文本+原型、融合等组件。
  - 图6（附录）：消融编码器各正则项（L_c, L_e, L_d）在不同数据集上的影响。
  - 图7（附录）：考察原型数量（ω）对预测LLM性能的影响。
  - 图5：迭代次数对文本质量和TimeXL性能的效应。
- **额外分析**：案例研究（图4、图11）展示多模态推理过程；附录F展示回归任务扩展。
- **评价**：实验覆盖多个领域和任务类型，消融全面，对比方法涵盖当前SOTA，公平性较高。但未提供统计显著性检验（如t检验）或不同随机种子多次重复的结果，可能影响稳定性结论。

## 6. 主要结论与发现
- TimeXL在4个数据集上均取得最佳F1和AUC，最高提升达8.9%（Weather数据集下相对TimeCAP）。
- 多模态原型能够捕获与真实世界条件一致的物理/语义模式（如高湿度+低压→降雨；低需求+库存增加→价格下跌）。
- 迭代反思-精炼机制有效提升文本质量和预测精度，通常在1-2次迭代后饱和。
- 融合预测（编码器+LLM）优于任一组件的单独预测，证实互补性。

## 7. 优点
- **可解释性突出**：原型学习天然提供案例级推理，LLM进一步生成人类可读的解释，符合高风控场景需求。
- **闭环优化设计**：通过反思-精炼循环持续改善文本质量，使模型自适应数据中的噪声和歧义。
- **灵活扩展性**：方法可扩展至回归任务（附录F），且对文本嵌入模型、LLM版本具普适性。
- **实验结果全面**：在气象、金融、医疗三个领域验证，对比方法包括时序、LLM、多模态三大类，消融实验设计合理。

## 8. 不足与局限
- **计算成本**：依赖多个LLM（GPT-4o）在循环中调用，推理与迭代训练开销大，未报告具体成本或延迟。
- **实验可控性**：未提供多次重复实验的标准差或置信区间，可能影响结果可靠性。
- **数据集规模局限**：金融数据集仅1876条记录，医疗数据约数千条，大样本场景下性能未知。
- **理论分析缺失**：缺乏对原型收敛性、迭代稳定性或误差有界的理论保障。
- **LLM作用域**：反思/精炼LLM的反馈依赖训练集批次策略，泛化到全新领域时的迁移能力未验证。
- **消融实验粒度**：未消融每个LLM代理（例如去掉反思代理仅保留精炼），也未量化各正则项的超参数敏感性。

（完）
