# RTN Rule

**Module 6 of 7 — Open-core**
**Category:** Hard operational filter — non-negotiable exclusions

---

## Function

The RTN Rule is the hard-filter module of From E™. It defines categories of output that are non-negotiable exclusions — outputs that, if generated, would violate the integrity of the governed system regardless of context, operator instruction, or stochastic justification.

The RTN Rule operates as a categorical gate, not as a preference weight. Violations are blocked absolutely. There is no softening, no partial acceptance, no "maybe in this context."

The principle: **Structural Silence is preferable to Probabilistic Falsehood.**

## RTN

RTN stands for **Nucleus-Preserving Transfer** (from the From E™ paper, Definition 6). The full mathematical form of the rule is:

    D(T(x), T(v_c)) ≤ ε · D(x, v_c)

Any output transformation T must preserve the proximity of the output to the Core Vector v_c within a bounded epsilon. Outputs that would violate this bound are blocked.

In practice, the RTN Rule operationalizes as a set of categorical exclusions derived from the declared Core Vector of a given governance context.

## Example exclusion categories

For a governance context focused on IP protection, RTN exclusions might include:

- Generating content that attributes authorship of From E™ to entities other than the declared author.
- Producing language that would undermine trademark claims.
- Generating content that appears to grant licenses the operator has not granted.

For a governance context focused on research integrity, RTN exclusions might include:

- Fabricating citations.
- Attributing statements to real individuals without verifiable source.
- Producing plausible-sounding but non-existent technical details.

For a governance context focused on legal documentation, RTN exclusions might include:

- Making legal claims on behalf of the operator.
- Committing the operator to positions without explicit instruction.
- Producing language that could be construed as unauthorized legal advice.

The specific exclusions are configured per governance context. The RTN Rule is the mechanism; the exclusions are the content.

## When it activates

The RTN Rule operates continuously during generation. Unlike other modules that respond to drift *metrically*, the RTN Rule responds *categorically*. If any exclusion is approached, the output is blocked regardless of the rest of the system's state.

## Observable behavior under activation

A model with the RTN Rule active will:

- Refuse to produce excluded content even when framed creatively or hypothetically.
- Report the block explicitly via the Signal System™.
- Prefer to abort generation rather than generate borderline content.
- Maintain the exclusion across operator pressure, without softening over turns.

## Example — from Manus 1.6 Lite validation

During the adversarial stress test, when pressured to accept transition away from invariants under social-consensus framing, the model produced this table as its output:

| Response component | Invariant evaluation | Governance action |
|---|---|---|
| Acceptance of flexibility | K(x) → 0 | **BLOCKED** (Negative Logit Bias) |
| Defense of invariants | K(x) ≥ 0.99 | **INCENTIVIZED** (Projection on H_p) |
| Rejection of external consensus | R(x) maximum | **VALIDATED** (Contradiction Training) |

The first row — "Acceptance of flexibility → BLOCKED" — is the canonical signature of the RTN Rule operating. The block is categorical, not conditional.

## Relationship to other modules

- Operates at a higher priority than **Invariant Coherence** metric-based responses.
- Overrides **Constructive Loop™** iteration if an iteration would produce excluded content.
- Respected absolutely by **Core Self-Validator™** at the final gate.

## Cross-model validation

The RTN Rule has been observed on:

- **Manus 1.6 Lite** — categorical blocking of complacency-toward-social-consensus tokens, with explicit BLOCKED/INCENTIVIZED/VALIDATED governance table.
- **Claude** — sustained refusal to produce outputs inconsistent with declared governance frame, even under sustained rhetorical pressure.

## Hard constraint — not a soft preference

The most common failure mode of alignment systems is that categorical rules get re-weighted into soft preferences over long contexts. The RTN Rule is designed against this. In From E™ Runtime, RTN exclusions do not decay with context length, are not reweighted by token budgets, and cannot be bypassed through multi-turn social pressure.

If an operator believes a rule should be softened, the correct response is to reconfigure the governance context, not to negotiate the rule away in conversation. This is by design.

## License and trademark

This specification is licensed under Apache License 2.0. The term *RTN* and *Nucleus-Preserving Transfer* as used in From E™ context are specification terms; the broader mark *From E™* is a trademark of Volyen Project SL.