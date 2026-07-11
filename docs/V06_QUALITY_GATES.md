# V06_QUALITY_GATES

## Gate 1: ROOT_PATH_GATE

All new public work must stay under `<PROJECT_ROOT>`. The legacy `<LEGACY_FINANCE_ROOT>` is historical reference only.

## Gate 2: S_STRUCTURAL_JUDGMENT_GATE

S must pass `S_STRUCTURAL_JUDGMENT_GATE` before B can judge topic viability.

Required:

- macro/policy/industry or business-model frame,
- normal expectation,
- abnormal divergence,
- at least two independent signal categories for a non-weak judgment,
- mechanism linking signals to the judgment,
- falsifier,
- causal boundaries.

If A's material is too thin, S must return `RETURN_TO_A_FOR_SOURCE_GAP`. If facts exist but S cannot form an objective professional judgment, S must return `RETURN_TO_Z_FOR_HUMAN_JUDGMENT`. B and C must not continue from a failed S gate.

## Gate 3: TOPIC_GATE

B must output `GO / PIVOT / KILL`.

- No reader value: `KILL`
- Material supports a different angle: `PIVOT`
- Current importance, expectation gap, evidence path, and author thesis exist: `GO`

## Gate 4: EVIDENCE_GATE

C must output evidence sufficiency.

- Key facts missing: `INSUFFICIENT`
- Source conflict cannot be resolved: `ESCALATE`
- Evidence only supports common knowledge: return to B
- Evidence supports the question with boundaries: `SUFFICIENT`

## Gate 5: B_CONFIRM_GATE

After C, B must output `B_CONFIRM_CARD` with one decision:

- `CONFIRM_GO_TO_D`
- `PIVOT_BEFORE_D`
- `RETURN_TO_C`
- `KILL`

D may start only when `D_ENTRY_ALLOWED: YES`.

## Gate 6: STYLE_ROUTE_GATE

D must name a concrete style-card route. Generic labels such as "finance KOL style" are not enough.

If no style card fits, D must return `STYLE_ROUTE_MISSING`.

## Gate 7: DRAFT_INPUT_GATE

E must receive B, C, and D handoffs. If any are missing, E must not draft.

## Gate 8: E_MICRO_SAMPLE_GATE

For new angles, new style routes, or any route after human dissatisfaction, E must produce a micro sample before a full draft.

Required:

- selected title,
- opening three paragraphs,
- first two section headings,
- paragraph movement,
- evidence-boundary plan.

If the micro sample does not create reader tension or preserve the S/B judgment, Z returns to D or B before a full E draft.

## Gate 9: PRODUCT_REVIEW_GATE

F must output both:

- `PROCESS_PASS / PROCESS_FAIL`
- `PRODUCT_PASS / PRODUCT_FAIL`

`PROCESS_PASS` means the workflow is complete. `PRODUCT_PASS` means the article is a publish candidate.

F must compare the draft against the current locked baseline in `docs/V06_LOCKED_GENERATION_CHAIN.md`.

A draft that is compliant but less worth reading than the baseline is `PRODUCT_FAIL`.

## Gate 10: REWRITE_LIMIT_GATE

E may rewrite at most once per round. If the second version still fails, the route returns to B, C, or D.

## Gate 11: TWO_PRODUCT_FAIL_GATE

If the same topic gets two consecutive `PRODUCT_FAIL` results, B must reconsider `PIVOT` or `KILL`.

## Gate 12: PRE_S_NOISE_GATE

Pre-S production attempts must not be used as canonical writing inputs.

They may be used only as failure examples or noise diagnostics unless Z explicitly promotes a narrow reusable rule.
