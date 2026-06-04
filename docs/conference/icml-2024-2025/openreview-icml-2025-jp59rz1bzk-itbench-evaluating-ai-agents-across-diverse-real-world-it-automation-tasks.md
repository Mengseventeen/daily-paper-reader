---
title: "ITBench: Evaluating AI Agents across Diverse Real-World IT Automation Tasks"
title_zh: ITBench：跨多样化真实世界IT自动化任务评估AI智能体
authors: "Saurabh Jha, Rohan R. Arora, Yuji Watanabe, Takumi Yanagawa, Yinfang Chen, Jackson Clark, Bhavya Bhavya, Mudit Verma, Harshit Kumar, Hirokuni Kitahara, Noah Zheutlin, Saki Takano, Divya Pathak, Felix George, Xinbo Wu, Bekir O Turkkan, Gerard Vanloo, Michael Nidd, Ting Dai, Oishik Chatterjee, Pranjal Gupta, Suranjana Samanta, Pooja Aggarwal, Rong Lee, Jae-wook Ahn, Debanjana Kar, Amit Paradkar, Yu Deng, Pratibha Moogi, Prateeti Mohapatra, Naoki Abe, Chandrasekhar Narayanaswami, Tianyin Xu, Lav R. Varshney, Ruchi Mahindru, Anca Sailer, Laura Shwartz, Daby Sow, Nicholas C. M. Fuller, Ruchir Puri"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=jP59rz1bZk"
tags: ["query:ai-finance"]
score: 6.0
evidence: ITBench包含FinOps场景，展示AI智能体在财务运营中的应用
tldr: 为实现AI智能体自动化IT任务，提出ITBench框架，初始发布覆盖站点可靠性工程、合规安全运营和财务运营（FinOps）三大领域，包含102个真实场景。提供一键式工作流和可解释指标，易扩展。实验显示当前AI智能体在FinOps等任务上仍有挑战。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1358, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 854, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1736, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1726, \"height\": 633, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 860, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1781, \"height\": 1040, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1669, \"height\": 1176, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 551, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1419, \"height\": 640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1749, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 385, \"height\": 278, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 857, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 860, \"height\": 680, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 683, \"height\": 1170, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 679, \"height\": 718, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1745, \"height\": 1896, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1755, \"height\": 1940, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1755, \"height\": 1914, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1746, \"height\": 1898, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1696, \"height\": 1007, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1535, \"height\": 824, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1706, \"height\": 876, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1399, \"height\": 686, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 385, \"height\": 280, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1446, \"height\": 853, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 683, \"height\": 2019, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 687, \"height\": 1765, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1763, \"height\": 2364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 684, \"height\": 1200, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jp59rz1bzk/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 702, \"height\": 394, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1808, \"height\": 445, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 962, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 869, \"height\": 676, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1728, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1759, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1481, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 774, \"height\": 581, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 851, \"height\": 532, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1762, \"height\": 1521, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1753, \"height\": 407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1769, \"height\": 620, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1705, \"height\": 1013, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1452, \"height\": 713, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 790, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1477, \"height\": 669, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 558, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1254, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 995, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1005, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1780, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1815, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1784, \"height\": 1070, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1807, \"height\": 2048, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 859, \"height\": 588, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1470, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1842, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1786, \"height\": 886, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1784, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1771, \"height\": 954, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1769, \"height\": 1029, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1763, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 851, \"height\": 256, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1752, \"height\": 404, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jp59rz1bzk/table-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 795, \"height\": 639, \"label\": \"Table\"}]"
motivation: 需要系统性基准评估AI智能体在IT自动化（含财务运营）中的效果。
method: 设计可扩展的基准框架，包含真实场景和标准化评估指标。
result: 初始102个场景，三个重点领域，支持社区扩展。
conclusion: 为AI智能体在IT自动化（包括财务运营）提供评测基础。
---

## Abstract
Realizing the vision of using AI agents to automate critical IT tasks depends on the ability to measure and understand effectiveness of proposed solutions. We introduce ITBench, a framework that offers a systematic methodology for benchmarking AI agents to address real-world IT automation tasks. Our initial release targets three key areas: Site Reliability Engineering (SRE), Compliance and Security Operations (CISO), and Financial Operations (FinOps). The design enables AI researchers to understand the challenges and opportunities of AI agents for IT automation with push-button workflows and interpretable metrics. IT-Bench includes an initial set of 102 real-world scenarios, which can be easily extended by community contributions. Our results show that agents powered by state-of-the-art models resolve only 11.4% of SRE scenarios, 25.2% of CISO scenarios, and 25.8% of FinOps scenarios (excluding anomaly detection). For FinOps-specific anomaly detection (AD) scenarios, AI agents achieve an F1 score of 0.35. We expect ITBench to be a key enabler of AI-driven IT automation that is correct, safe, and fast. IT-Bench, along with a leaderboard and sample agent implementations, is available at https://github.com/ibm/itbench.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **背景**：现代IT系统高度复杂（云原生、微服务），故障频发（如CrowdStrike事件损失54亿美元）。SRE、CISO、FinOps等角色面临日益严峻的管理挑战，亟需AI agent自动化IT任务。
- **问题**：缺乏系统性、可复现的基准来评估AI agent在真实IT任务中的效果，现有基准（TrainTicket、AIOpsLab、InsightBench等）覆盖面窄、缺乏自动化评估和真实环境。
- **整体意义**：ITBench首次提出全面、开放、可扩展的基准框架，覆盖SRE（站点可靠性工程）、CISO（合规与安全运营）、FinOps（财务运营）三大关键领域，旨在推动AI agent在IT自动化中的正确、安全、高效部署。

## 2. 论文提出的方法论
- **核心思想**：将IT自动化任务形式化为场景（scenario），每个场景定义为 `<M, E, T, D>` 四元组（元数据、环境、触发事件、预期结果）。agent与环境构成部分可观测马尔可夫决策过程（POMDP），agent通过工具与环境交互。
- **关键技术细节**：
  - **场景规范**：包括名称、描述、领域（SRE/CISO/FinOps）、复杂度（Easy/Medium/Hard）、ground truth等元数据。
  - **AI agent架构**：使用ReAct（推理-行动循环）、反思（错误自我纠正）、分解（分离推理与观察）等机制。每个领域配备专用工具集：
    - SRE/FinOps: NL2Kubectl、NL2Traces、NL2Metrics、NL2Logs、NL2Alerts、Mitigation等。
    - CISO: 生成Kyverno/OPA Rego策略、生成playbook、运行kubectl/playbook等。
  - **评估指标**：
    - SRE: pass@1（诊断/缓解）、NTAM（归一化拓扑感知匹配，用于故障定位和传播链）、MTTD/MTTR。
    - CISO: pass@1、TTP（处理时间）。
    - FinOps: pass@1、F1分数、排名分数、token利用率、资源效率接近度。
  - **leaderboard**：支持API/UI，提供自动化环境部署、注入故障、评估、清理全流程。
- **公式与算法流程**（文字说明）：
  - agent决策：`a_t = f(o_t | past observations, past actions)`
  - 环境转移：`s_t = g(s_{t-1}, a_{t-1})`
  - 观测：`o_t = h(s_t)`
  - 停止时间：`t* = min{t | a_t = ⊥}`
  - 成功率：`E_{p~π}[I(g(s_{t*}, ...) = s_G)]`

## 3. 实验设计
- **数据集/场景**：
  - **SRE**：42个场景（21个种子场景×2种观测配置：有/无追踪），源自真实SaaS产品故障，涉及缓存故障、高CPU、破损镜像等，复杂度：Easy 24%、Medium 52%、Hard 24%。
  - **CISO**：50个场景，基于CIS基准（Kubernetes、RHEL9），分为4个类：Kyverno（Easy）、k8s-opa（Medium）、rhel-opa（Medium）、kyverno-update（Hard）。
  - **FinOps**：10个场景，包括告警驱动（预算超支、自动伸缩误配置）、数据洞察（6个KPI查询）、异常检测（2个AD场景）。复杂度：Easy 20%、Medium 30%、Hard 50%。
- **基准方法**：
  - 对比8种LLM：GPT-4o、Llama-3.3-70B-instruct、Llama-3.1-8B-instruct、Granite-3.1-8B-instruct（自然语言）；GPT-4o-mini、Llama-3.1-405B-instruct、Mixtral-8x7B-instruct、Mistral-Large-2（代码生成）。
  - 所有模型使用128K上下文窗口，温度=0，top_p=1e-7，greedy解码。
- **评估方式**：
  - SRE：每场景10次独立运行；CISO：每场景8次；FinOps：数据洞察固定温度=0（零方差），AD和告警场景多次运行。
  - 统计标准误差。

## 4. 资源与算力
- 文中未明确给出GPU型号、数量或训练时长（因仅进行LLM推理，未涉及训练）。
- 推理硬件：主要使用AWS EC2 m4.xlarge实例（1 control-plane + 3 worker节点，各12核48GB RAM）。也支持Kind集群在消费级笔记本上运行（Intel Xeon Gold 6248，12核16GB RAM）。
- FinOps数据洞察使用的LLM推理耗时为token计数（如GPT-4o平均6232 tokens/场景），但未给出总体GPU小时数。

## 5. 实验数量与充分性
- **实验数量**：
  - SRE：42场景 × 10 runs × 4 models = 1680 trials（实际完成率>98.7%）。
  - CISO：50场景 × 8 runs × 8 models = 3200 trials（完成率>90%）。
  - FinOps：告警驱动2场景（多次运行），数据洞察6场景 × 4 models（每场景10次），AD 2场景 × 4 models。
- **充分性评价**：
  - **充分**：覆盖多模型、多复杂度、有/无追踪消融、失败案例分析（工具使用、推理路径）。指标全面（pass@1、NTAM、MTTD/MTTR、F1、排名分数等）。
  - **客观性**：使用固定种子和超参数，统计标准误差。但CISO和FinOps场景数偏少（尤其FinOps告警驱动仅2场景）。
  - **局限性**：未进行LLM微调对比；部分场景（FinOps Hard）所有模型均失败，缺乏区分度。

## 6. 主要结论与发现
- **整体性能低下**：GPT-4o表现最好，但SRE诊断pass@1仅13.81%，缓解11.43%；CISO pass@1为25.19%；FinOps告警诊断33%，AD F1=0.6。说明当前SOTA agent在真实IT任务中远未达到实用水平。
- **复杂度影响**：所有模型在Hard场景上成功率极低（SRE缓解Hard场景为0%；CISO kyverno-update类最高仅17.74%）。
- **追踪是关键**：SRE场景移除追踪后，GPT-4o诊断率从18.1%降至9.52%，缓解率从20%降至2.86%。
- **诊断与缓解非严格依赖**：某些场景agent误诊但成功缓解（如通用缩放操作），反之亦然（诊断准确但无法缓解）。
- **推理缺陷**：agent过度依赖NL2Kubectl，小模型频繁产生无效调用，成功推理路径更集中（少绕路、高覆盖）。
- **CISO发现**：GPT-4o在Easy类（Kyverno）表现突出（pass@1=40.28%），但Hard类（kyverno-update）仅17.74%；代码生成模型（GPT-4o-mini）在OPA Rego上优于GPT-4o。
- **FinOps发现**：数据洞察场景中，大模型理解SQL查询更好；但多步骤聚合场景（如方差计算）全部失败；AD中GPT-4o F1=0.6，Llama-3.3-70B因误解query得分为0。

## 7. 优点
- **真实性**：SRE场景源于实际SaaS产品事故，CISO基于行业标准CIS基准，FinOps基于FinOps基金会KPI，具有高度代表性和实践价值。
- **开放可扩展**：完全开源（GitHub），允许社区添加新场景和新领域；使用标准技术栈（Kubernetes、Ansible、OpenTelemetry等）。
- **自动化评估**：提供一键部署、故障注入、清理、评估流水线，支持部分评分（如NTAM指标区分部分正确）。
- **可解释性**：通过NTAM指标和轨迹分析量化agent推理质量（绕路节点数、覆盖比例），揭示失败模式。
- **安全防护**：容器化agent环境，限制危险命令执行。
- **多领域覆盖**：首次在同一框架下统一评估SRE、CISO、FinOps三大角色任务。

## 8. 不足与局限
- **场景数量有限**：目前仅102场景，FinOps仅10个（含2个告警驱动、6个数据洞察、2个AD），Hard场景过少，可能导致统计方差大。
- **未覆盖全部IT任务**：缺少预防性任务（如容量规划）、威胁分析、DevOps流程等，agent仅处理反应式问题。
- **LLM依赖风险**：未考虑微调或领域定制，且agent可能产生危险命令（如`kubectl delete node`），虽有防护但未完全消除。
- **评估指标局限**：自然语言输出（如故障条件描述）未自动评测（计划用LLM-as-judge未实现）；FinOps部分指标（如模型token利用率）仅报告平均，未深入分析。
- **实验条件简化**：FinOps数据洞察使用固定数据集（零方差），但真实场景数据动态变化；FinOps告警驱动场景仅2个，结论泛化性存疑。
- **硬件资源不明确**：未报告具体GPU型号和总计算时间，不利于复现和能耗评估。
- **偏差风险**：SRE场景源自同一组织（IBM）的内部事故，可能存在领域偏见；CISO仅基于CIS标准，未覆盖其他合规框架（如NIST、GDPR）。

（完）
