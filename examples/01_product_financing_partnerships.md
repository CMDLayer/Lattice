# Worked Example 1 — Product Validation, Financing, and Partnerships

## Scenario

A small software company has:
- a technically strong product,
- limited cash runway,
- low market awareness,
- several enthusiastic early customers,
- one possible distribution partner,
- and uncertainty about which enterprise use case will scale.

The company wants to reach a repeatable growth position without committing prematurely to a large sales team.

## Condition Space

**Objective:** Reach a credible, repeatable growth path while preserving runway.

**Constraints**
- limited cash,
- uncertain enterprise use case,
- low awareness,
- no large sales force.

**Assets**
- functioning product,
- enthusiastic early customers,
- candidate partner,
- founder expertise.

**Important uncertainty**
- which use case produces repeatable willingness to pay.

## Dimensions

### D1 — Product Validation
Local objective: identify and operationalize the strongest repeatable use case.

Independent plan:
1. Select 3–5 high-potential early customers.
2. Instrument usage and business outcomes.
3. Run structured pilot cycles.
4. Convert successful patterns into a repeatable deployment package.

### D2 — Financing
Local objective: extend runway on acceptable terms while reducing fundraising uncertainty.

Independent plan:
1. Build financial model and financing options.
2. Prepare data room.
3. Develop investor narrative around evidence, not projections alone.
4. Open conversations only when evidence threshold is met.

### D3 — Partnerships
Local objective: validate whether an external channel can lower distribution cost.

Independent plan:
1. Define partner value proposition.
2. Test fit with candidate partner.
3. Create limited-scope co-selling or referral experiment.
4. Measure sourced pipeline and operational burden.

## State Extraction

D1-A2 produces:
- credible usage data,
- measured outcome evidence,
- clearer use-case segmentation.

D1-A4 produces:
- repeatable deployment method,
- known onboarding effort,
- standardized case material.

D3-A2 produces:
- clear partner objections and requirements.

D3-A3 produces:
- external channel performance data,
- evidence of distribution economics.

## Bridge Discovery

### B1 — Product Validation → Financing
Source state:
credible measured usage/outcome evidence.

Mechanism:
financing conversations can rely on observed customer behavior rather than speculative projections.

Effect:
evidence + risk reduction.

Counterfactual:
without the evidence, investor diligence depends more heavily on assumptions and narrative.

Strength:
strong.

### B2 — Product Validation → Partnerships
Source state:
repeatable deployment package.

Mechanism:
a partner can evaluate and sell a packaged motion more easily than an improvised founder-led process.

Effect:
capability + access.

Strength:
strong.

### B3 — Partnerships → Product Validation
Source state:
partner objections and prospect patterns.

Mechanism:
these reveal whether the use case generalizes beyond the original customer set.

Effect:
information.

Strength:
moderate to strong.

### B4 — Partnerships → Financing
Source state:
measured channel economics.

Mechanism:
gives evidence about customer acquisition leverage and growth efficiency.

Effect:
evidence + risk.

Strength:
moderate.

## Architecture A — Staged Evidence Transformation

```text
D1 Product Validation
pilot → measured outcomes → repeatable package
                         │
                         ▼
D3 Partnerships
limited channel test → channel economics
                         │
                         ▼
D2 Financing
data room + investor process
```

Core chain:
`pilot evidence -> partner-ready package -> channel economics -> stronger financing evidence`

Why it works:
D3 transforms product evidence into distribution evidence. The middle plane is not a pass-through.

Tradeoff:
fundraising starts later, but with stronger evidence.

## Architecture B — Parallel Learning Convergence

```text
D1 Product evidence ───────┐
                           ├──> D2 Financing threshold
D3 Channel evidence ───────┘
```

Both D1 and D3 run in parallel, and financing begins only when enough uncertainty has been reduced.

Tradeoff:
faster learning, more simultaneous workload.

## Stress Test

If the partner channel fails:
- D1 still produces valuable product evidence.
- Financing can still proceed using direct customer proof.
- D3 failure itself becomes information about channel fit.

If pilot outcomes are mixed:
- do not activate fundraising bridge as "strong."
- preserve runway and use D3 prospect feedback to refine segmentation.

## Lesson

The company is not using product pilots "to raise money" in a simplistic sense. The pilots are locally necessary for product learning. Their consequences create evidence that financing and partnership dimensions can use.
