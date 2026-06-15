# Semantic Query Optimization Paper List

> Continuously updated paper list on **Semantic Query Optimization**, covering SQL query rewriting, NL2SQL / Text-to-SQL, query equivalence, and LLM-based query optimization.
>
> Kindly let us know if we have missed any great papers. PRs are welcome!
>
> Inspired by [AIDB](https://github.com/TsinghuaDatabaseGroup/AIDB) from Tsinghua Database Group.

---

# Table of Contents

- [0. Survey and Tutorial](#0-survey-and-tutorial)
- [1. SQL Query Rewriting](#1-sql-query-rewriting)
  - [1.1 Rule-based Rewriting](#11-rule-based-rewriting)
  - [1.2 Learning-based Rewriting](#12-learning-based-rewriting)
  - [1.3 LLM-based Rewriting](#13-llm-based-rewriting)
  - [1.4 Query Equivalence Verification](#14-query-equivalence-verification)
- [2. NL2SQL / Text-to-SQL](#2-nl2sql--text-to-sql)
  - [2.1 Datasets and Benchmarks](#21-datasets-and-benchmarks)
  - [2.2 Prompt-based Methods](#22-prompt-based-methods)
  - [2.3 Fine-tuning Methods](#23-fine-tuning-methods)
  - [2.4 Agent-based Methods](#24-agent-based-methods)
- [3. Semantic Operators over Unstructured Data](#3-semantic-operators-over-unstructured-data)
- [4. Cardinality and Cost Estimation](#4-cardinality-and-cost-estimation)
- [5. Plan Optimization](#5-plan-optimization)

---

## 0. Survey and Tutorial

**A Survey on Advancing the DBMS Query Optimizer: Cardinality Estimation, Cost Model, and Plan Enumeration.** ![](https://img.shields.io/badge/-learned_optimizer-orange)

*Hai Lan, Zhifeng Bao, Yuwei Peng. Data Science and Engineering, 2021.* [[paper](https://link.springer.com/article/10.1007/s41019-020-00149-7)]

**Database Meets Artificial Intelligence: A Survey.** ![](https://img.shields.io/badge/-ai4db-Informational) ![](https://img.shields.io/badge/-db4ai-informational)

*Xuanhe Zhou, Chengliang Chai, Guoliang Li, et al. TKDE, 2020.* [[paper](http://dbgroup.cs.tsinghua.edu.cn/ligl/papers/aidb.pdf)]

**Natural Language to SQL: State of the Art and Open Problems.** ![](https://img.shields.io/badge/-nl2sql-blue)

*Yuyu Luo, Nan Tang, Guoliang Li, et al. VLDB, 2025.* [[paper](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/VLDB25-NL2SQL.pdf)]

**A Survey of Text-to-SQL in the Era of LLMs: Where are we, and where are we going?** ![](https://img.shields.io/badge/-nl2sql-blue) ![](https://img.shields.io/badge/-llm-f5f5dc)

*Xinyu Liu et al. arXiv, 2024.* [[paper](https://arxiv.org/abs/2408.05109)]

**A Survey of Query Optimization in Large Language Models.** ![](https://img.shields.io/badge/-llm4db-Informational)

*arXiv, 2024.* [[paper](https://arxiv.org/abs/2412.17558)]

**Learned Query Optimizer: At the Forefront of AI-Driven Databases.** ![](https://img.shields.io/badge/-learned_optimizer-orange)

*Zhu, Rong, Ziniu Wu, Chengliang Chai, et al. EDBT, 2022.* [[paper](https://openproceedings.org/2022/conf/edbt/tutorial-1.pdf)]

---

## 1. SQL Query Rewriting

### 1.1 Rule-based Rewriting

**Extensible/rule-based query rewrite optimization in Starburst.** ![](https://img.shields.io/badge/-rule_based-green)

*H. Pirahesh, J. M. Hellerstein, W. Hasan. SIGMOD, 1992.* [[paper](https://dl.acm.org/doi/10.1145/130283.130294)]

**A rule-based query rewriter in an extensible DBMS.** ![](https://img.shields.io/badge/-rule_based-green)

*Beatrice Finance, Georges Gardarin. ICDE, 1991.* [[paper](https://ieeexplore.ieee.org/document/131472)]

**Optimization of Common Table Expressions in MPP Database Systems.** ![](https://img.shields.io/badge/-rule_based-green)

*Amr El-Helw, Venkatesh Raghavan, et al. VLDB, 2015.* [[paper](http://www.vldb.org/pvldb/vol8/p1704-el-helw.pdf)]

---

### 1.2 Learning-based Rewriting

**LearnedRewrite: A Learned Query Rewrite System using Monte Carlo Tree Search.** ![](https://img.shields.io/badge/-MCTS-yellowgreen) ![](https://img.shields.io/badge/-cost_model-orange)

*Zhou, Xuanhe, et al. VLDB, 2022.* [[paper](https://dl.acm.org/doi/10.14778/3611540.3611633)]

**WeTune: Automatic Discovery and Verification of Query Rewrite Rules.** ![](https://img.shields.io/badge/-rule_discovery-yellowgreen) ![](https://img.shields.io/badge/-formal_verification-purple)

*Zhaoguo Wang, Zhonglin Zhou, Yicun Yang, et al. SIGMOD, 2022.* [[paper](https://dl.acm.org/doi/10.1145/3514221.3517843)] [[code](https://github.com/WeTune/WeTune-code)]

**SlabCity: Whole-Query Optimization using Program Synthesis.** ![](https://img.shields.io/badge/-program_synthesis-purple)

*Rui Dong, Jie Liu, Yuxuan Zhu, Cong Yan, Barzan Mozafari, Xinyu Wang. VLDB, 2023.* [[paper](https://dl.acm.org/doi/10.14778/3611540.3611583)]

**QueryBooster: Improving SQL Performance Using Middleware Services for Human-Centered Query Rewriting.** ![](https://img.shields.io/badge/-human_in_the_loop-yellowgreen)

*Qiushi Bai, Sadeem Alsudais, Chen Li. VLDB, 2023.* [[paper](https://dl.acm.org/doi/10.14778/3587136.3587140)]

**Efficient Query Rewrite Rule Discovery via Standardized Enumeration and Learning-to-Rank.** ![](https://img.shields.io/badge/-rule_discovery-yellowgreen)

*arXiv, 2026.* [[paper](https://arxiv.org/abs/2602.00000)]

---

### 1.3 LLM-based Rewriting

**LLM-R2: A Large Language Model Enhanced Rule-based Rewrite System for Boosting Query Efficiency.** ![](https://img.shields.io/badge/-llm-f5f5dc) ![](https://img.shields.io/badge/-rule_retrieval-yellowgreen)

*Zhaodonghui Li, Haitao Yuan, Huiming Wang, Gao Cong, Lidong Bing. VLDB, 2024.* [[paper](https://dl.acm.org/doi/10.14778/3617838.3617840)]

**R-Bot: An LLM-based Query Rewrite System.** ![](https://img.shields.io/badge/-llm-f5f5dc) ![](https://img.shields.io/badge/-agent-blue)

*Sun, Zhou, Li. arXiv, 2024.* [[paper](https://arxiv.org/abs/2408.01503)]

**Query Rewriting via Large Language Models.** ![](https://img.shields.io/badge/-llm-f5f5dc)

*Jie Liu, Barzan Mozafari. arXiv, 2024.* [[paper](https://arxiv.org/abs/2403.09060)]

**QUITE: A Query Rewrite System Beyond Rules with LLM Agents.** ![](https://img.shields.io/badge/-llm-f5f5dc) ![](https://img.shields.io/badge/-multi_agent-blue) ![](https://img.shields.io/badge/-training_free-grey)

*arXiv, 2025.* [[paper](https://arxiv.org/abs/2506.07675)]

**E3-Rewrite: Learning to Rewrite SQL for Executability, Equivalence, and Efficiency.** ![](https://img.shields.io/badge/-llm-f5f5dc) ![](https://img.shields.io/badge/-execution_driven-yellowgreen)

*arXiv, 2025.* [[paper](https://arxiv.org/abs/2508.09023)]

**OmniTune: A Universal Framework for Query Refinement via LLMs.** ![](https://img.shields.io/badge/-llm-f5f5dc)

*SIGMOD, 2026.*

**Leveraging Query Optimizers to Verify the Soundness of LLM-based Query Rewrites for Real-World Workloads.** ![](https://img.shields.io/badge/-llm-f5f5dc) ![](https://img.shields.io/badge/-formal_verification-purple)

*CIDR, 2026.*

---

### 1.4 Query Equivalence Verification

**HoTTSQL: Proving query rewrites with univalent SQL semantics.** ![](https://img.shields.io/badge/-formal_verification-purple)

*Shumo Chu, Konstantin Weitz, Alvin Cheung, Dan Suciu. PLDI, 2017.* [[paper](https://dl.acm.org/doi/10.1145/3062341.3062385)]

**Proving Query Equivalence Using Linear Integer Arithmetic.** ![](https://img.shields.io/badge/-formal_verification-purple)

*Haoran Ding, Zhaoguo Wang, Yicun Yang, et al. SIGMOD (PACMMOD), 2023.* [[paper](https://dl.acm.org/doi/10.1145/3626729)]

**QED: A Powerful Query Equivalence Decider for SQL.** ![](https://img.shields.io/badge/-formal_verification-purple)

*Shuai Wang, Shaowei Pan, Alvin Cheung. VLDB, 2024.* [[paper](https://dl.acm.org/doi/10.14778/3681954.3682017)]

---

## 2. NL2SQL / Text-to-SQL

### 2.1 Datasets and Benchmarks

**Spider: A Large-Scale Human-Labeled Dataset for Complex and Cross-Domain Semantic Parsing and Text-to-SQL Task.** ![](https://img.shields.io/badge/-benchmark-red)

*Tao Yu, Rui Zhang, Kai Yang, et al. EMNLP, 2018.* [[paper](https://aclanthology.org/D18-1425/)] [[data](https://yale-lily.github.io/spider)]

**WikiSQL: Seq2SQL: Generating Structured Queries from Natural Language using Reinforcement Learning.** ![](https://img.shields.io/badge/-benchmark-red)

*Victor Zhong, Caiming Xiong, Richard Socher. arXiv, 2017.* [[paper](https://arxiv.org/abs/1709.00103)] [[data](https://github.com/salesforce/WikiSQL)]

**BIRD: Can LLM Already Serve as A Database Interface? A BIg Bench for Large-Scale Database Grounded Text-to-SQLs.** ![](https://img.shields.io/badge/-benchmark-red) ![](https://img.shields.io/badge/-llm-f5f5dc)

*Jinyang Li, Binyuan Hui, Ge Qu, et al. NeurIPS, 2023.* [[paper](https://arxiv.org/abs/2305.03111)] [[data](https://bird-bench.github.io/)]

**Spider 2.0: Evaluating Language Models on Real-World Enterprise Text-to-SQL Workflows.** ![](https://img.shields.io/badge/-benchmark-red)

*Fangyu Lei, Jixuan Chen, Yuxiao Ye, et al. arXiv, 2024.* [[paper](https://arxiv.org/abs/2411.07763)]

**NL2SQL-BUGs: A Benchmark for Detecting Semantic Errors in NL2SQL Translation.** ![](https://img.shields.io/badge/-benchmark-red) ![](https://img.shields.io/badge/-semantic_error-orange)

*Xinyu Liu, Shuyu Shen, Boyan Li, Nan Tang, Yuyu Luo. KDD, 2025.* [[paper](https://arxiv.org/abs/2503.11984)]

---

### 2.2 Prompt-based Methods

**DIN-SQL: Decomposed In-Context Learning of Text-to-SQL with Self-Correction.** ![](https://img.shields.io/badge/-prompt-lightgrey) ![](https://img.shields.io/badge/-decomposition-yellowgreen)

*Mohammadreza Pourreza, Davood Rafiei. NeurIPS, 2023.* [[paper](https://arxiv.org/abs/2304.11015)] [[code](https://github.com/MohammadrezaPourreza/Few-shot-NL2SQL-with-prompting)]

**MAC-SQL: A Multi-Agent Collaborative Framework for Text-to-SQL.** ![](https://img.shields.io/badge/-multi_agent-blue) ![](https://img.shields.io/badge/-prompt-lightgrey)

*Bing Wang, Changyu Ren, Jian Yang, et al. arXiv, 2023.* [[paper](https://arxiv.org/abs/2312.11242)] [[code](https://github.com/wbbeyourself/MAC-SQL)]

**DAIL-SQL: Efficient Prompt Engineering for Large Language Models in Text-to-SQL.** ![](https://img.shields.io/badge/-prompt-lightgrey) ![](https://img.shields.io/badge/-in_context_learning-yellowgreen)

*Dawei Gao, Haibin Wang, Yaliang Li, et al. VLDB, 2024.* [[paper](https://arxiv.org/abs/2308.15363)] [[code](https://github.com/BeachWang/DAIL-SQL)]

**CHASE-SQL: Multi-Path Reasoning and Preference Optimized Candidate Selection in Text-to-SQL.** ![](https://img.shields.io/badge/-multi_path_reasoning-yellowgreen)

*arXiv, 2024.* [[paper](https://arxiv.org/abs/2410.01943)]

**Alpha-SQL: Zero-Shot Text-to-SQL Using Monte Carlo Tree Search.** ![](https://img.shields.io/badge/-MCTS-yellowgreen) ![](https://img.shields.io/badge/-zero_shot-grey)

*Boyan Li, Jiayi Zhang, Ju Fan, et al. arXiv, 2025.* [[paper](https://arxiv.org/abs/2502.17248)]

---

### 2.3 Fine-tuning Methods

**RESDSQL: Decoupling Schema Linking and Skeleton Parsing for Text-to-SQL.** ![](https://img.shields.io/badge/-fine_tuning-purple) ![](https://img.shields.io/badge/-schema_linking-blue)

*Haoyang Li, Jing Zhang, Cuiping Li, Hong Chen. AAAI, 2023.* [[paper](https://arxiv.org/abs/2302.05965)] [[code](https://github.com/RUCKBReasoning/RESDSQL)]

**OmniSQL: Synthesizing High-Quality Text-to-SQL Data at Scale.** ![](https://img.shields.io/badge/-fine_tuning-purple) ![](https://img.shields.io/badge/-data_synthesis-yellowgreen)

*Haoyang Li, et al. arXiv, 2025.* [[paper](https://arxiv.org/abs/2503.02240)]

---

### 2.4 Agent-based Methods

**Rethinking Schema Linking: A Context-Aware Bidirectional Retrieval Approach for Text-to-SQL.** ![](https://img.shields.io/badge/-schema_linking-blue) ![](https://img.shields.io/badge/-retrieval-yellowgreen)

*arXiv, 2024.* [[paper](https://arxiv.org/abs/2510.14296)]

**Lucy: Think and Reason to Solve Text-to-SQL.** ![](https://img.shields.io/badge/-chain_of_thought-yellowgreen) ![](https://img.shields.io/badge/-reasoning-blue)

*arXiv, 2024.* [[paper](https://arxiv.org/abs/2407.05153)]

**XiYan-SQL: A Novel Multi-Generator Framework for Text-to-SQL.** ![](https://img.shields.io/badge/-multi_agent-blue)

*arXiv, 2025.* [[paper](https://arxiv.org/abs/2507.04701)]

**Automated Validation and Fixing of Text-to-SQL Translation with Execution Consistency.** ![](https://img.shields.io/badge/-validation-orange) ![](https://img.shields.io/badge/-execution_feedback-yellowgreen)

*Yicun Yang, Zhaoguo Wang, Yu Xia, Zhuoran Wei. arXiv, 2025.*

---

## 3. Semantic Operators over Unstructured Data

**LOTUS: Enabling Semantic Queries with LLMs Over Tables of Unstructured and Structured Data.** ![](https://img.shields.io/badge/-semantic_operators-blue) ![](https://img.shields.io/badge/-llm-f5f5dc)

*Liana Patel, Siddharth Jha, et al. VLDB, 2024.* [[paper](https://arxiv.org/abs/2407.11418)] [[code](https://github.com/stanford-futuredata/lotus)]

**Semantic Operators and Their Optimization: Enabling LLM-Based Data Processing with Accuracy Guarantees in LOTUS.** ![](https://img.shields.io/badge/-semantic_operators-blue) ![](https://img.shields.io/badge/-accuracy_guarantees-green)

*Patel et al. VLDB, 2025.* [[paper](https://www.vldb.org/pvldb/vol18/p4171-patel.pdf)]

**Querying Large Language Models with SQL.** ![](https://img.shields.io/badge/-llm_as_db-blue)

*Mohammed Saeed, et al. EDBT, 2024.* [[paper](https://openproceedings.org/2024/conf/edbt/paper-61.pdf)]

---

## 4. Cardinality and Cost Estimation

**Are We Ready For Learned Cardinality Estimation?** ![](https://img.shields.io/badge/-cardinality_estimation-orange) ![](https://img.shields.io/badge/-experimental-red)

*Xiaoying Wang, Changbo Qu, Weiyuan Wu, Jiannan Wang, Qingqing Zhou. VLDB, 2021.* [[paper](https://dl.acm.org/doi/10.14778/3461535.3461539)]

**A Unified Deep Model of Learning from both Data and Queries for Cardinality Estimation.** ![](https://img.shields.io/badge/-cardinality_estimation-orange) ![](https://img.shields.io/badge/-deep_learning-purple)

*Peifeng Wu, Junru Shao, Tianyi Li, et al. SIGMOD, 2021.* [[paper](https://arxiv.org/abs/2107.12295)]

---

## 5. Plan Optimization

**SkinnerDB: Regret-Bounded Query Evaluation via Reinforcement Learning.** ![](https://img.shields.io/badge/-reinforcement_learning-blue) ![](https://img.shields.io/badge/-adaptive_execution-yellowgreen)

*Immanuel Trummer, Junxiong Wang, Deepak Maram, et al. SIGMOD, 2019.* [[paper](https://dl.acm.org/doi/10.1145/3299869.3300088)]

**Bao: Making Learned Query Optimization Practical.** ![](https://img.shields.io/badge/-plan_hints-yellowgreen) ![](https://img.shields.io/badge/-tree_conv-purple)

*Ryan Marcus, Parimarjan Negi, Hongzi Mao, et al. SIGMOD, 2021.* [[paper](https://dl.acm.org/doi/10.1145/3448016.3452838)] [[code](https://github.com/learnedsystems/BaoForPostgreSQL)]

**LEON: A New Framework for ML-Aided Query Optimization.** ![](https://img.shields.io/badge/-plan_selection-yellowgreen)

*Xu Chen, Haitian Chen, Zibo Liang, et al. VLDB, 2023.* [[paper](https://dl.acm.org/doi/10.14778/3598581.3598598)]

---

> **Contributing**: Please open a PR or Issue to add missing papers. Format: `**Title** [badges] *Authors. Venue, Year.* [[paper](link)] [[code](link)]`
