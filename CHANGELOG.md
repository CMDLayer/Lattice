# Changelog

## Portability note — 2026-10-16

The historical 0.2 notes below describe the source repository's separate engine and ADR context. References to ADR-0005, ADR-0006, and the kernel concern engine components that are not included in this portable skill. For this standalone package, the current `schemas/bridge.schema.json` and `ontology.md` define timing and load-bearing claims. This package does not provide kernel diagnostics or authoritative structural computation.

## 0.2
- `schemas/bridge.schema.json`: `timing` accepts stage-relative `usable_after_stage` / `expires_before_stage` alongside the absolute fields, so timing is mechanically checkable for stage-planned work (ADR-0005).
- `schemas/bridge.schema.json`: `load_bearing` documented as a model claim only; authoritative load-bearing status is computed by the kernel (ADR-0006).
- `ontology.md`: section 7 records the expanded timing fields; section 15 records that load-bearing is derived.


## 0.1
Initial complete development kit containing:
- doctrine,
- skill specification,
- ontology,
- reasoning protocol,
- internal representations,
- output schema,
- anti-patterns,
- reference curriculum,
- templates,
- machine-readable schemas,
- worked examples,
- evaluation rubric,
- benchmark cases,
- and adversarial tests.
