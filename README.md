# Cross-Dimensional Causal Orchestration (CDCO)
## Agent Skill Development Kit

**Version:** 0.1  
**Purpose:** Train an agent to generate multiple independently coherent plans whose consequences deliberately create useful causal conditions across different dimensions of activity.

This kit treats cross-dimensional orchestration as a planning framework rather than a deterministic control model. The central premise is simple:

> A plan should be evaluated not only by what its actions accomplish locally, but also by what conditions those actions create for other plans.

The kit is intended for agents that receive a set of conditions, objectives, constraints, uncertainties, and available capabilities, then produce several strategies whose internal plans are both independently rational and causally connected across dimensions.

## Core idea

Traditional planning mostly asks:

`What should happen next inside this plan?`

CDCO adds a second question:

`What else does this action change, and which other plan can use that change?`

A cross-dimensional architecture is therefore built from:

1. **Dimensions** — relatively independent domains of action.
2. **Plans** — coherent sequences inside each dimension.
3. **Actions** — interventions within a plan.
4. **State changes** — new conditions produced by actions.
5. **Bridges** — causal relationships through which a state change becomes relevant to another dimension.
6. **Handoffs** — moments when an effect in one dimension becomes an input, enabler, constraint, signal, resource, or opportunity in another.
7. **Orchestration** — the deliberate sequencing of several such bridges without assuming full control of downstream events.

## Design principles

- **Causality over cleverness.** A proposed bridge must change something real, not merely sound related.
- **Independent coherence.** Each dimension should make sense on its own.
- **Conditionality over certainty.** Bridges often change feasibility, probability, cost, timing, information, access, risk, or optionality rather than guaranteeing outcomes.
- **Sparse leverage.** Prefer a few meaningful bridges to dense artificial interconnection.
- **Forward and backward reasoning.** Search both from action → consequence → consumer and from desired condition → possible producer.
- **Uncertainty is native.** The method orchestrates in imperfect environments; it does not pretend to eliminate uncertainty.
- **Human agency is a constraint.** Do not model manipulation, coercion, deception, or exploitation as acceptable bridge mechanisms.

## Package contents

- `SKILL.md` — primary agent skill instructions.
- `theory_and_doctrine.md` — compact theory, definitions, and governing principles.
- `ontology.md` — terms and formal objects.
- `reasoning_protocol.md` — required multi-pass planning procedure.
- `internal_representations.md` — structured intermediate representations.
- `output_schema.md` — human-readable output contract.
- `anti_patterns.md` — failure modes and prohibited shortcuts.
- `reference_curriculum.md` — intellectual foundations and topics to teach.
- `references/` — concise topic primers suitable for retrieval or agent context.
- `training_cases.md` — progressive training curriculum and additional scenario prompts.
- `templates/` — reusable prompt and worksheet templates.
- `schemas/` — JSON Schemas for machine-readable plans and bridges.
- `examples/` — worked cases showing the framework in practice.
- `evals/` — evaluation rubric, benchmark cases, evaluator prompts, and expected characteristics.

## Recommended implementation pattern

Use CDCO as a **planning skill**, not as the agent's entire identity. The agent should first understand the user's real objective and factual situation, then invoke this skill when the problem benefits from multiple interacting lines of action.

The agent should generally produce:
- 3–6 dimensions,
- 2–5 horizontal actions per dimension,
- 2–6 high-quality cross-dimensional bridges,
- 2–4 alternative orchestration architectures,
- explicit assumptions and uncertainty,
- a bridge ledger that explains why each bridge is causal,
- and a short stress test showing how the architecture behaves if one bridge fails.

The framework should scale down when the problem is simple and scale up when the environment has more actors, constraints, time horizons, or independent workstreams.

## Minimal mental model

```text
Dimension A:  A1 → A2 → A3
                       │
                       │ creates condition X
                       ▼
Dimension B:  B1 → B2 → B3
                   │
                   │ transforms X into Y
                   ▼
Dimension C:  C1 → C2 → C3
```

The important object is not the vertical line itself. It is the claim that **condition X is a genuine consequence of A3, and condition X materially changes what is possible, likely, timely, affordable, knowable, or advantageous on Dimension B.**

That claim must survive scrutiny.
