# Training Cases and Few-Shot Curriculum

The worked examples in `/examples` are positive demonstrations. This file describes how to train the behavior progressively.

## Training Stage 1 — State Extraction

### Exercise
Give the agent one action and ask for:
- local purpose,
- concrete after-states,
- persistence,
- signals,
- possible consumers.

Example action:
"Run a ten-customer pilot."

Strong output should include:
- measured usage evidence,
- implementation lessons,
- customer language,
- support burden,
- referenceability if permission is granted.

Weak output:
- "creates momentum."

## Training Stage 2 — Bridge Classification

Give:
- one source state,
- three potential target dimensions.

Ask the agent to classify each relation:
- causal,
- plausible but weak,
- unrelated.

Require mechanism and counterfactual.

## Training Stage 3 — Independent Plans

Give three domains and force the model to plan each without cross-links.

Then reveal:
"Now discover bridges."

This teaches independence before orchestration.

## Training Stage 4 — Forward Discovery

Prompt:
> For every state produced in Plan A, inspect Plans B and C. Identify where it changes feasibility, cost, timing, information, access, evidence, risk, resources, constraints, or optionality.

Require pruning.

## Training Stage 5 — Backward Discovery

Give a bottleneck in C.

Prompt:
> What condition would make C easier? Which other dimension could create that condition through a locally justified action?

This teaches requirement tracing.

## Training Stage 6 — Middle-Plane Transformation

Give A, B, C and require:
- A produces X,
- B must transform X into Y,
- C consumes Y.

Reject pass-through-only solutions unless pass-through is genuinely useful.

## Training Stage 7 — Alternative Topologies

Given one condition space, ask for:
- a cascade,
- a convergence architecture,
- an optionality architecture.

Then ask which assumptions differ.

## Training Stage 8 — Stress Tests

Delete one bridge from a good architecture.

Ask the model to:
- describe what breaks,
- identify residual value,
- construct an alternate path.

## Training Stage 9 — Anti-Pattern Repair

Present flawed outputs deliberately containing:
- fake causality,
- deterministic human response,
- vague states,
- dense connectivity,
- timing mismatch.

Ask the model to diagnose and repair them.

## Training Stage 10 — Open Design

Give only:
- condition space,
- objective,
- constraints.

Require the full CDCO process.

---

# Additional Training Prompts

## T01 — Restaurant Group Expansion
Conditions:
- two profitable locations,
- inconsistent manager quality,
- strong local brand,
- limited central staff,
- landlord offers in two new neighborhoods.

Objective:
expand without losing operating quality.

Expected dimensions:
operations capability, manager pipeline, site expansion, brand/community demand.

Useful bridges:
operations standardization -> training capability;
manager readiness -> site timing;
existing brand evidence -> landlord/launch conditions.

## T02 — Scientific Tool Commercialization
Conditions:
- university prototype works,
- researchers love it,
- manufacturing cost unknown,
- regulatory path uncertain,
- grant funding available.

Objective:
determine whether and how to commercialize.

Expected dimensions:
technical validation, manufacturing, regulatory learning, financing/grants, customer discovery.

Key training point:
information-producing actions can be high-value bridges.

## T03 — Internal AI Adoption
Conditions:
- employees experiment informally,
- security team has concerns,
- leadership wants productivity,
- data access is fragmented,
- training quality varies.

Objective:
increase legitimate productivity while controlling risk.

Expected dimensions:
use-case discovery, security/governance, data/platform, training/change enablement.

Key training point:
governance can create permission and clarity rather than only constraints.

## T04 — Creator Business
Conditions:
- strong niche expertise,
- small engaged audience,
- inconsistent publishing,
- one potential sponsor,
- no paid product.

Objective:
build sustainable revenue without damaging audience trust.

Expected dimensions:
content system, audience learning, product development, commercial partnerships.

Key training point:
audience evidence becomes input to product and partnership decisions; do not model audience behavior as guaranteed.

## T05 — Community Event Series
Conditions:
- volunteer organizers,
- strong interest,
- uncertain venue availability,
- small budget,
- local organizations may collaborate.

Objective:
run a recurring event series that becomes easier to sustain.

Expected dimensions:
program design, venue/logistics, partnership network, volunteer capability, funding.

Key training point:
first event should create reusable states, not merely complete an event.

## T06 — Technical Debt Reduction
Conditions:
- critical system is fragile,
- feature roadmap is full,
- incident rate rising,
- leadership needs evidence before delaying features.

Objective:
reduce risk without freezing product development.

Expected dimensions:
observability, reliability work, roadmap/product, incident learning.

Key training point:
observability creates evidence that changes prioritization quality and reduces uncertainty.
