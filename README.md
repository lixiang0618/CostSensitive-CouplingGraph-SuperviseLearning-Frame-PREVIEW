#  Cost-Sensitive Coupling Graph Supervise Learning 

##  Project Overview

> **Overview:**  
> This project builds a **cost-sensitive coupling graph supervised learning framework**,  
> automatically converts structured data into HeteroData, and provides fine-grained cost-sensitive learning strategies.
> ⚠️## Note: The full code and data will be released later. Stay tuned! ##

##  Usage Steps

### 1️⃣ Generate Coupling Graph
```bash
python -m graph_generation --config configs/config.yaml
```
**Example Excel File (partial):**

| patient_id | fraud_label | region | amount | hospital_id | city | level | disease_code | disease_type | duration |
|------------|------------|--------|--------|-------------|------|-------|--------------|--------------|---------|
| 001 | 0 | guangxi | 1120 | 111 | hangzhou | High | 1001 | Chronic | 30 |
| 002 | 0 | guangdong | 469 | 112 | tengchong | High | 1002 | Acute | 820 |
| 003 | 0 | ningxia | 3 | 113 | wuzhou | Medium | 1001 | Acute | 821 |

### 2️⃣ Visualize Coupling Graph
```bash
python -m graph_visualize --config configs/config.yaml
```
![Coupling Graph Visualization](example.png)

### 3️⃣ Convert to HeteroData
```bash
python -m graph_to_hetero --config configs/config.yaml
```

### 4️⃣ Cost-Sensitive Training
Full workflow provided. Train directly with HAN or other frameworks.

## ✨ Highlights
-  Highly configurable: basic & coupling nodes, attributes, and coupling methods
-  Interactive visualization
-  Cost-sensitive training strategies

---

#  成本敏感耦合图监督学习 

## 项目简介
> 本项目构建了一个**成本敏感的耦合图监督学习框架**，能自动将结构化数据转换为异构图（HeteroData），并支持细粒度成本敏感策略。
> 在**华中师范大学信息管理学院肖飞老师**指导下完成。
> ⚠️## Note: The full code and data will be released later. Stay tuned! ##

##  功能模块

### 1️⃣ 创建耦合图
```bash
python -m graph_generation --config configs/config.yaml
```
**示例 Excel 文件（部分）：**

| patient_id | fraud_label | region | amount | hospital_id | city | level | disease_code | disease_type | duration |
|------------|------------|--------|--------|-------------|------|-------|--------------|--------------|---------|
| 001 | 0 | guangxi | 1120 | 111 | hangzhou | 高级 | 1001 | 慢性 | 30 |
| 002 | 0 | guangdong | 469 | 112 | tengchong | 高级 | 1002 | 急性 | 820 |
| 003 | 0 | ningxia | 3 | 113 | wuzhou | 中级 | 1001 | 急性 | 821 |

### 2️⃣ 可视化耦合图
```bash
python -m graph_visualize --config configs/config.yaml
```
![耦合图可视化](example.png)

### 3️⃣ 转换为 HeteroData
```bash
python -m graph_to_hetero --config configs/config.yaml
```

### 4️⃣ 成本敏感训练
全套耦合异构图及细粒度成本敏感策略，可直接用 HAN 等框架完成训练。

## ✨ 项目亮点
-  高度可配置：自定义基本节点与耦合节点、耦合方式、节点属性
-  交互式可视化
-  成本敏感训练策略
