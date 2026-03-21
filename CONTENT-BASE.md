# 内容底座设计（V1）

## 目标
为股票学习系统建立可持续扩充的内容底座，让网站、知识沉淀、自动化提醒三者共享同一套内容结构。

---

## 一、底座原则

### 1. 展示层与内容层分离
- 网站负责展示
- Markdown 负责沉淀深度内容
- JSON 负责结构化读取

### 2. 先样例、后规模
先把一套模板和 10~20 个样例条目跑通，再逐步扩容。

### 3. 一切内容可复盘
每个条目都应包含：
- 是什么
- 为什么重要
- 关键结论
- 如何使用
- 后续延伸

---

## 二、目录结构

```text
stock-learning-site/
├── content/
│   ├── knowledge/
│   ├── stocks/
│   ├── sectors/
│   ├── outputs/
│   └── resources/
└── data/
    ├── dashboard.json
    ├── knowledge-pool.json
    ├── stocks.json
    ├── sectors.json
    ├── outputs.json
    └── resources.json
```

---

## 三、核心内容对象

### 1. Knowledge
用于管理知识点卡片。

字段：
- id
- title
- category
- priority
- status
- summary
- whyItMatters
- practicalUse
- mistakes
- relatedTopics
- source
- updatedAt

### 2. Stock
用于管理个股研究。

字段：
- id
- name
- ticker
- sector
- thesis
- businessModel
- keyMetrics
- risks
- watchItems
- updatedAt

### 3. Sector
用于管理行业研究。

字段：
- id
- name
- definition
- drivers
- industryChain
- leaders
- indicators
- risks
- updatedAt

### 4. Output
用于管理输出内容。

字段：
- id
- title
- type
- date
- summary
- relatedTopics
- nextActions

### 5. Resource
用于管理资料来源。

字段：
- id
- title
- type
- topic
- quality
- link
- notes

---

## 四、首批学习主线

### P0（必须优先）
- 利率与估值
- 三大财务报表
- ROE / 现金流
- PE / PB / DCF
- 行业景气度
- 商业模式分析

### P1（第二层）
- 宏观周期
- 汇率与流动性
- 龙头公司研究法
- 财报拆解案例
- 行业产业链研究

### P2（延伸层）
- 交易心理
- 仓位管理
- 高阶估值模型
- 主题投资框架

---

## 五、内容生产流程

### 流程 1：新知识进入系统
1. 发现主题
2. 加入 Knowledge Pool
3. 标记优先级
4. 学习并摘要
5. 形成知识卡片
6. 关联到行业/个股/输出

### 流程 2：个股研究进入系统
1. 建立个股卡片
2. 写清商业模式
3. 补充关键指标
4. 记录投资逻辑
5. 更新风险点与跟踪项

### 流程 3：输出进入系统
1. 每日复盘
2. 每周总结
3. 提炼出长期结论
4. 回写到知识卡片/研究库

---

## 六、模板建议

### Knowledge 模板
- 定义
- 重要性
- 核心逻辑
- 关键指标/公式
- 实战使用方式
- 常见误区
- 相关知识
- 案例

### Stock 模板
- 公司简介
- 商业模式
- 投资逻辑
- 财务表现
- 估值观察
- 风险点
- 持续跟踪清单

### Sector 模板
- 行业定义
- 产业链
- 景气驱动
- 龙头公司
- 跟踪指标
- 风险因素

---

## 七、当前落地建议

先做三件事：
1. 建 1 份 knowledge-pool.json 样例
2. 建 1 份 dashboard.json 样例
3. 建 3~5 篇知识卡片 Markdown 样例

这样网站马上就能从“静态说明页”升级成“半数据驱动学习系统”。
