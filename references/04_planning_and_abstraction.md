# Reference Primer — Planning, Hierarchy, and Abstraction

## Horizontal planning

Each dimension needs a plan that can stand on its own.

Useful primitives:
- goals,
- subgoals,
- prerequisites,
- actions,
- decision points,
- exit conditions,
- partial ordering.

## Why partial order matters

Many actions need not be totally sequenced. Over-sequencing creates unnecessary dependencies.

CDCO benefit:
Independent dimensions can proceed asynchronously until a bridge requires synchronization.

## Abstraction levels

Do not mix:
- broad strategic objectives,
- projects,
- tasks,
- individual actions,
- and states
without naming the level.

A dimension should usually contain items at comparable planning resolution.

## Hierarchical decomposition

A large orchestration may contain sub-orchestrations.

Use recursion only when:
- the lower-level system has enough complexity to warrant it,
- its interfaces to the higher layer are clear.

## Agent questions

- What must be ordered?
- What can proceed independently?
- What is a goal versus a state?
- Are dimensions at a comparable level?
- Is recursion clarifying or merely adding complexity?
