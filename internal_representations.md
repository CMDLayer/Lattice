# Internal Representations

These representations are intended to structure an agent's planning process without requiring exposure of private chain-of-thought. They can be stored as JSON, YAML, graph objects, or database rows.

## 1. ConditionSpace

```yaml
objective:
  terminal: ""
  intermediate: []
constraints:
  hard: []
  soft: []
resources: []
actors: []
systems: []
uncertainties: []
deadlines: []
time_windows: []
existing_commitments: []
ethical_boundaries: []
facts: []
assumptions: []
```

## 2. Dimension

```yaml
id: D1
name: ""
local_objective: ""
scope: ""
controls: []
does_not_control: []
resources: []
constraints: []
time_horizon: ""
success_signals: []
actions: []
```

## 3. Action

```yaml
id: D1-A1
dimension_id: D1
name: ""
local_purpose: ""
prerequisites: []
execution:
  owner_type: ""
  duration: ""
  resources: []
expected_local_result: ""
state_changes: []
decision_points: []
exit_conditions: []
```

## 4. StateChange

```yaml
id: S1
source_action_id: D1-A1
before: []
after: []
effect_types: []
persistence: transient | persistent | durable
activation_time: ""
expiry_time: ""
signals: []
confidence: high | medium | low
```

## 5. Bridge

```yaml
id: B1
source_dimension_id: D1
source_action_id: D1-A1
state_change_id: S1
target_dimension_id: D2
target_plan_element: D2-A2
mechanism: ""
effect_type: information
downstream_affordance: ""
counterfactual: ""
timing:
  available_from: ""
  useful_until: ""
strength: strong | moderate | weak | speculative
confidence: high | medium | low
load_bearing: false
assumptions: []
signals: []
agency_note: ""
status: keep | optional | downgrade | reject
```

## 6. Handoff

```yaml
id: H1
bridge_id: B1
artifact_or_condition: ""
producer: ""
consumer: ""
handoff_method: ""
acceptance_signal: ""
failure_signal: ""
```

## 7. Architecture

```yaml
id: ARCH-1
name: ""
pattern: cascade | convergence | hub_spoke | reciprocal | optionality_tree | staged_transformation | custom
meta_objective: ""
dimensions: []
bridges: []
causal_chains: []
load_bearing_bridges: []
redundancies: []
key_assumptions: []
primary_tradeoffs: []
```

## 8. Causal Chain

```yaml
id: CHAIN-1
steps:
  - action: D1-A2
  - state: S3
  - bridge: B2
  - action: D2-A1
  - state: S5
  - bridge: B5
  - action: D3-A3
description: ""
weakest_link: ""
```

## 9. Bridge Matrix

A compact matrix can help discovery.

Rows = source state changes.  
Columns = target dimensions.

Cell values:
- blank: no meaningful relation
- `C`: capability
- `I`: information
- `A`: access
- `R`: resource
- `T`: timing
- `E`: evidence
- `K`: constraint
- `O`: optionality
- `P`: probability/position
- combinations allowed when necessary

Example:

| Source state | Product | Financing | Partnerships | Hiring |
|---|---|---|---|---|
| validated use case | — | E | E/A | I |
| signed partner LOI | R | E | — | P |
| repeatable deployment | C | E | A | C |

The matrix is a discovery tool, not proof. Each non-empty cell still needs causal validation.

## 10. Dependency vs. Leverage Tag

Every bridge should be tagged:

- `dependency`: target cannot proceed without it.
- `leverage`: target can proceed, but becomes materially better.
- `option`: target gains an additional viable move.
- `signal`: target receives useful information.
- `hedge`: target's downside or exposure is reduced.

This distinction improves robustness.

## 11. Bridge Confidence Model

Confidence may be estimated from:
- mechanism clarity,
- evidence quality,
- actor independence,
- timing certainty,
- historical precedent,
- number of assumptions,
- and observability.

Suggested rule:
- High: direct mechanism, observable, few assumptions.
- Medium: credible mechanism, some external dependence.
- Low: multiple assumptions or uncertain response.
- Speculative: imaginative connection with insufficient evidence.

## 12. Architecture Health Metrics

Optional qualitative metrics:

### Local Coherence
Do the dimensions still make sense independently?

### Causal Density
Number of validated bridges / number of possible cross-dimension pairs.

Low-to-moderate density is often healthier than maximum density.

### Load-Bearing Ratio
Load-bearing bridges / total bridges.

High ratio implies fragility.

### Probabilistic Dependence
Share of bridges that rely on independent human or market responses.

### State Reuse
How many state changes support more than one legitimate downstream use?

### Observability
How many bridges have measurable activation signals?

### Reversibility
How easy it is to unwind actions if assumptions fail?

These are diagnostic, not universal optimization targets.
