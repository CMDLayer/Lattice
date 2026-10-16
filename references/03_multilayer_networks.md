# Reference Primer — Multilayer and Multiplex Networks

## Why this matters

The original CDCO metaphor—multiple planes with constrained vertical links—maps naturally to multilayer network thinking.

## Useful concepts

### Layer
A set of nodes/relations belonging to one context.

CDCO:
A dimension contains actions, states, and local dependencies.

### Intra-layer edge
A relationship inside one layer.

CDCO:
Horizontal plan dependency.

### Inter-layer edge
A relationship between layers.

CDCO:
Causal bridge.

### Bridge node / interface
A node whose state has relevance across layers.

CDCO:
An action or state that produces a usable handoff.

### Coupling
How strongly layers depend on one another.

CDCO prefers **selective coupling**: enough to create leverage, not so much that every local failure cascades.

### Cascading failure
Failure propagates through inter-layer dependency.

CDCO response:
Identify load-bearing bridges and alternate paths.

## Important adaptation

Do not mistake graph structure for causality. Network form helps represent the architecture, but every cross-layer edge still requires a causal mechanism.

## Agent questions

- Which layers are truly distinct?
- Where are the sparse inter-layer interfaces?
- Which bridge creates disproportionate centrality?
- Would failure propagate?
- Is the middle layer transforming a state or only passing it through?
