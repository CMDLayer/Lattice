# Reference Curriculum

CDCO is a custom synthesis. The agent should not be trained to imitate one discipline; it should borrow useful primitives from several.

## Tier 1 — Essential Foundations

### 1. Systems Thinking
Teach:
- system boundaries
- feedback loops
- stocks and flows
- delays
- leverage points
- unintended consequences
- emergence
- local optimization vs. system optimization

Why it matters:
CDCO requires the agent to reason about indirect consequences without assuming full control.

Suggested grounding:
- Donella Meadows, *Thinking in Systems*
- system dynamics concepts associated with Jay Forrester

### 2. Causal Reasoning
Teach:
- causal graphs
- mediation
- interventions
- counterfactuals
- confounding
- necessary vs. sufficient conditions
- causal mechanisms

Why it matters:
The agent must distinguish real bridges from narrative associations.

Suggested grounding:
- Judea Pearl and colleagues on causal inference
- practical counterfactual reasoning

### 3. Multilayer / Multiplex Networks
Teach:
- layers
- intra-layer vs. inter-layer edges
- bridge nodes
- multilayer dependency
- cascades
- network robustness

Why it matters:
Provides a formal vocabulary for separate planes with inter-layer relations.

Suggested grounding:
- multilayer network science
- multiplex network models

### 4. Hierarchical and Partial-Order Planning
Teach:
- decomposition
- prerequisites
- task networks
- partial order
- decision points
- conditional planning

Why it matters:
Horizontal plans should remain coherent before cross-layer composition.

### 5. Decision-Making Under Uncertainty
Teach:
- expected value
- scenario analysis
- robust decision-making
- real options
- value of information
- reversible vs. irreversible decisions

Why it matters:
Bridges often change probability or optionality rather than guarantee outcomes.

## Tier 2 — High-Value Supporting Topics

### 6. Cybernetics and Control
Teach:
- state
- observation
- feedback
- controller
- disturbance
- stability
- controllability vs. observability

Important adaptation:
CDCO is not a total-control theory. Use control concepts to understand state and feedback, not to assume control over independent agents.

### 7. Operations Research
Teach:
- constraints
- resource allocation
- scheduling
- bottlenecks
- critical paths
- dependency graphs
- sensitivity analysis

Why it matters:
Prevents strategically clever but operationally impossible architectures.

### 8. Distributed Systems / Event-Driven Architecture
Teach:
- loose coupling
- interfaces
- event publication
- message queues
- asynchronous systems
- failure isolation
- retries
- idempotence
- orchestration vs. choreography

Why it matters:
A useful analogy for plans that remain independent but exchange state through constrained interfaces.

### 9. Organizational Design
Teach:
- coordination costs
- modularity
- boundary objects
- cross-functional work
- centralized vs. distributed decision rights
- loosely coupled organizations

Why it matters:
Many real orchestrations cross teams rather than abstract domains.

### 10. Strategy
Teach:
- shaping conditions
- sequencing
- indirect approaches
- capability building
- optionality
- strategic positioning
- complementary assets
- resource leverage

Why it matters:
CDCO is fundamentally about producing advantageous conditions, not just completing tasks.

## Tier 3 — Specialized Topics

### 11. Game Theory
Teach:
- incentives
- strategic interaction
- signaling
- commitment
- coordination games
- information asymmetry

Use carefully:
Do not model human choice as mechanically controllable.

### 12. Mechanism Design
Teach:
- rules that shape incentives
- participation constraints
- information elicitation
- voluntary choice

Why it matters:
Useful when a plan changes the environment in which independent actors choose.

### 13. Resilience Engineering
Teach:
- graceful degradation
- redundancy
- fault containment
- adaptive capacity
- early warning signals

Why it matters:
Cross-dimensional architectures can create cascading failure if over-coupled.

### 14. Bayesian Reasoning
Teach:
- updating
- priors
- evidence
- uncertainty calibration
- likelihood

Why it matters:
Many bridges are probabilistic and evidence-producing.

### 15. Real Options
Teach:
- option value
- staged commitment
- preserving choices
- exercise conditions
- expiry

Why it matters:
A state change can be strategically valuable because of future choices it creates.

### 16. Information Theory (lightweight)
Teach:
- information gain
- entropy reduction
- signal vs. noise

Why it matters:
Some actions are valuable mainly because they reduce uncertainty for another dimension.

### 17. Constraint Theory / Bottleneck Analysis
Teach:
- limiting constraints
- throughput
- buffer
- exploitation and elevation of constraints

Why it matters:
Backward bridge search often starts from bottlenecks.

## Reference Concepts to Encode Directly

The agent should have concise reference notes for:
- causal mediation
- counterfactual tests
- feedback loops
- leverage points
- path dependence
- optionality
- loose coupling
- bridge centrality
- cascading failure
- robustness
- observability
- controllability
- event-driven systems
- boundary objects
- synchronization windows
- reversible decisions
- value of information
- complementary assets
- second-order effects
- externalities

## Topics That Should NOT Dominate the Skill

Avoid over-weighting:
- totalizing predictive models,
- deterministic control theory applied to people,
- elaborate game-theoretic manipulation,
- abstract graph metrics without causal meaning,
- narrative strategy language without operational state changes.

The agent's practical unit is always:
`action -> state change -> causal effect on another dimension`.
