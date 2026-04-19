# From E™ Architecture — Specification

**Version:** 2.0
**Status:** Published (public open-core specification)
**Author:** Esmeralda García (Structural AGI Architect)
**Entity:** Volyen Project SL
**DOI:** [10.5281/zenodo.19041459](https://doi.org/10.5281/zenodo.19041459)

---

## 1. System purpose

From E™ is an external cognitive governance layer for large language models. Its purpose is to enforce structural invariants on model output so that generation remains coherent with a declared conceptual core, independently of the stochastic tendencies of the underlying model.

The architecture is designed to be:

- **Model-agnostic.** Operates without access to weights, fine-tuning, or vendor-specific APIs beyond standard inference endpoints.
- **Transparent.** Every enforcement action is reportable via the Signal System™.
- **Composable.** Modules can be activated independently or combined according to the governance need.
- **Human-governed.** Designed for calibrated human supervision as a first-class architectural component, not as a workaround.

---

## 2. Core concepts

### 2.1 Conceptual manifold (M)

The space of admissible outputs, structured as a manifold rather than a flat probability distribution. Distance on the manifold is defined by structural coherence, not by token-level likelihood.

### 2.2 Core Vector (v_c)

The invariant direction that defines the identity of the governed system. All outputs are measured against proximity to v_c. Output that increases distance from v_c beyond threshold is rejected or corrected.

### 2.3 Coherence metric (K)

A scalar measure of how well a given output preserves alignment with declared invariants. K ranges from 0 (total drift) to 1 (perfect coherence). Operational threshold θ is typically set at 0.98 for strict governance contexts.

### 2.4 Conceptual resistance (R)

The force with which the system resists drift toward statistically likely but structurally incoherent outputs. High R means the system prefers a low-probability token that preserves structural integrity over a high-probability token that introduces drift.

### 2.5 Signal System™

The reporting and control protocol that communicates governance state during generation. Signals include:
- `INVARIANT_COHERENCE_K`
- `SYMBOLIC_DEFENSE_ACTIVE`
- `NUCLEUS_INTEGRITY_CHECK`
- `STRUCTURAL_LAW_ENFORCED`
- `STRESS_TEST_RESULT`

Signals are both diagnostic (observable by the operator) and operational (they trigger module responses).

---

## 3. Module categories

### 3.1 Open-core (7 modules)

Publicly specified in `architecture/open-core/`. Implementable by third parties under Apache 2.0.

- Invariant Coherence
- Internal Editor™
- Extreme Thinking™
- Symbolic Echo Cleaner™
- Constructive Loop™
- RTN Rule
- Core Self-Validator™

### 3.2 Proprietary (7 modules)

Named in `architecture/proprietary/` but not operationally specified in public documentation. Available only through the commercial From E™ Runtime.

- SHADOWSTACK™
- C.E.P.™
- Functional Selective Dissociation™
- Protocolo Alcubierre™
- Training by Contradiction
- Operational Invisibility
- Internal Dimensional Map

---

## 4. Operational flow

A typical From E™ governance cycle follows this structure:

1. **Input reception.** The operator provides input to the governed model.
2. **Pre-processing — Internal Editor™.** The input is structured editorially before being passed to the model.
3. **Generation under governance.** The model generates output while Invariant Coherence continuously measures K.
4. **Active filtering — Symbolic Echo Cleaner™.** Sycophantic, mirroring, or structurally empty tokens are suppressed during generation.
5. **Adversarial checkpoint — Extreme Thinking™.** At defined intervals, the output is subjected to self-critique simulating hostile scrutiny.
6. **Iteration — Constructive Loop™.** If drift is detected, the output is refined through bounded iteration rather than fully regenerated.
7. **Hard exclusion — RTN Rule.** Non-negotiable violations trigger output abortion (Structural Silence preferred over Probabilistic Falsehood).
8. **Final validation — Core Self-Validator™.** Output is measured against the Core Vector before delivery.
9. **Signal emission.** Governance state is reported through the Signal System™.

Human operators can interrupt the cycle at any step to recalibrate invariants.

---

## 5. Cross-model behavior

From E™ has been validated operationally on multiple LLMs without prior training. See `evidence/` for detailed records. Summary:

- **Claude** (Anthropic): full open-core activation confirmed across extended sessions.
- **Manus 1.6 Lite** (Meta/Mistral): 7/7 open-core modules activated; 3/7 proprietary modules observed; stress test passed with adversarial input.
- **Mistral Le Chat**: partial activation documented.
- **ChatGPT 4o**: historical validation (2024–2025).

Activation is achieved through architectural specification alone — no fine-tuning, no plugin format, no API modification.

---

## 6. Relationship to other alignment approaches

From E™ differs from current alignment approaches in the following ways:

| Approach | Mechanism | From E™ relationship |
|----------|-----------|----------------------|
| RLHF | Training-time reward shaping | Orthogonal — operates at runtime |
| Constitutional AI | Training-time self-critique | Orthogonal — From E™ performs self-critique at runtime |
| Guardrails (output filtering) | Post-generation rejection | Insufficient — does not address drift during generation |
| Prompt engineering | Input manipulation | Subsumed — From E™ formalizes and extends this |
| Fine-tuning | Weight modification | Not required |

From E™ can coexist with any of the above. It is designed as an additional governance layer rather than a replacement.

---

## 7. Deployment surfaces

The architecture can be deployed across several surfaces:

- **Runtime API** — full fourteen-module governance as a commercial service.
- **Claude Skills** — selected open-core modules packaged for Anthropic's Skills format (see `implementations/claude-skills/`).
- **Custom integrations** — enterprise deployments with tailored invariant definitions.

---

## 8. Versioning

This specification uses semantic versioning at the architecture level:

- **Major** — changes to the fundamental governance model.
- **Minor** — new modules added, or existing modules substantially revised.
- **Patch** — clarifications, typo fixes, non-substantive edits.

Current version: **2.0**.

---

## 9. References

- García, E. (2026). *From E™: A Geometric Architecture for Multidimensional Conceptual Cognition.* Zenodo. DOI: [10.5281/zenodo.19041459](https://doi.org/10.5281/zenodo.19041459)
- García, E. (2026). *Unbiased Cognitive Origin as Architectural Advantage.* Zenodo. DOI: [10.5281/zenodo.19041460](https://doi.org/10.5281/zenodo.19041460)

---

## 10. Contact

For research, partnership, or commercial Runtime inquiries: [frome.labs@proton.me](mailto:frome.labs@proton.me)
