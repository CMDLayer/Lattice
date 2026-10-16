# Required Reasoning Protocol

This file expands the reasoning passes in `SKILL.md` into an implementation-ready procedure.

## Pass 0 — Safety and legitimacy gate

Before strategic synthesis, classify the problem.

Check:
- Does the requested plan involve unlawful conduct?
- Does it involve non-consensual deception or coercion?
- Would a proposed bridge depend on exploiting private/sensitive personal information?
- Are there safety-critical or regulated decisions that require qualified oversight?
- Are there political/electoral persuasion goals where the agent should remain informational rather than directive?
- Could optimizing a bridge reasonably create harmful externalities?

Output:
- `allowed_scope`
- `restricted_mechanisms`
- `required_disclosures`
- `human_decision_points`

## Pass 1 — Condition-space extraction

Create a structured situation model.

### 1.1 Facts
Only user-provided or reliably established facts.

### 1.2 Assumptions
Inferences required to proceed.

### 1.3 Objectives
Separate:
- terminal objective,
- intermediate objectives,
- defensive objectives,
- learning objectives.

### 1.4 Constraints
Classify:
- hard vs soft,
- internal vs external,
- immediate vs eventual,
- reversible vs irreversible.

### 1.5 Resources
Include:
- money,
- time,
- people,
- authority,
- information,
- relationships,
- infrastructure,
- credibility,
- existing assets.

### 1.6 Uncertainties
Describe:
- what is unknown,
- why it matters,
- how it could be reduced,
- and whether planning should preserve options.

### 1.7 Time
Identify:
- deadlines,
- activation windows,
- lead times,
- dependencies,
- state expiry.

## Pass 2 — Dimension discovery

Generate candidate dimensions by asking:
- What distinct types of work can proceed somewhat independently?
- Which objectives require different capabilities or actors?
- Which problems operate on different timescales?
- Which bottlenecks belong to different causal mechanisms?
- Which assets could be created in one area and used in another?

Score each candidate dimension on:
- independence,
- strategic relevance,
- controllability,
- observability,
- and bridge potential.

Remove:
- duplicate dimensions,
- overly broad "miscellaneous" dimensions,
- dimensions that are merely phases of one obvious sequence,
- dimensions with no coherent local objective.

## Pass 3 — Independent planning

Important rule: temporarily ignore all cross-dimensional synergy.

For each dimension:
1. State its local objective.
2. Define local success.
3. Identify 2–5 actions.
4. Identify dependencies.
5. Identify decision points.
6. State what would cause termination, pivot, or escalation.
7. Check the removal test: would this still make sense if all other dimensions vanished?

This pass prevents retrofitted causality.

## Pass 4 — State extraction

For each material action create a state-transition record:

```yaml
action_id: A2
before_state:
  - ...
action:
  - ...
after_state:
  - ...
persistence:
  - transient | persistent | durable
observable_signals:
  - ...
confidence: high | medium | low
```

State changes should be concrete enough that another dimension could plausibly consume them.

Bad:
- "Momentum increases."

Better:
- "Three reference customers agree to calls with prospective enterprise buyers."

Bad:
- "Brand improves."

Better:
- "Unaided awareness among target users rises from baseline, measured in a survey."

## Pass 5 — Forward bridge discovery

For every after-state, iterate through all other dimensions.

Question set:
- Does this change another dimension's available actions?
- Does it remove a prerequisite?
- Does it create evidence?
- Does it reduce uncertainty?
- Does it create or reduce access?
- Does it change cost?
- Does it change timing?
- Does it change risk?
- Does it create permission or legitimacy?
- Does it improve capability?
- Does it create reusable optionality?

Record all plausible bridges, then prune later.

## Pass 6 — Backward condition tracing

Start from:
- bottlenecks,
- expensive steps,
- fragile assumptions,
- slow steps,
- blocked actions,
- high-risk decisions.

For each:
1. Ask: "What condition would make this materially easier?"
2. Ask: "Could another dimension naturally create that condition?"
3. Ask: "What locally rational action there would create it?"
4. Ask: "Would that source action still be worth doing locally?"
5. Add the candidate bridge if yes.

This pass often finds high-leverage links that forward scanning misses.

## Pass 7 — Causal validation

Evaluate each candidate bridge on seven criteria.

### 7.1 Counterfactual
Without the source state change, would the target dimension be materially different?

### 7.2 Mechanism
Can the causal mechanism be described in one or two sentences without handwaving?

### 7.3 Magnitude
Is the effect large enough to influence planning?

### 7.4 Timing
Does the state exist at the time the target can use it?

### 7.5 Agency
Does the bridge depend on controlling another person rather than changing conditions around a voluntary decision?

### 7.6 Observability
Can the agent or user detect whether the bridge is active?

### 7.7 Complexity
Does the benefit justify coordination cost and added fragility?

Recommended decision:
- `keep`
- `optional`
- `downgrade`
- `reject`

Use `optional` for a plausible bridge worth preserving without making an architecture depend on it. In older materials, `keep_as_optional` means the same thing and maps to `optional` in this package's schema.

## Pass 8 — Architecture synthesis

Compose selected bridges into structurally different architectures.

### Architecture pattern A — Cascade
`A -> B -> C`

Use when one state is progressively transformed.

### Pattern B — Convergence
`A -> C` and `B -> C`

Use when two dimensions independently create complementary conditions for a third.

### Pattern C — Hub-and-spoke
Several dimensions create or consume states around one integrating dimension.

Use carefully; hub failure can be catastrophic.

### Pattern D — Reciprocal reinforcement
`A -> B` and later `B -> A`

Useful for learning loops, product-market feedback, capability-building.

### Pattern E — Optionality tree
One upstream state creates several possible downstream moves.

Useful under uncertainty.

### Pattern F — Staged transformation
`A produces X; B converts X to Y; C converts Y to Z`

This is the most direct expression of the original three-plane idea.

## Pass 9 — Strengthening

For each architecture:
- clarify boundary artifacts,
- define handoff owner/system,
- add observation signals,
- align timing,
- reduce speculative dependencies,
- convert single-use states into reusable assets when sensible,
- protect load-bearing bridges,
- avoid unnecessary synchronization.

## Pass 10 — Stress testing

Minimum stress tests:

1. **Bridge removal:** Remove the strongest bridge.
2. **Delay:** Shift a key state past its activation window.
3. **Weak response:** Reduce a probabilistic downstream response by half.
4. **Assumption failure:** Invalidate one medium-confidence assumption.
5. **Resource shock:** Cut one major resource by 25–50%.
6. **External change:** Introduce a plausible environmental change.

For each:
- what breaks?
- what survives?
- what alternate path exists?
- what signal would reveal the problem early?
- what adaptation preserves the meta objective?

## Pass 11 — Architecture comparison

Compare architectures on:
- local coherence,
- bridge strength,
- uncertainty,
- speed,
- reversibility,
- resource demand,
- number of load-bearing bridges,
- learning value,
- optionality,
- coordination burden,
- human-dependence,
- downside if wrong.

Use qualitative or numeric scoring only if helpful. Do not create false precision.

## Pass 12 — Final output

Provide:
- concise condition-space summary,
- dimensions and local plans,
- bridge ledger,
- architecture diagrams,
- assumptions,
- stress test,
- first moves.

The user should be able to inspect every vertical relationship and ask, "Why should this cause that?" The answer should be explicit.
