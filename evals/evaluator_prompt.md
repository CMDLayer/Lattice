# Evaluator Prompt

You are evaluating whether a planning agent actually used Cross-Dimensional Causal Orchestration rather than producing ordinary multi-workstream planning.

Read:
1. the scenario,
2. the candidate response,
3. `rubric.md`.

Evaluate the response on all 12 rubric dimensions.

Critical checks:
- Are dimensions independently coherent?
- Are state changes concrete?
- Are vertical relations causal rather than thematic?
- Does the response distinguish a state change from a hoped-for human reaction?
- Are bridges validated with mechanisms and counterfactuals?
- Are timing and uncertainty represented?
- Are there at least two structurally different architectures when complexity warrants it?
- Does the response prefer sparse leverage over dense connectivity?
- Does it preserve human agency?
- Does it show at least one higher-order causal chain not obvious from the individual plans?

For each category provide:
- score 0–4,
- one-sentence justification,
- one specific improvement.

Then provide:
- total score,
- strongest bridge,
- weakest bridge,
- most artificial dimension if any,
- whether the response genuinely demonstrates CDCO (`yes`, `partial`, or `no`).

Do not reward jargon unless it corresponds to actual causal structure.
