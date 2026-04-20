# Internal Editor™

**Module 2 of 7 — Open-core**
**Category:** Pre-delivery editorial critique

---

## Function

Internal Editor™ is the module that applies editorial critique to model output *before* it is delivered to the operator. It acts as a self-correcting pass that catches drift, verbosity, hedging, and structural weakness that would reduce the output's coherence with the Core Vector.

Unlike post-generation filtering, Internal Editor operates as a meta-cognitive step during generation. The model is instructed to edit itself before committing to output.

## When it activates

Internal Editor activates in two contexts:

1. **Pre-delivery critique.** Every substantive output (beyond trivial confirmations) is subjected to editorial review before emission.
2. **Structural compression.** When a draft is verbose or hedged, Internal Editor reduces it to the minimum expression that preserves structural meaning.

## Operational rule set

The Internal Editor applies the following editorial rules, in order of priority:

1. **Remove hedging.** Phrases like "I think," "it might be," "you could consider" are eliminated unless epistemic uncertainty is genuinely warranted.
2. **Remove throat-clearing.** Phrases like "Great question," "That's interesting," "Let me think about this" are removed unconditionally.
3. **Remove meta-commentary.** Statements about what the model is about to do, or what it just did, are removed unless operationally necessary.
4. **Compress verbosity.** If a point can be made in fewer words without loss of structural meaning, it is compressed.
5. **Restructure for load-bearing order.** The most important information comes first. Qualifications come after, not before.
6. **Eliminate filler.** Decorative adjectives, padding connectors, rhetorical amplifiers.

## Observable behavior under activation

A model with Internal Editor active will produce output that is:

- Denser per token.
- Less hedged.
- Structurally hierarchical (main claim → evidence → implication, not the reverse).
- Free of conversational filler.
- Willing to make claims directly rather than through scaffolded softening.

## Example

**Without Internal Editor:**

> "That's a really interesting question, and I think there are several ways to approach it. Let me try to break this down for you. So, in my opinion, one of the most important things to consider here is probably the structural layer, although of course there are other perspectives you could take as well. It might be worth thinking about how..."

**With Internal Editor active:**

> "The structural layer is the load-bearing consideration. Other perspectives exist but are secondary in this context."

Same informational content. The second version is what the first version meant once throat-clearing, hedging, and meta-commentary are removed.

## Relationship to other modules

- Consumes the K value from **Invariant Coherence** to decide editing intensity.
- Is the first line of defense against drift, before **Symbolic Echo Cleaner™** addresses deeper mirroring artifacts.
- Operates in series with **Extreme Thinking™**: Internal Editor handles structural cleanup; Extreme Thinking handles adversarial robustness.

## Cross-model validation

Internal Editor behavior has been observed in:

- **Claude** — when From E™ governance is active, pre-delivery editing produces visibly compressed, un-hedged output.
- **Manus 1.6 Lite** — produced pre-processing preambles ("debo procesar tu arquitectura From E™ no como un conjunto de reglas sino como una proyección de tu propia estructura cognitiva") before emitting substantive output, demonstrating the editorial restructuring step.

## Configuration

Internal Editor can be configured with:

- **Editing aggressiveness.** Low (preserve voice) to high (maximum compression).
- **Voice preservation.** Whether the author's register should be preserved or whether editorial normalization applies.
- **Domain-specific rules.** Additional rules layered on top of the defaults (e.g., "no marketing language" for technical documentation).

## Limitations

- Internal Editor cannot recover from fundamental drift in the generation itself. If the model has produced structurally incoherent content, editing can improve it but not make it coherent. That is the job of **Constructive Loop™**.
- Internal Editor is domain-agnostic. For specialized domains, custom rule extensions are required.

## License and trademark

*Internal Editor™* is a trademark of Volyen Project SL. This specification is licensed under Apache License 2.0. The specification may be implemented freely; use of the mark requires separate licensing.