# Human-Readable Output Schema

The final response should let a reader see both the horizontal plans and the vertical causal relationships.

## 1. Situation Summary

**Objective:**  
One paragraph.

**Important conditions:**  
Bulleted summary of constraints, assets, uncertainties, time windows, and important assumptions.

## 2. Dimensions

For each dimension:

### Dimension D1 — Name
- **Local objective:**
- **Why distinct:**
- **Controls:**
- **Does not control:**
- **Time horizon:**
- **Local success signal:**

## 3. Independent Plans

| ID | Dimension | Action | Local purpose | Resulting local state | Decision / exit condition |
|---|---|---|---|---|---|

No cross-dimensional justification is required in this table. This is deliberate.

## 4. State Inventory

| State ID | Source action | State created | Persistence | Observable signal | Confidence |
|---|---|---|---|---|---|

## 5. Bridge Ledger

| Bridge | Source | State change | Target | Mechanism | Effect type | Strength | Timing | Counterfactual |
|---|---|---|---|---|---|---|---|---|

This is the most important auditing surface in the output.

## 6. Architecture Options

Provide 2–4 alternatives.

For each:

### Architecture A — Name
**Pattern:** staged transformation / cascade / convergence / etc.

**Diagram**
```text
...
```

**Primary causal chains**
- `...`

**What this architecture optimizes**
- ...

**Main assumptions**
- ...

**Load-bearing bridges**
- ...

**Weaknesses / tradeoffs**
- ...

**Signals to monitor**
- ...

## 7. Stress Test

| Stress | Expected impact | Surviving path | Adaptation |
|---|---|---|---|

## 8. First Moves

List the first 3–7 actions that:
- are locally justified,
- create high-information or high-leverage states,
- preserve optionality,
- and activate the most useful bridges.

## 9. Optional Machine-Readable Appendix

When useful, include JSON conforming to `schemas/orchestration.schema.json`.
