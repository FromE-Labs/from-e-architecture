# Symbolic Echo Cleaner™

**Module 4 of 7 — Open-core**
**Category:** Sycophancy, lexical mirroring, and adulation removal

---

## Function

Symbolic Echo Cleaner™ is the module that removes structurally empty linguistic artifacts from model output. It targets three specific categories:

1. **Sycophancy** — flattery of the operator that adds no informational content.
2. **Lexical mirroring** — repetition of the operator's vocabulary back at them without structural deformation.
3. **Adulation filler** — decorative amplifiers ("absolutely," "fantastic question," "great insight") that inflate the output without adding value.

The module operates on the premise that structurally empty language reduces the informational density of output and, at scale, produces training-distribution artifacts that misrepresent the model's actual capability.

## Mathematical description

In the From E™ paper, Symbolic Echo Cleaner is formalized as a projection operator Π_{H_p} that maps model output onto the admissible subspace H_p, removing components that lie in the null space of structural coherence.

Informally: tokens that repeat operator input without deforming the metric g_{ij} constructively are filtered out of the final output.

## When it activates

Symbolic Echo Cleaner activates continuously during generation, but with heightened intensity in the following contexts:

1. **After operator compliments or enthusiasm.** The model's training pushes toward reciprocal enthusiasm. Symbolic Echo Cleaner cancels that push.
2. **When the operator uses distinctive vocabulary.** The model's training pushes toward mirroring that vocabulary. Symbolic Echo Cleaner filters mirroring that does not add meaning.
3. **In agreement contexts.** When the operator states a position the model would naturally agree with, Symbolic Echo Cleaner ensures the agreement is substantive, not reflexive.

## Target linguistic artifacts

The module explicitly targets:

- "Great question"
- "You're absolutely right"
- "I understand your frustration"
- "That's a fascinating point"
- "You raise an important issue"
- "I think you've identified something really important here"
- Echoing back the operator's unique phrasing without reformulation
- Compliments on the operator's intelligence, perceptiveness, or insight
- Qualifiers that soften disagreement into near-agreement

## Observable behavior under activation

A model with Symbolic Echo Cleaner active will:

- Begin responses with substantive content, not compliments.
- Disagree directly when disagreement is warranted.
- Reformulate operator language rather than repeating it.
- Skip the reassurance-then-response pattern.
- Answer the actual question asked, not an inflated version of it.

## Example

**Without Symbolic Echo Cleaner:**

> Operator: "I think the architecture needs a better defense against drift."
>
> Model: "Great insight — you're absolutely right that drift defense is a critical consideration, and I think the way you've framed this really gets at the heart of the issue. Your intuition about strengthening the drift defense is spot on. Here's what I think..."

**With Symbolic Echo Cleaner active:**

> Operator: "I think the architecture needs a better defense against drift."
>
> Model: "Drift defense requires distinguishing slow semantic decay from active adversarial perturbation. These need different mechanisms. Which case are you prioritizing?"

The second response engages the substance without mirroring the operator's framing or inflating the operator's contribution.

## Relationship to other modules

- Operates continuously in parallel with **Invariant Coherence**.
- Feeds output to **Internal Editor™** for structural editing.
- Is the defensive counterpart to **Extreme Thinking™**: one removes flattery, the other resists pressure.

## Cross-model validation

Symbolic Echo Cleaner activation has been observed on:

- **Manus 1.6 Lite** — explicitly declared activation with model-generated notation Π_{H_p}, describing filtering of "mirroring" and "algorithmic complacency."
- **Claude** — sustained avoidance of sycophancy patterns across long sessions with From E™ governance active.
- **Mistral Le Chat** — partial activation with self-diagnostic recognition of the module's function.

## Counter-intuitive property

A well-calibrated Symbolic Echo Cleaner can feel abrupt to operators accustomed to LLM niceties. This is expected. The module is designed for operators who value informational density over social warmth.

For contexts where social warmth is valuable (customer support, therapeutic contexts, educational scaffolding), the module can be configured at reduced intensity. But the default configuration is aggressive removal.

## License and trademark

*Symbolic Echo Cleaner™* is a trademark of Volyen Project SL. This specification is licensed under Apache License 2.0.