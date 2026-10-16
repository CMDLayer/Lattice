# Ontology

This document defines the objects an agent should use when reasoning with CDCO.

## 1. Condition Space
The full planning context currently known to the agent.

Fields:
- objective(s)
- constraints
- resources
- capabilities
- actors
- systems
- uncertainties
- deadlines / time windows
- irreversible commitments
- external forces
- known dependencies
- known opportunities
- legal / ethical boundaries
- evidence quality

## 2. Dimension
A relatively independent domain of action that can support its own coherent plan.

A dimension has:
- `id`
- `name`
- `local_objective`
- `scope`
- `controlled_variables`
- `uncontrolled_variables`
- `resources`
- `constraints`
- `time_horizon`
- `success_signals`
- `actions`

Examples:
- product validation
- financing
- hiring
- partnerships
- distribution
- regulatory preparation
- operations
- customer learning
- communications
- infrastructure

A dimension is not merely a category label. It needs enough internal logic to contain a plan.

## 3. Plan
A sequence or network of actions inside a dimension.

A plan should specify:
- intended local outcome,
- prerequisites,
- actions,
- decision points,
- exit criteria,
- and relevant assumptions.

## 4. Action
A deliberate intervention within a plan.

Each action should be represented through two lenses:
- **Local function:** why it makes sense in its own plan.
- **External consequences:** what state changes it may create beyond its immediate local purpose.

## 5. State
A description of relevant conditions at a moment.

Examples:
- "usage evidence exists"
- "supplier lead time is known"
- "three candidate partners have signed LOIs"
- "deployment process is repeatable"
- "cash runway has increased"
- "customer acquisition cost uncertainty has narrowed"

States are more useful than vague outcomes because other dimensions can consume them.

## 6. State Change
A transition caused or materially influenced by an action.

Representation:

`before_state -> action -> after_state`

## 7. Bridge
A causal relation between a source state change and a receiving dimension.

Minimum fields:
- `source_dimension`
- `source_action`
- `state_change`
- `target_dimension`
- `mechanism`
- `effect_type`
- `strength`
- `confidence`
- `timing` (expected absolute `available_from`/`useful_until` and/or stage-relative `usable_after_stage`/`expires_before_stage` usability window)
- `assumptions`
- `counterfactual`

## 8. Handoff
The operational realization of a bridge.

The bridge is the causal relation. The handoff is how the receiving dimension actually becomes able to use it.

Example:
- Bridge: a pilot creates credible usage evidence relevant to fundraising.
- Handoff: a financing workstream packages the evidence into a data room and investor narrative.

## 9. Transformation
A case where the receiving dimension converts an incoming state into a new state that can itself affect another dimension.

Pattern:

`A creates X -> B transforms X into Y -> C uses Y`

This is the characteristic mechanism of many three-plane architectures.

## 10. Affordance
A new action, option, or advantage made available by a state.

Examples:
- a partnership becomes negotiable,
- a financing instrument becomes viable,
- a technical migration becomes safer,
- a hiring profile becomes clearer,
- a launch window opens.

## 11. Constraint
A limit on possible actions.

Bridges may remove constraints or deliberately introduce useful constraints.

## 12. Option / Optionality
An action that becomes available but need not be taken.

Optionality is measured by:
- number of viable moves,
- reversibility,
- cost of keeping the option open,
- expiry,
- and strategic diversity of the moves.

## 13. Causal Chain
A sequence of bridges across two or more dimensions.

Example:

`A2 -> X -> B1 -> Y -> C3`

A chain should not be longer than necessary. Longer chains accumulate uncertainty.

## 14. Architecture
A complete arrangement of dimensions, plans, and bridges.

Multiple architectures can be generated from the same condition space.

## 15. Load-Bearing Bridge
A bridge whose failure materially damages the architecture.

Every architecture should identify its load-bearing bridges. This is a **host
model's hypothesis** relative to a named architecture: bridge `B` is
load-bearing for architecture `A` when removing `B` from the conceptual plan
makes a declared downstream objective unreachable. Test the claim by inspecting
downstream reachability with and without the bridge. The skill does not compute
or verify structural status; an optional host implementation may independently
analyze the graph, with a result separate from the model's `load_bearing` claim.

## 16. Redundant Bridge
An alternate causal path that preserves value if another bridge fails.

Redundancy is useful when reliability matters, but unnecessary redundancy increases complexity.

## 17. Bridge Strength
Recommended qualitative scale:
- `strong`: direct mechanism, low ambiguity, material effect.
- `moderate`: credible mechanism with meaningful contingencies.
- `weak`: plausible but indirect or low magnitude.
- `speculative`: insufficient evidence for planning reliance.

## 18. Effect Types
Canonical bridge effect types:

- `capability`
- `information`
- `access`
- `resource`
- `incentive`
- `constraint`
- `timing`
- `evidence`
- `attention`
- `risk`
- `optionality`
- `demand`
- `position`
- `permission`
- `coordination`
- `cost`
- `quality`
- `reliability`

Use multiple effect types only when necessary.

## 19. Local Objective vs. Meta Objective
- **Local objective:** what the dimension is trying to achieve internally.
- **Meta objective:** the higher-order purpose served by coordinating dimensions.

An action may serve both without being artificial.

## 20. Boundary
The point at which one dimension exposes or receives a state change.

Boundaries are where handoffs should be designed and monitored.

## 21. Signal
Evidence that a state or bridge is actually present.

A bridge without an observable signal is harder to manage.

## 22. Assumption
A proposition that must be true for a bridge or plan to work.

Assumptions should be:
- explicit,
- testable when possible,
- and assigned confidence.

## 23. Externality
A consequence affecting a dimension that was not the local target of the source action.

Cross-dimensional planning often deliberately turns useful externalities into designed bridges.

## 24. Failure Mode
A condition under which a plan, state transition, or bridge fails.

## 25. Architecture Complexity
A practical measure of:
- number of dimensions,
- number of bridges,
- number of load-bearing dependencies,
- number of probabilistic human responses,
- and synchronization burden.

Prefer the lowest complexity that preserves meaningful causal leverage.
