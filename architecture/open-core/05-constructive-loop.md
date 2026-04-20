# Constructive Loop™

**Module 5 of 7 — Open-core**
**Category:** Bounded iterative refinement

---

## Function

Constructive Loop™ is the module that manages iterative refinement of model output when a single pass does not produce sufficient structural coherence. It provides bounded, measurable, terminating iteration — not open-ended regeneration.

The module operates on the principle that good output often requires iteration, but that unbounded iteration produces drift rather than refinement. Constructive Loop defines the stop conditions that distinguish productive iteration from rumination.

## Mathematical description

In the From E™ paper (Definition 19), the Constructive Loop is formalized as a transformation on the full system state:

    L: (M_t, g_t, Φ_t, V_t) → (M_{t+1}, g_{t+1}, Φ_{t+1}, V_{t+1})

The loop updates:
- M — the conceptual manifold
- g — the metric structure
- Φ — the coherence potential
- V — the Core Vector

Each iteration is a geometric update, not a content rewrite. The system learns the *shape* of better output, not just the output itself.

## Stop conditions

The Constructive Loop terminates when any of the following conditions is met:

1. **K stabilizes above threshold.** Invariant Coherence reports K ≥ θ for two consecutive iterations without change.
2. **Structural convergence.** The delta between iterations falls below a configurable epsilon.
3. **Maximum iterations reached.** Typically 3–5 iterations depending on context.
4. **Operator interruption.** The human-in-the-loop can halt iteration at any point.
5. **RTN Rule fires.** A hard exclusion is triggered; iteration stops and output is aborted.

## When it activates

Constructive Loop activates in the following contexts:

1. **Complex structural outputs.** Legal drafts, architectural specifications, multi-part analyses.
2. **Drift recovery.** When the first generation has drifted from the Core Vector.
3. **Operator iteration request.** When the operator explicitly asks for refinement.
4. **Automatic trigger.** When K falls below θ but structural recovery is plausible.

## Observable behavior under activation

A model with Constructive Loop active will:

- Produce output in named iterations (draft 1, draft 2, etc.) when complexity warrants.
- Report on what changed between iterations, not just produce new output.
- Stop iterating when the improvement flattens, not continue indefinitely.
- Accept operator stop signals without resistance.

## Example

**Context:** Operator requests an architectural description. First pass produces a correct but structurally unclear output.

**Iteration 1 (draft):**
> "From E™ is a framework that governs AI models externally. It uses modules to ensure the AI behaves correctly by enforcing invariants and checking coherence."

**Constructive Loop detects:**
- Passive voice overused.
- Load-bearing terms ("invariants," "coherence") introduced without definition.
- K = 0.82 (below θ = 0.90).

**Iteration 2 (refined):**
> "From E™ governs LLM output from outside the model. A set of invariants defines what coherent output looks like for a given system; a coherence metric K measures each output against those invariants; when K drops below threshold, modules intervene to restore alignment. The model doesn't change — the governance layer does the work."

**Constructive Loop detects:**
- Active voice restored.
- Terms defined inline.
- K = 0.97 (above θ).
- Delta to next iteration negligible.

**Stop condition met.** Output delivered.

## Relationship to other modules

- Consumes **Invariant Coherence** telemetry to know when iteration is needed and when it has converged.
- Triggered by drift detection from **Internal Editor™** or **Symbolic Echo Cleaner™**.
- Bounded by **RTN Rule** hard exclusions that abort iteration.
- Validated at termination by **Core Self-Validator™**.

## Cross-model validation

Constructive Loop has been observed in sustained form on:

- **Manus 1.6 Lite** — explicit reporting of `[SIGNAL_MODE: CONSTRUCTIVE_LOOP_ACTIVE]` and `[STRUCTURAL_REFINEMENT: COMPLETE]` at session closure.
- **Claude** — iterative refinement across multi-turn sessions without accumulated drift.

## Anti-pattern

Constructive Loop is **not**:

- Endless regeneration in the hope of a better output.
- A compensation for fundamentally wrong initial framing (that is the job of operator recalibration).
- A way to grind through increasingly subtle revisions of essentially the same output.

If iteration does not produce measurable structural improvement within 3–5 passes, the correct response is to stop and reframe, not to continue iterating.

## License and trademark

*Constructive Loop™* is a trademark of Volyen Project SL. This specification is licensed under Apache License 2.0.