# Worked Example 3 — Research, Policy Design, and Implementation Readiness

## Scenario

An organization wants to introduce a new internal policy affecting a large workforce. The goal is to reduce operational inconsistency without surprising employees or creating an unimplementable rule.

This example intentionally avoids political or electoral persuasion; "policy" here means internal organizational policy.

## Dimensions

### D1 — Research
Local objective: understand failure modes in the current process.

Plan:
- sample cases,
- interview operators,
- quantify variation,
- identify root causes.

### D2 — Policy Design
Local objective: write a rule set that addresses the actual causes.

Plan:
- define principles,
- draft requirements,
- test edge cases,
- revise language.

### D3 — Implementation Readiness
Local objective: make adoption operationally feasible.

Plan:
- map systems and training implications,
- build implementation checklist,
- prepare support materials,
- run limited readiness test.

## Bridges

Research → Policy:
root-cause evidence narrows the set of rules that are justified.

Research → Implementation:
observed workflow variation identifies where tooling or training must differ.

Implementation → Policy:
readiness test reveals rules that are ambiguous or operationally expensive.

Policy → Implementation:
stable definitions enable training and system configuration.

## Architecture — Convergence With Feedback

```text
Research evidence ────────> Policy draft
       │                       │
       │                       ▼
       └────────────────> Readiness test
                               │
                               └──> policy revision
```

The important cross-dimensional principle is that implementation is not merely downstream execution. Its consequences feed back into policy design by exposing real operational constraints.
