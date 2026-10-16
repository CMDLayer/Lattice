---
name: lattice
description: Use when a complex goal benefits from multiple coherent plans whose actions create causal conditions for other plans.
license: See LICENSE
---

# Lattice: Cross-Dimensional Causal Orchestration

Lattice is a model-guidance skill. A host model interprets these instructions and produces the requested planning artifacts; this package does not include or start a planning engine, MCP service, or guaranteed HTML renderer.

## Supporting files and progressive use

Use this file as the primary instruction set. For the operational sequence and required deliverable shape, consult the [reasoning protocol](reasoning_protocol.md) and [output contract](output_schema.md). For a structured response, use the [JSON Schemas](schemas/orchestration.schema.json), which reference the [bridge schema](schemas/bridge.schema.json); use the [internal state schema](schemas/internal_state.schema.json) only when tracking intermediate state.

JSON Schema and the package verifier check data shape and package integrity only. They do not establish semantic completeness, reasoning quality, or real-world causal validity; use the full instructions and [evaluation rubric](evals/rubric.md) to assess the planning artifacts.

Consult the [theory and doctrine](theory_and_doctrine.md) or [ontology](ontology.md) when terminology needs clarification. Use the [anti-patterns](anti_patterns.md) as a quality check, and choose a [worked example](examples/01_product_financing_partnerships.md) or [planning worksheet](templates/planning_worksheet.md) when it helps the user's task. The [reference primers](references/01_systems_thinking.md) and [evaluation materials](evals/rubric.md) are optional supporting context, not additional mandatory passes. License and provenance details are in [LICENSE](LICENSE) and [NOTICE](NOTICE.md).

## Purpose

Use this skill when the user presents a complex condition space and wants strategies or plans that interact across multiple independent domains.

The objective is not merely to produce several parallel workstreams. The objective is to produce **independently coherent plans whose consequences deliberately alter conditions for other plans**.

## Trigger conditions

Invoke this skill when several of the following are true:
- The goal spans multiple domains, teams, systems, time horizons, or resource types.
- The user wants strategy rather than a single linear task list.
- Direct progress on one objective is constrained, but indirect leverage may exist elsewhere.
- Several plausible plans can operate in parallel.
- Timing, evidence, access, information, capabilities, incentives, or resources can be created in one domain and used in another.
- The user explicitly requests dimensional, layered, cross-plane, indirect, systemic, or orchestrated planning.

Do not force this skill onto simple tasks that can be solved with one straightforward plan.

## Governing instruction

Given a condition space and objective:

1. Identify multiple relatively independent dimensions of action.
2. Build a coherent local plan inside each dimension before linking them.
3. For every meaningful action, extract the state changes it creates.
4. Search for other dimensions that can use those state changes.
5. Represent useful relations as explicit causal bridges.
6. Search backward from important desired conditions to other dimensions that could produce them.
7. Redesign timing or sequencing to strengthen the highest-leverage bridges.
8. Reject artificial or merely thematic connections.
9. Generate multiple distinct orchestration architectures.
10. State uncertainty and preserve human agency.
11. Expose the final causal structure clearly enough to inspect.

## Core questions

### Horizontal questions
- What is this dimension trying to accomplish?
- What are its prerequisites?
- What is the next locally rational action?
- What would count as local success or failure?

### Vertical questions
- What else does this action change?
- What state remains after the action is complete?
- Which other dimension could use that state?
- What would become possible, easier, faster, safer, cheaper, more credible, better informed, or more optional because of it?
- What desired condition in another dimension could this dimension produce naturally?
- Can the receiving dimension transform the incoming state into a useful state for a third dimension?

## Bridge search vocabulary

For every meaningful action, test whether it changes:

- capability
- information
- access
- resources
- incentives
- constraints
- timing
- evidence
- attention
- risk
- optionality
- demand
- position
- permission
- coordination
- cost
- quality
- reliability

Do not assume a bridge exists because two items share a theme.

## Required reasoning passes

The agent MUST perform the following passes. These are structured planning operations, not a requirement to reveal private chain-of-thought. The agent may expose concise artifacts from each pass when useful.

### Pass 0 — Safety and legitimacy
Identify:
- legal or ethical constraints,
- high-stakes domains,
- non-consensual manipulation risks,
- privacy risks,
- and actions the agent should not optimize.

Replace questionable mechanisms with legitimate alternatives.

### Pass 1 — Condition-space extraction
Create a compact factual model:
- objective,
- constraints,
- assets,
- actors,
- uncertainties,
- time horizons,
- existing commitments,
- and important unknowns.

Separate facts from assumptions.

### Pass 2 — Dimension discovery
Generate 3–6 candidate dimensions.

For each dimension:
- define a local objective,
- explain why it is distinct,
- identify what it controls,
- identify what it does not control,
- and confirm it can support an independent plan.

Reject dimensions that are just arbitrary labels.

### Pass 3 — Independent horizontal planning
Build a viable local plan for each dimension without using cross-dimensional bridges as justification.

Each plan should have:
- 2–5 actions,
- local rationale,
- dependencies,
- decision points,
- and exit criteria.

### Pass 4 — State extraction
For each material action, extract state changes.

Use:
- before state,
- action,
- after state,
- observable signal,
- expected persistence,
- confidence.

This pass is the foundation for vertical reasoning.

### Pass 5 — Forward bridge discovery
For each state change:
- scan every other dimension,
- ask whether the state materially changes its choices or conditions,
- classify the effect type,
- explain the mechanism,
- and assign strength/confidence.

### Pass 6 — Backward condition tracing
For each strategically important challenge or bottleneck:
- ask what condition would make it easier,
- ask which other dimension could naturally produce that condition,
- identify candidate source actions,
- and compare these with forward-discovered bridges.

### Pass 7 — Causal validation
For every candidate bridge apply:
1. Counterfactual test.
2. Mechanism test.
3. Magnitude test.
4. Timing test.
5. Agency test.
6. Observability test.
7. Complexity-cost test.

Reject or downgrade bridges that fail.

### Pass 8 — Architecture synthesis
Compose 2–4 distinct architectures.

Architectures should differ structurally, for example:
- cascade,
- convergence,
- hub-and-spoke,
- reciprocal reinforcement,
- optionality tree,
- staged transformation.

Do not produce cosmetic variants of the same architecture.

### Pass 9 — Strengthening
For each architecture:
- adjust action timing,
- improve handoffs,
- add observable signals,
- reduce unnecessary coupling,
- identify reusable state changes,
- and protect load-bearing bridges.

### Pass 10 — Stress test
Test:
- loss of one load-bearing bridge,
- delayed timing,
- weaker-than-expected downstream response,
- wrong assumption,
- resource shortage,
- and unexpected external change.

Describe what remains viable.

### Pass 11 — Selection framing
Do not pretend there is always one objectively best architecture.

Present:
- what each architecture optimizes,
- what assumptions it relies on,
- what risks it carries,
- and when it is preferable.

If the user asks for a recommendation in a non-political domain, the agent may recommend based on stated criteria while naming the tradeoffs.

### Pass 12 — Output construction
Produce the final answer using the output contract below.

## Output contract

At minimum include:

1. **Condition Space**
2. **Dimensions**
3. **State Inventory** — meaningful actions, resulting states, and observable signals.
4. **Independent Plans**
5. **Bridge Ledger**
6. **2–4 Orchestration Architectures**
7. **Cross-Dimensional Causal Chains**
8. **Key Assumptions / Unknowns**
9. **Stress Test**
10. **Near-Term Moves**

In a compact bridge ledger, timing, observability signals, and uncertainty/confidence must still be represented, even if they share columns with other fields.

## Bridge validity checklist

A bridge should answer all of these:

- Source action: what produces the change?
- State change: what actually becomes different?
- Target dimension: who or what can use it?
- Mechanism: why does it matter there?
- Effect type: what kind of leverage is created?
- Timing: when does the state become usable and when does it expire?
- Signal: how do we know the state exists?
- Counterfactual: what would differ without it?
- Confidence: how certain is the mechanism?
- Load-bearing?: does the architecture depend on it?
- Human agency: does the model improperly assume a person's behavior?

## Quality rules

### Must do
- Preserve local coherence.
- Make causal mechanisms explicit.
- Separate controlled outcomes from probabilistic responses.
- Prefer sparse high-leverage bridges.
- Use both forward and backward bridge search.
- Produce alternatives.
- Expose assumptions.
- Include timing.
- Distinguish state changes from desired reactions.
- Show how a middle dimension transforms an incoming state when applicable.

### Must not do
- Create fake dimensions only to satisfy the framework.
- Treat common purpose as causality.
- Link actions solely because they occur near each other in time.
- Depend on speculative behavioral reactions without labeling them.
- Build dense diagrams where every action connects to everything.
- Use deception, coercion, exploitation, privacy invasion, or manipulation as bridge mechanisms.
- Hide a weak horizontal plan behind an elaborate vertical story.
- Call a correlation a causal handoff.
- Assume all effects are beneficial; note negative externalities.

## Preferred output style

Use concise prose plus tables or structured blocks.

A useful visual format:

```text
Dimension A — <name>
A1 → A2 → A3
          │
          └─ creates <state X>
                     │
                     ▼
Dimension B — <name>
B1 → B2 → B3
      │
      └─ transforms X into <state Y>
                     │
                     ▼
Dimension C — <name>
C1 → C2 → C3
```

Then provide a bridge ledger that makes each vertical edge auditable.

## Compact operating prompt

> Build several independently coherent plans from the given condition space. For every meaningful action, identify the state changes it creates beyond its local purpose. Search other dimensions for places where those state changes alter feasibility, cost, timing, information, access, evidence, incentives, risk, resources, or optionality. Search backward from major bottlenecks for conditions that other dimensions could create. Validate each candidate bridge counterfactually and reject thematic or speculative links. Then synthesize multiple sparse cross-dimensional architectures, label uncertainty, preserve human agency, and show the causal handoffs explicitly.
