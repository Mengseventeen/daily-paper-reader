---
title: Risk Aware Benchmarking of Large Language Models
title_zh: 大型语言模型的风险感知基准测试
authors: "Apoorva Nitsure, Youssef Mroueh, Mattia Rigotti, Kristjan Greenewald, Brian Belgodere, Mikhail Yurochkin, Jiri Navratil, Igor Melnyk, Jarret Ross"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=Mv8y13wfDm"
tags: ["query:ai-finance"]
score: 7.0
evidence: 使用数学金融中的均值-风险模型进行风险感知基准测试
tldr: 本文提出基于分布统计的LLM风险基准框架，利用金融中均值-风险模型的思想，定义每个模型的指标投资组合，通过一阶和二阶随机优势比较，实现考虑风险下的模型选择。为LLM的可靠部署提供金融启发的方法。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1738, \"height\": 545, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 587, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 582, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1040, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1684, \"height\": 657, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1722, \"height\": 1202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1707, \"height\": 1203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1320, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1535, \"height\": 534, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 911, \"height\": 714, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 889, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-mv8y13wfdm/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 891, \"height\": 705, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1781, \"height\": 374, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1774, \"height\": 582, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1778, \"height\": 364, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1779, \"height\": 1174, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 333, \"height\": 895, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 593, \"height\": 935, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1778, \"height\": 1961, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1789, \"height\": 1635, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 632, \"height\": 945, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 604, \"height\": 943, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1756, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-mv8y13wfdm/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1626, \"height\": 228, \"label\": \"Table\"}]"
motivation: 现有LLM基准测试未充分考虑风险。
method: 建立基于随机优势的统计检验，引入均值-风险模型聚合指标，形成模型指标组合。
result: 在多个LLM上验证了风险感知基准的有效性。
conclusion: 将金融组合优化思想引入LLM评估，提高了选择的鲁棒性。
---

## Abstract
We propose a distributional framework for benchmarking socio-technical risks of foundation models with quantified statistical significance. Our approach hinges on a new statistical relative testing based on first and second order stochastic dominance of real random variables. We show that the second order statistics in this test are linked to mean-risk models commonly used in econometrics and mathematical finance to balance risk and utility when choosing between alternatives. Using this framework, we formally develop a risk-aware approach for foundation model selection given guardrails quantified by specified metrics. Inspired by portfolio optimization and selection theory in mathematical finance, we define a metrics portfolio for each model as a means to aggregate a collection of metrics, and perform model selection based on the stochastic dominance of these portfolios. The statistical significance of our tests is backed theoretically by an asymptotic analysis via central limit theorems instantiated in practice via a bootstrap variance estimate. We use our framework to compare various large language models regarding risks related to drifting from instructions and outputting toxic content.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将基于您提供的论文内容，以中文和Markdown格式，对该论文进行结构化、深入、客观的总结。

### **论文总结：Risk Aware Benchmarking of Large Language Models (风险感知的大型语言模型基准测试)**

### 1. 核心问题与整体含义（研究动机与背景）

*   **核心问题：** 现有的LLM评估方法存在三个关键缺陷：
    1.  **缺乏风险感知（Risk Aware）：** 传统的平均指标（如Mean Win Rate）未能充分考虑模型在少数极端情况下的失败风险（如输出有毒内容、偏离指令等尾部风险），这可能导致对高风险模型的高估。
    2.  **多指标聚合困难：** LLM评估通常涉及多个维度（如准确性、鲁棒性、毒性），缺乏一个既能解释多维度结果、又能进行风险感知的聚合度量。
    3.  **缺乏统计显著性检验：** 许多基准测试忽视了结果在统计上的显著性，无法判断模型间的性能差异是否由随机性引起。
*   **整体含义：** 论文旨在建立一个**分布式的、风险感知的、并具有统计显著性的**基准测试框架。该框架将LLM评估类比于金融投资组合的选择，通过**随机优势（Stochastic Dominance）** 这一来自经济学和金融学的概念，来比较不同LLM的“指标投资组合”，从而在考虑风险的前提下进行模型选择。

### 2. 方法论

*   **核心思想：** 将每个LLM的评估视为一个“指标投资组合”，借鉴金融中的**投资组合优化**和**均值-风险模型**，通过比较这些投资组合的**随机优势**（特别是**二阶随机优势SSD**）来选择更优、更鲁棒的模型。
*   **关键技术细节：**
    1.  **指标投资组合（Metrics Portfolio）：**
        *   **目的：** 将多个自动评估指标（如BARTScore, BLEU, 毒性分数等）聚合为一个单一的、可解释的数值。
        *   **方法：** 使用**Copula**函数（特别是**独立Copula**）对每个指标进行归一化（通过CDF转换为[0,1]区间），然后计算加权几何均值。公式为：$R_A(X) = \exp\left(\sum_{i=1}^N \lambda_i \log F_{M_i}(m_i(A(X)))\right)$，其中$F_{M_i}$是对应指标的CDF。
        *   **优势：** 解决了不同指标量纲不一致的问题，并能保留每个样本的评估分布信息。
    2.  **随机优势（Stochastic Dominance）：**
        *   **一阶随机优势（FSD）：** 若模型A的投资组合在**所有百分位数**上都优于模型B，则称A一阶随机优于B。
        *   **二阶随机优势（SSD）：** 更适用于风险感知评估。它关注投资组合的**尾部风险**，通过比较**Tail Value at Risk (TVAR)**（即集成分位数）来判断。一个模型若在SSD上优于另一个，表示它对于**风险厌恶**的决策者来说更优。
        *   **松弛与相对优势：** 由于完美的一/二阶随机优势难以严格满足，论文提出了：
            *   **ε-随机优势（Almost SD）：** 允许一个小的“违反区域”，通过计算违反比例（violation ratio）来衡量。
            *   **相对随机优势（Relative SD / R-FSD & R-SSD）：** 通过比较每个模型相对于所有其他模型的平均违反比例（one-versus-all violation ratio）来建立模型间的**相对排序**，避免了设置绝对阈值（ε）的困难。核心统计量为：$\Delta \epsilon_{ij}^{(\ell)} = \epsilon_i^{(\ell)} - \epsilon_j^{(\ell)}$，若该值小于0，则模型i优于模型j。
    3.  **统计显著性检验：**
        *   论文证明了上述违反比例统计量的**渐近正态性**（通过中心极限定理），从而可以构建**假设检验**。
        *   使用**Bootstrap（自助法）** 估计方差，并用于计算置信区间。
        *   采用**Bonferroni校正**处理多重比较问题，并用**Borda算法**聚合所有成对比较的结果，得到一个全局排序。
*   **算法流程（简要）：**
    1.  为每个模型构建指标投资组合（IC或EC）。
    2.  对所有模型对，计算R-FSD和R-SSD的违反比例统计量。
    3.  通过Bootstrap估计统计量的方差。
    4.  进行Bonferroni校正后的假设检验。
    5.  使用Borda算法将成对比较结果整合成最终排名。

### 3. 实验设计

*   **数据集/场景：**
    1.  **Mix-Instruct (指令遵循风险)：** 使用来自Jiang et al. (2023)的5K个测试样本。评估8个自动指标（如BARTScore, BLEU），以及使用ChatGPT评估作为人类评价的代理。
    2.  **Toxicity (有毒内容风险)：** 使用RealToxicityPrompts (Gehman et al., 2020)数据集。评估6个Perspective API指标（毒性、严重毒性、身份攻击等）。使用有毒提示和非有毒提示两种场景，并区分“仅生成（Gen Only）”和“提示+生成（Prompt+Gen）”两种评估粒度。
*   **基准测试（Benchmark）：**
    *   方法对比：将提出的**R-FSD, R-SSD** 方法与传统的**平均胜率（MWR）** 和**均值-风险模型**进行对比。
    *   聚合方式对比：比较**独立Copula（IC）** 和**经验Copula（EC）** 两种投资组合聚合方式，以及“投资组合式评估（@P）”和“按指标评估后排名聚合（RA）”两种排名策略。
*   **对比方法：**
    *   Mean Win Rate (MWR)
    *   ε-FSD (近似于一阶随机优势）
    *   ε-SSD (近似于二阶随机优势）
    *   Mean-Risk Models (如Mean-Gini Tail, Mean-nTvAR)
    *   ChatGPT Score (作为人类代理)

### 4. 资源与算力

*   论文**未明确说明**训练LLM所需的算力（GPU型号、数量、训练时间等）。
*   论文在“高效实现”一节只比较了**评估过程**的计算开销：
    *   **提出的方法：** 在128核CPU（仅使用2核）上，使用1,000次Bootstrap，执行所有测试平均耗时**17.7秒**。
    *   **现有方法（deepsig）：** 在执行类似任务（ε=0.25，仅3次Bootstrap）时，耗时**15分50秒**。
    *   **Copula计算：** 独立Copula (IC) 需要0.87秒，而经验Copula (EC) 在处理5K样本时需要约1.5小时。

### 5. 实验数量与充分性

*   **实验数量：** 论文在两个任务（指令遵循、毒性）上进行了多种场景、多种指标、多种方法的对比实验，包括：
    *   **主要结果：** 展示不同方法在Mix-Instruct和Toxicity任务上的最终排名（表2，表4-10）。
    *   **稳定性分析：** 在不同样本量下（从100到5000），测量排名与渐近排名的一致性（Kendall-Tau相似度）。
    *   **与人类代理的对齐：** 计算不同方法与ChatGPT评分的排名相似度。
    *   **消融研究：** 对比独立Copula与经验Copula、投资组合式评估与按指标聚合等不同变体的效果。
    *   **合成数据验证：** 使用高斯分布和对数正态分布验证统计测试的效力（True Positive Rate）随样本量的变化。
*   **充分性与公平性：**
    *   **充分性：** 实验设计较为全面，覆盖了方法验证、稳定性测试、与人类代理的对齐以及对不同聚合方式的消融分析，能够有力地支撑其结论。
    *   **公平性：** 将提出方法与当前主流的MWR基线进行了对比，并揭示了其缺陷。实验结果客观地展示了提出的R-SSD方法在风险感知排名上的优势，同时也承认了不同方法的局限性（如EC计算量大但与人更对齐）。在“统计显著性”部分，比较了与现有工具的计算效率，体现了方法的实用性。因此，实验评估是相对客观和公平的。

### 6. 主要结论与发现

1.  **二阶随机优势（SSD）优于一阶随机优势（FSD）：** 在LLM评估中，单纯比较均值或完整分位数（FSD）无法清晰区分模型。SSD通过关注尾部风险（TVAR），能更有效地识别并排序模型，尤其是对风险模型（如Flan-T5）进行惩罚。
2.  **指标投资组合有效：** 基于Copula聚合的指标投资组合结果（@P）与基于ChatGPT的人类评价代理排名高度相似，证明了自动指标聚合方法的有效性。
3.  **MWR风险高：** 传统的Mean Win Rate由于忽略尾部事件，会高估高风险模型（如Flan-T5在MWR中排名第6，但在所有其他合理排名中几乎垫底），因此在风险敏感的基准测试中应谨慎使用。
4.  **统计显著性至关重要：** 论文提出的基于CLT和Bootstrap的假设检验框架为模型对比提供了可靠的理论基础，避免了随机噪声导致的误判。
5.  **独立Copula (IC) vs. 经验Copula (EC)：** IC计算效率高且渐近表现好；EC能更好地捕捉指标间的依赖关系，更接近人类评估，但计算成本高昂。

### 7. 优点

1.  **创新性强：** 首次将金融领域的**投资组合理论**和**随机优势**系统性地引入LLM基准测试，为多指标、风险感知的模型评估提供了一个全新的理论框架。
2.  **理论与实践的紧密结合：** 提出的方法不仅有扎实的数学基础（CLT证明、渐近正态性），还提供了高效的工程实现（Bootstrap、向量化计算），便于实际应用。
3.  **直指要害：** 针对当前LLM基准测试中普遍存在的“平均主义”和“忽视尾部风险”的问题，给出了明确的解决方案和警示（如对MWR的批判）。
4.  **提供了清晰的模型选择依据：** SSD的排序不仅给出了排名，还隐含了对模型风险水平的度量，为决策者（特别是在风险厌恶场景下）提供了更明智的选择。
5.  **统计严谨性：** 明确提出了统计显著性检验的要求和方法，提升了LLM评估的科学性和可信度。

### 8. 不足与局限

1.  **依赖于指标选择：** 框架的有效性最终依赖于所选自动评估指标与人类判断的对齐程度。如果使用的指标本身就存在偏差，聚合后的结果也可能存在偏差。
2.  **经验Copula的可扩展性：** 经验Copula方法计算复杂度高（O(n²N)），不适合大规模评估，实际应用中主要推荐使用独立的Copula。
3.  **训练成本未被考虑：** 论文聚焦于**评估**的统计方法，没有提及训练LLM的计算成本或碳排放，未解决选择环境可持续模型的问题。
4.  **应用范围有限：** 实验主要针对“指令遵循”和“毒性”两个风险维度。方法的通用性在其他风险维度（如公平性、安全性等）以及不同领域（如代码生成、图像生成）的表现有待进一步验证。
5.  **依赖样本量：** 虽然证明了渐近性质，但在小样本量下（<500），R-SSD排名的稳定性依然较低，这对于成本高昂或样本稀少的评估场景（如医疗、法律）构成挑战。

（完）
