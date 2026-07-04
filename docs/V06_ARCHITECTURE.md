# V06_ARCHITECTURE

## 目标

V06 的目标不是继续修 V05/R6，而是把 BE THE MASTER 从“门禁循环”改成“先判题、再补证据、再定风格、最后写稿和产品审稿”的低噪音链路。

## 固定根目录

- 当前根目录：`<PROJECT_ROOT>`，真实本地路径只记录在 `local_registry/`
- 旧目录：`<LEGACY_FINANCE_ROOT>`，真实本地路径只记录在 `local_registry/`
- 旧目录只作历史参考，不允许新写入。

## 角色结构

| 角色 | 名称 | 核心职责 | 产物 |
|---|---|---|---|
| Z | 项目统筹 | 编号、路径、登记、归因、迭代审批 | Z_ROUND_REVIEW |
| A-V06 | 资讯搜寻 | 找材料、标来源、分事实/观点、标风险 | A_SOURCE_PACKET |
| B-V06 | 选题立项 | 判断是否值得写，输出 GO/PIVOT/KILL | B_TOPIC_DECISION_CARD |
| C-V06 | 证据增强 | 补数据、案例、反证和不确定性 | C_EVIDENCE_PACK |
| D-V06 | 风格路线 | 选择 KOL 风格资源和表达策略 | D_STYLE_ROUTE_CARD |
| E-V06 | 成稿写作 | 只按 B/C/D 输出成稿 | E_DRAFT_PACKAGE |
| F-V06 | 产品审稿 | 区分流程通过和产品通过 | F_PRODUCT_REVIEW_REPORT |

## 关键变化

1. B 拥有选题生杀权。
2. C 证据不足时必须回 B，不让 E 硬写。
3. D 不再审稿，只做风格路线。
4. F 才是最终产品审稿。
5. `PROCESS_PASS` 不等于 `PRODUCT_PASS`。
6. 一轮最多允许 E 修改一次。
7. 旧 A/B/C/D 线程归档，不作为 V06 派发目标。
