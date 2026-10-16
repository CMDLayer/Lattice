# Worked Example 2 — Hiring, Operations, and Sales

## Scenario

A professional services firm is growing but has inconsistent delivery quality. Sales opportunities are increasing, but leadership is hesitant to hire aggressively because project staffing needs are unclear.

## Dimensions

### D1 — Operations
Local objective: make delivery repeatable and measurable.

Plan:
1. map project stages,
2. define standard operating checkpoints,
3. measure workload and rework,
4. create role-level capacity model.

### D2 — Hiring
Local objective: add capacity without over-hiring.

Plan:
1. define role archetypes,
2. build candidate pipeline,
3. sequence hires against observed capacity gaps,
4. establish onboarding.

### D3 — Sales
Local objective: improve conversion and sell work the firm can deliver well.

Plan:
1. segment opportunities,
2. standardize qualification,
3. refine scope templates,
4. prioritize high-fit deals.

## Bridges

### Operations → Hiring
State:
measured workload and role-level capacity model.

Mechanism:
hiring decisions can be tied to actual bottlenecks rather than intuition.

Effect:
information + risk reduction.

### Operations → Sales
State:
standardized delivery stages and scope boundaries.

Mechanism:
sales can qualify and scope deals that match reliable delivery patterns.

Effect:
quality + constraint.

### Sales → Hiring
State:
qualified pipeline by service type and expected start date.

Mechanism:
hiring can anticipate capacity needs with better timing.

Effect:
timing + information.

### Hiring → Operations
State:
new capacity in specific role.

Mechanism:
operations can relieve a verified bottleneck and test whether throughput improves.

Effect:
capability.

## Architecture — Reciprocal Reinforcement

```text
Operations measurement
      │
      ├──> Hiring precision
      │         │
      │         └──> bottleneck capacity
      │
      └──> Sales scoping discipline
                 │
                 └──> qualified demand timing
                              │
                              └──> Hiring sequencing
```

This architecture contains loops, but the loops are bounded by observable states.

## Anti-pattern avoided

Bad plan:
"Sell more, then hire more, then improve operations."

That is linear and reactive.

CDCO plan:
Use operations to create capacity evidence, use sales to create demand timing evidence, and let both inform hiring. Hiring then changes operations capability.
