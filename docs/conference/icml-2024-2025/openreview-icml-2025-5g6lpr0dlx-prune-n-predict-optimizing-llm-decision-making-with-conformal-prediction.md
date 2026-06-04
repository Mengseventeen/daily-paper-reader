---
title: "Prune 'n Predict: Optimizing LLM Decision-making with Conformal Prediction"
title_zh: 剪枝预测：用共形预测优化大语言模型决策
authors: "Harit Vishwakarma, Alan Mishler, Thomas Cook, Niccolo Dalmasso, Natraj Raman, Sumitra Ganesh"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=5g6LPR0Dlx"
tags: ["query:ai-finance"]
score: 5.0
evidence: 共形预测用于金融等高风险领域的LLM决策
tldr: 大语言模型在高风险领域（如金融、医疗）中可能产生错误输出带来风险。本文利用共形预测生成包含正确答案的高概率预测集，并提出CROQ方法通过缩小选项范围重新提问来提高准确率。实验表明该方法显著降低错误率，增强了LLM在金融决策中的可靠性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 729, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1451, \"height\": 684, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1552, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1593, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1595, \"height\": 801, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1768, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1767, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1772, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1776, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1775, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1774, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1772, \"height\": 516, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1771, \"height\": 511, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5g6lpr0dlx/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1769, \"height\": 507, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1564, \"height\": 569, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1573, \"height\": 585, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1574, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1052, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1430, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1567, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1563, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1568, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 985, \"height\": 1234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1432, \"height\": 1119, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1563, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1564, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1511, \"height\": 377, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1346, \"height\": 1049, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 983, \"height\": 1235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 984, \"height\": 1235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1462, \"height\": 1144, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1565, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1541, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1484, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1770, \"height\": 186, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5g6lpr0dlx/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1104, \"height\": 1542, \"label\": \"Table\"}]"
motivation: LLM在金融等高风险领域可能产生错误输出，需量化不确定性。
method: 采用共形预测生成预测集，并通过CROQ方法修订问题提高决策准确性。
result: 显著减少了LLM在多项选择等任务中的错误。
conclusion: 该方法为金融等领域的可靠LLM应用提供了实用的不确定性量化框架。
---

## Abstract
Large language models (LLMs) are empowering decision-making in several applications, including tool or API usage and answering multiple-choice questions (MCQs). However, incorrect outputs pose significant risks in high-stakes domains like healthcare and finance. To quantify LLM uncertainty and thereby mitigate these risks, recent works employ conformal prediction (CP), a model- and distribution-agnostic framework that uses LLM outputs to generate a \emph{prediction set} containing the true answer with high probability. Leveraging CP, we propose \emph{conformal revision of questions} (CROQ), which revises the question by narrowing down the available choices to those in the prediction set and asking the LLM the revised question. We expect LLMs to be more accurate on revised questions with fewer choices. Furthermore, we expect CROQ to be effective when the prediction sets from CP are small. Commonly used logit scores often lead to large sets, diminishing CROQ's effectiveness. To overcome this, we propose CP-OPT, an optimization framework to learn scores that minimize set sizes while maintaining coverage. Our extensive experiments on MMLU,  ToolAlpaca, and TruthfulQA datasets with multiple LLMs show that CROQ improves accuracy over the standard inference, with more pronounced gains when paired with CP-OPT.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

大语言模型（LLM）在多种决策任务中表现出色，例如工具/API调用、多项选择题（MCQ）回答等。然而，LLM经常出现过度自信的错误输出，这在高风险领域（如医疗、金融）中构成显著风险。为量化LLM的不确定性并降低风险，已有研究采用共形预测（Conformal Prediction, CP）——一种模型无关、分布无关的框架，利用LLM输出生成一个以高概率包含正确答案的“预测集”。本文在此基础上提出两个核心贡献：一是利用CP的预测集来修剪错误选项，从而改进LLM的准确性；二是优化CP的得分函数以减小预测集大小，进一步提高效果。

## 2. 论文提出的方法论

### 2.1 核心思想
- 受人类考试中“排除法”启发：减少多选题中的干扰项可以提高正确率。论文首先通过实验验证了“选项越少，LLM准确率越高”的单调关系。
- 利用共形预测产生的预测集（高概率包含正确答案）来修剪掉部分干扰项，得到修订后的问题（更少选项），再让LLM回答修订后的问题。该方法称为**Conformal Revision of Questions (CROQ)**。

### 2.2 关键技术细节
- **CROQ流程**：
  1. 固定一个得分函数 \(g\)（如LLM的logits或本文提出的CP-OPT得分），在标定集上通过分割共形预测（Split Conformal Prediction）得到阈值 \(\hat{\tau}_\alpha\)，满足边际覆盖率 \(\ge 1-\alpha\)。
  2. 对于测试问题，构造预测集 \(C(x; g, \hat{\tau}_\alpha) = \{y: g(x,y) \ge \hat{\tau}_\alpha\}\)。
  3. 若预测集大小为1或等于原始选项数，则直接使用LLM原始答案；否则将问题修订为只包含预测集中的选项（重新编号），然后让LLM回答修订后的问题。
- **CP-OPT得分优化**：
  - 目标：最小化期望预测集大小，同时保持覆盖率 \(\ge 1-\alpha\)。
  - 使用可微的sigmoid近似替换指示函数，并通过惩罚项将覆盖约束转化为无约束优化。
  - 在学习一个3层神经网络作为得分函数 \(g\)，输入为LLM最后一层隐藏表示和logits的拼接。
  - 在训练集上优化，然后使用独立的标定集重新计算阈值（避免过拟合偏差）。

### 2.3 公式与算法流程（文字说明）
- 优化问题（P2）：\(\min_{g,\tau} \tilde{S}(g,\tau) + \lambda (\tilde{P}(g,\tau) - 1 + \alpha)^2 - \hat{C}(g) + \lambda_1 \|g\|_2^2\)，其中 \(\tilde{S}\) 是平均集大小的sigmoid近似，\(\tilde{P}\) 是覆盖率的sigmoid近似，\(\hat{C}\) 是交叉熵项。
- 使用随机梯度下降求解。

## 3. 实验设计

### 3.1 数据集与场景
- **MMLU**：57个领域，标准4选项，另构造10、15选项版本。
- **TruthfulQA**：评估真实性，原始MCQ形式，构造4、10、15选项版本。
- **ToolAlpaca**：工具选择任务，构造4、10、15选项。
- 额外在MMLU-Pro（10选项）和NL2SQL（表选择）上做了扩展实验。

### 3.2 Benchmark
- 对比方法：标准单次推理（不修剪选项）作为baseline。
- 对比得分函数：
  - LLM Logits（softmax）。
  - CP-OPT（本文方法）。
- 未对比自一致性得分（Su et al., 2024），因其计算成本过高。

### 3.3 模型
- Llama-3-8B-Instruct
- Phi-3-4k-mini-Instruct
- gemma-2-9b-it-SimPO（简称Gemma-2）

### 3.4 主要评价指标
- 平均预测集大小、覆盖率（目标95%）
- CROQ前后的准确率，统计显著性（配对t检验，\(\alpha=0.05\)）

## 4. 资源与算力

论文未明确说明使用的GPU型号、数量或训练时长。仅提到使用了开源的小型至中型模型（8B和9B参数），优化过程为后处理（post-hoc），训练时间相对可控。但具体硬件配置未列出。

## 5. 实验数量与充分性

- **实验组数**：主实验涉及3个数据集 × 3种选项数 × 3个模型 = 27个设置，每种设置都报告了平均集大小、覆盖率、CROQ准确率。
- **额外实验**：MMLU-Pro（1个设置）、NL2SQL应用（3种方法对比）、不同α值（覆盖率）的权衡分析（图4、5）、基于集大小的条件准确率分析（附录多张表格）。
- **消融与敏感性分析**：对超参数λ、学习率等进行了调优报告（附录表21）。
- **公平性**：统计显著性标注；所有实验使用零样本提示；数据集划分独立；标定集与测试集不重叠。
- **充分性评价**：实验覆盖了多种模型、多种选项数、多个数据集，并验证了单调性假设，结论较为稳健。但未在更大模型（如70B、GPT-4）上验证，可能影响泛化性。

## 6. 主要结论与发现

- **H1（CP-OPT减小集大小）**：在27个设置中，17个显著减小集大小，6个同时伴随覆盖率下降（但多数仍高于95%），剩余4个无显著差异。CP-OPT使集大小分布向更小偏移。
- **H2（CROQ提高准确率）**：使用logits时，19/27设置准确率提升（9个显著）；使用CP-OPT时，24/27设置提升（13个显著）。最大提升达7.24%（ToolAlpaca 15选项，Llama-3）。
- **H3（CROQ+CP-OPT优于CROQ+logits）**：22/27设置中CP-OPT带来更高准确率（12个显著），最大提升4.56%（TruthfulQA 15选项，Phi-3）。
- **α-准确率权衡**：存在最优覆盖率参数（约α=0.1~0.2），过小（高覆盖）则修剪不足，过大（低覆盖）则过多丢失正确答案。
- **应用扩展**：在NL2SQL表选择任务中，CROQ+CP-OPT较包含所有表减少45% token成本，且准确率略高。

## 7. 优点

- **方法的通用性**：CROQ不依赖于特定LLM或API，得分函数可来自不同模型或非LLM来源（如嵌入相似性），适用于多轮修剪甚至模型级联。
- **理论保证**：共形预测提供边际覆盖率保证，且CP-OPT优化后仍保持该保证。
- **简单有效**：无需重新训练LLM，仅需后处理优化一个轻量网络，计算开销低。
- **实验设计细致**：验证了选项数与准确率的单调关系，分析了不同α的影响，并进行了条件准确率分析（按集大小分层）。
- **实用性**：在真实应用（NL2SQL）中展示了成本降低和准确率提升。

## 8. 不足与局限

- **实验覆盖有限**：仅使用小型至中型开源模型（8B/9B），未测试更大模型（如GPT-4、Llama-70B）或闭源API（如GPT-4o）。对于闭源模型，若logits不可用，本文方法无法直接应用（需借助其他得分函数）。
- **边际覆盖率仅保证整体**：不同子群（如不同问题难度）的覆盖率可能低于95%，论文未做条件覆盖率分析。
- **多轮CROQ未实现**：论文仅讨论了两轮（一次修剪），理论上多轮迭代可进一步提升，但存在校准复杂度和计算成本增加的问题（作者在展望中提及）。
- **假设的局限性**：单调性假设（选项越少准确率越高）在大部分情况成立，但可能存在反转（如删除关键干扰项后模型反而困惑），论文未深入探讨。
- **优化稳定性**：CP-OPT使用sigmoid近似和随机梯度下降，超参数（λ、学习率）需针对每个数据集-模型组合调整，调参成本较高。
- **计算资源未报告**：缺少训练CP-OPT网络的具体硬件和耗时，难以复现成本。

（完）
