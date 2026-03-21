# KNOWLEDGE-ASSET-MAPPING.md

## 目的
将 `content/knowledge/` 中的核心知识卡片，映射到全球资产配置框架中。

说明：
- 本文件先做 **P0/P1 核心知识主题的实装映射**
- 暂不直接改写 `data/knowledge-pool.json` 的原始结构
- 后续确认字段方案后，再回填到数据层

---

## 一、P0 知识卡片映射

### 1. 利率如何影响估值
- 原文件：`content/knowledge/interest-rate-and-valuation.md`
- 影响资产：
  - 权益
  - 国债
  - 美债
  - 黄金
  - 汇率
- 应用场景：
  - 估值判断
  - 利率周期判断
  - 风格切换判断
  - 大类资产比较
- 主要映射：
  - `content/assets/us-treasuries.md`
  - `content/assets/china-gov-bonds.md`
  - `content/assets/gold.md`
  - `content/assets/equities-overview.md`
  - `content/assets/a-shares.md`
  - `content/assets/us-stocks.md`
- 配置动作示例：
  - 利率下行时，提高对长久期成长/债券/黄金的关注
  - 利率上行时，降低高估值成长权重，关注价值/高股息/防守配置

### 2. ROE 为什么重要
- 原文件：`content/knowledge/roe-dupont.md`
- 影响资产：
  - 权益
- 应用场景：
  - 个股质量判断
  - 行业龙头筛选
  - 组合持仓优选
- 主要映射：
  - `content/assets/equities-overview.md`
  - `content/assets/a-shares.md`
  - `content/assets/hk-stocks.md`
  - `content/assets/us-stocks.md`
  - `content/stocks/`
- 配置动作示例：
  - 优先关注高 ROE 且可持续的龙头公司
  - 避免被短期高利润但低质量盈利误导

### 3. 自由现金流怎么看
- 候选原文件：
  - `content/knowledge/free-cash-flow.md`
  - `content/knowledge/cashflow-vs-profit.md`
- 影响资产：
  - 权益
  - 高股息策略
- 应用场景：
  - 识别企业盈利质量
  - 判断分红持续性
  - 评估资本开支与现金创造能力
- 主要映射：
  - `content/assets/equities-overview.md`
  - `content/assets/a-shares.md`
  - `content/assets/hk-stocks.md`
  - `content/assets/us-stocks.md`
  - `content/sectors/high-dividend.md`
  - `content/stocks/`
- 配置动作示例：
  - 优先选择自由现金流稳定、资本开支纪律清晰的公司
  - 高股息配置需结合现金流验证，而不只看股息率

### 4. 行业景气度怎么判断
- 原文件：`content/knowledge/sector-prosperity-framework.md`
- 影响资产：
  - 权益
  - 行业轮动
- 应用场景：
  - 行业配置
  - 周期判断
  - 风格切换
- 主要映射：
  - `content/assets/a-shares.md`
  - `content/assets/hk-stocks.md`
  - `content/assets/us-stocks.md`
  - `content/sectors/`
- 配置动作示例：
  - 景气上行行业提高关注度和权重
  - 景气下行但估值未充分消化的行业谨慎参与

### 5. 仓位管理与回撤控制
- 候选原文件：
  - `content/knowledge/position-sizing.md`
  - `content/knowledge/position-and-drawdown.md`
- 影响资产：
  - 权益
  - 黄金
  - 债券
  - 组合层
- 应用场景：
  - 风险预算
  - 仓位分配
  - 回撤控制
  - 再平衡
- 主要映射：
  - `frameworks/portfolio-template.md`
  - `frameworks/weekly-review-template.md`
  - `content/assets/gold.md`
  - `content/assets/bonds.md`
  - `content/assets/equities-overview.md`
- 配置动作示例：
  - 高波动资产不只看赔率，也看组合承受力
  - 用仓位控制代替情绪化交易

---

## 二、P1 可继续扩展的主题

### 商业模式分析框架
- 原文件：`content/knowledge/business-model-framework.md`
- 主要影响：权益 / 个股研究
- 主要用途：
  - 判断企业赚钱方式
  - 判断竞争优势是否可持续
  - 支撑长期持仓逻辑

### 预期差为什么重要
- 原文件：`content/knowledge/expectation-gap.md`
- 主要影响：权益 / 交易复盘
- 主要用途：
  - 区分“好公司”和“好投资机会”
  - 判断市场预期是否过高或过低

### ROIC
- 原文件：`content/knowledge/roic.md`
- 主要影响：权益 / 个股质量判断
- 主要用途：
  - 衡量资本配置效率
  - 辅助判断护城河与长期复利能力

---

## 三、现阶段结论
原来的知识卡片已经可以分成三类角色：

1. **宏观/估值锚**
   - 利率如何影响估值
   - 美债/国债/黄金/汇率相关知识

2. **行业配置锚**
   - 行业景气度怎么判断
   - 行业生命周期
   - 产业链研究

3. **个股质量锚**
   - ROE
   - ROIC
   - 自由现金流
   - 商业模式

4. **组合管理锚**
   - 仓位管理
   - 回撤控制
   - 预期差复盘

这说明原本的知识库已经具备升级为“资产配置知识中台”的基础。

---

## 四、下一步建议
- [ ] 将本映射逐步回填到 `data/knowledge-pool.json`
- [ ] 为 `content/sectors/` 补充“宏观敏感变量”字段
- [ ] 为 `content/stocks/` 补充“配置角色”字段
- [ ] 建立第一版 `weekly allocation review` 输出样板
