# V06_QUALITY_GATES

## Gate 1: ROOT_PATH_GATE

所有新写入必须在 `<PROJECT_ROOT>`。旧 `<LEGACY_FINANCE_ROOT>` 只读。

## Gate 2: TOPIC_GATE

B 必须输出 `GO / PIVOT / KILL`。

- 无读者价值：`KILL`
- 材料只够另一角度：`PIVOT`
- 有现实重要性、预期差、证据路径和作者判断：`GO`

## Gate 3: EVIDENCE_GATE

C 必须输出 `SUFFICIENT / INSUFFICIENT`。

- 关键事实缺失：`INSUFFICIENT`
- 数据口径冲突无法解释：`ESCALATE`
- 证据只够解释常识：回 B

## Gate 4: STYLE_ROUTE_GATE

D 必须指定具体风格资源卡，不得用“财经 KOL 风格”这类泛称。

## Gate 5: DRAFT_INPUT_GATE

E 必须同时收到 B、C、D 三张上游卡。缺任一张，不能写稿。

## Gate 6: PRODUCT_REVIEW_GATE

F 必须同时输出：

- `PROCESS_PASS / PROCESS_FAIL`
- `PRODUCT_PASS / PRODUCT_FAIL`

## Gate 7: REWRITE_LIMIT_GATE

E 每轮最多修改一次。第二次仍不达标，必须回 B 或 C。

## Gate 8: TWO_PRODUCT_FAIL_GATE

同一选题连续两轮 `PRODUCT_FAIL`，B 必须重新判断 `PIVOT` 或 `KILL`。
