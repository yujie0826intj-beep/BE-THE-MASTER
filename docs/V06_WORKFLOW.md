# V06_WORKFLOW

## 固定流程

```text
Z -> A -> B -> C -> B_CONFIRM -> D -> E -> F -> Z
```

## 阶段说明

1. `Z_INIT`
   - 确认任务、材料边界、写入路径和噪音风险。
   - 创建任务目录和派发卡。

2. `A_SOURCE`
   - A 搜寻或整理允许范围内的材料。
   - 输出 `A_SOURCE_PACKET.md`。

3. `B_TOPIC_GATE`
   - B 判断题目是否值得写。
   - 输出 `GO / PIVOT / KILL`。

4. `C_EVIDENCE`
   - C 对 B 的立题补证据、找反证和不确定性。
   - 输出 `SUFFICIENT / INSUFFICIENT`。

5. `B_CONFIRM`
   - B 根据 C 的证据重新确认。
   - 如证据不足，必须 `PIVOT` 或 `KILL`。

6. `D_STYLE`
   - D 从 `resources/style_cards/` 选择或生成风格路线。
   - D 不审稿。

7. `E_DRAFT`
   - E 只根据 B/C/D 写稿。
   - 每轮最多一次修订。

8. `F_PRODUCT_REVIEW`
   - F 同时输出 `PROCESS_PASS/FAIL` 和 `PRODUCT_PASS/FAIL`。

9. `Z_CLOSE`
   - Z 记录结论、归因和是否进入下一轮。

## 路由规则

- B `KILL`：Z 关闭本题。
- B `PIVOT`：Z 重新定义题目，不给 E。
- C `INSUFFICIENT`：回 B，不给 D/E。
- F `PROCESS_FAIL`：回对应缺口角色。
- F `PROCESS_PASS / PRODUCT_FAIL`：先回 B 或 C，不连续让 E 重写。
