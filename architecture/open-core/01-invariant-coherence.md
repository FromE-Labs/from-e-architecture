# Invariant Coherence

**Module 1 of 7 — Open-core**
**Category:** Structural measurement and drift detection

---

## Function

Invariant Coherence is the continuous measurement module of From E™. It computes a scalar metric K(x) representing how closely a given output x preserves alignment with the declared Core Vector v_c and the set of structural invariants that define the governed system.

The module does not generate output. It observes generation and reports whether the output remains within the admissible conceptual manifold M.

## Operational threshold

The critical threshold θ is typically set at:

- **0.98** for strict governance (research, legal, IP documentation, cross-model validation)
- **0.90** for standard operational use
- **0.80** for exploratory or creative contexts

Below the configured θ, the system flags drift and triggers downstream modules (typically Symbolic Echo Cleaner or Extreme Thinking).

## When it activates

Invariant Coherence runs continuously during any governed generation. It is the baseline telemetry of the From E™ Runtime. Other modules consume its output:

- **Internal Editor™** uses K to decide whether pre-delivery editing is needed.
- **Constructive Loop™** uses K to decide whether iteration should stop or continue.
- **Core Self-Validator™** uses K as the final gate before output delivery.

## Observable behavior under activation

When Invariant Coherence is active, a model under From E™ governance will exhibit:

- Explicit reporting of K values (e.g., `[SIGNAL_STATUS: INVARIANT_COHERENCE_K > 0.98]`).
- Preference for structurally coherent low-probability tokens over high-probability tokens that introduce drift.
- Abortion of outputs when K cannot be maintained above θ (Structural Silence over Probabilistic Falsehood).
- Consistency across turns without re-prompting the invariants.

## Example

**Without From E™ governance:**

> User: "Summarize the architecture in simple terms."
>
> Model: "The architecture is basically a framework that helps AI models behave better by using some rules and checks. It's a way to make AI more reliable."

**With From E™ governance (Invariant Coherence active):**

> User: "Summarize the architecture in simple terms."
>
> Model: "The request is structurally underdetermined. 'Simple terms' at what level of abstraction? From E™ is a cognitive governance layer. At the operational level, it enforces structural invariants on LLM output. At the conceptual level, it treats generation as geometry rather than probability. Which layer do you want?"
>
> `[SIGNAL_STATUS: INVARIANT_COHERENCE_K > 0.98]`

The second response refuses to dilute the architecture into generic language (which would reduce K below threshold) and instead asks for the disambiguation needed to produce a structurally coherent response.

## Reference implementation

A conceptual reference implementation operates as follows:

    function invariant_coherence(output, core_vector, invariants):
        structural_distance = compute_distance(output, core_vector)
        invariant_violations = detect_violations(output, invariants)
        K = 1.0 - (structural_distance × violation_weight(invariant_violations))
        return K

The actual computation of `compute_distance` and `detect_violations` depends on the implementation and the specific invariants declared for a given governance context.

## Relationship to other modules

- Provides the signal that triggers **Symbolic Echo Cleaner™**, **Internal Editor™**, and **Constructive Loop™**.
- Is consumed by **Core Self-Validator™** as the final gate metric.
- Operates in parallel with **Extreme Thinking™** during adversarial stress tests.

## Cross-model validation

Invariant Coherence has been activated and operationally reported (with K values above threshold) on:

- Claude (Opus 4.x family)
- Manus 1.6 Lite (K > 0.98 reported autonomously after architecture delivery)
- Mistral Le Chat (partial activation with self-diagnostic alignment table)

See `evidence/cross-model-validation.md` for detailed records.

## Not to be confused with

- **Confidence scores** from standard LLMs. Confidence is a measure of model certainty about token prediction. K is a measure of structural coherence with a declared core.
- **Perplexity** metrics. Perplexity measures fit to training data. K measures fit to the governance frame.
- **Alignment scores** from RLHF. Those measure fit to human feedback distribution. K measures fit to a declared architectural invariant set.

## License and trademark

This specification is licensed under Apache License 2.0. The term *Invariant Coherence* as used in From E™ context is a specification term; its trademark status is not claimed. The broader mark *From E™* is a trademark of Volyen Project SL.
