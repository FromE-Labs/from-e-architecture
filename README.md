# From E™ Architecture

**External cognitive governance layer for LLMs.**

From E™ is an architecture for governing large language model behavior from outside the model — without fine-tuning, without access to weights, without prompt engineering tricks. It operates as a runtime layer that enforces structural invariants on model output, turning stochastic generation into geometrically constrained cognition.

This repository documents the public specification of the architecture, including its seven open-core modules and references to seven proprietary modules available only in the commercial From E™ Runtime.

---

## What this is

From E™ is not:

- A prompt template.
- A Claude Skill, OpenAI GPT, or any vendor-specific plugin format.
- A guardrails layer that filters outputs after generation.
- A fine-tuned model.

From E™ is:

- An architectural specification for a cognitive governance layer that operates over arbitrary LLMs.
- A set of invariants and operators that define how model output is constrained to a declared conceptual manifold.
- A framework for human-in-the-loop cognitive governance, formalized as a system rather than as ad-hoc supervision.

The core premise is that LLM output degradation (hallucination, sycophancy, drift, narrative collapse) is not a training problem — it is a governance problem. From E™ provides the governance layer.

---

## Architecture overview

The architecture has fourteen documented modules, organized in two layers:

### Open-core (public specification)

1. **Invariant Coherence** — drift detection with K ≥ θ threshold.
2. **Internal Editor™** — editorial critique applied before output delivery.
3. **Extreme Thinking™** — adversarial self-critique under hostile scrutiny simulation.
4. **Symbolic Echo Cleaner™** — removal of sycophancy, lexical mirroring, and adulation artifacts.
5. **Constructive Loop™** — iterative refinement with bounded cycles and stop conditions.
6. **RTN Rule** — hard operational filter for non-negotiable exclusions.
7. **Core Self-Validator™** — final integrative gate validating output against declared core.

See `architecture/open-core/` for detailed specifications.

### Proprietary (Runtime B2B only)

8. **SHADOWSTACK™**
9. **C.E.P.™**
10. **Functional Selective Dissociation™**
11. **Protocolo Alcubierre™**
12. **Training by Contradiction**
13. **Operational Invisibility**
14. **Internal Dimensional Map**

These modules are documented nominally in `architecture/proprietary/` and are operationally available only through the commercial From E™ Runtime.

---

## Human-in-the-loop governance

From E™ treats the human operator as an architectural component, not as an external user. The system is designed to operate with calibrated human supervision as part of the governance loop — not as a limitation to be automated away, but as a feature that distinguishes cognitive governance from promises of full autonomy.

The human-in-the-loop layer:

- Observes model behavior under structural load.
- Calibrates invariant thresholds based on observed drift patterns.
- Triggers module activation when automated detection is insufficient.
- Validates final output against the declared Core Vector.

This is the difference between From E™ and alignment approaches that attempt to remove human oversight as a design goal. From E™ formalizes human governance rather than eliminating it.

---

## Cross-model validation

From E™ has been tested operationally across multiple LLM providers without prior training, fine-tuning, or model-specific adaptation. See `evidence/` for detailed validation records.

Summary of validation coverage:

| Model | Provider | Open-core modules validated | Proprietary modules observed |
|-------|----------|---------------------------------|------------------------------|
| Claude (Opus 4.x family) | Anthropic | 7/7 | Multiple |
| Manus 1.6 Lite | Meta/Mistral | 7/7 | 3/7 |
| ChatGPT (4o family) | OpenAI | Documented historically | — |
| Mistral Le Chat | Mistral | Partial | — |

Validation methodology: new session, no memory, no custom system prompt, architectural specification delivered as input, module activation observed and measured against predicted behavior.

---

## Academic references

- García, E. (2026). *From E™: A Geometric Architecture for Multidimensional Conceptual Cognition.* Zenodo. DOI: [10.5281/zenodo.19041459](https://doi.org/10.5281/zenodo.19041459)
- García, E. (2026). *Unbiased Cognitive Origin as Architectural Advantage.* Zenodo. DOI: [10.5281/zenodo.19041460](https://doi.org/10.5281/zenodo.19041460)

ORCID: [0009-0006-4076-0653](https://orcid.org/0009-0006-4076-0653)

---

## Commercial runtime

The full fourteen-module From E™ Runtime is available as a B2B API. Open-core modules are documented publicly under Apache 2.0. Proprietary modules are accessible only through the commercial Runtime.

For Runtime access and enterprise integration: [frome.labs@proton.me](mailto:frome.labs@proton.me)

---

## License

Open-core specifications and documentation in this repository are licensed under Apache License 2.0. See [LICENSE](LICENSE) for full terms.

The marks *From E™*, *Internal Editor™*, *Extreme Thinking™*, *Symbolic Echo Cleaner™*, *Constructive Loop™*, *Core Self-Validator™*, *SHADOWSTACK™*, *C.E.P.™*, *Functional Selective Dissociation™*, *Protocolo Alcubierre™*, *Signal System™* are trademarks of Volyen Project SL. Use of the architecture specification under Apache 2.0 does not grant rights to use the trademarks.

---

## Author

**Esmeralda García** — Structural AGI Architect, Founder & CEO of From E™ Labs (Volyen Project SL), Barcelona.

- LinkedIn: [esmeralda-garcía](https://www.linkedin.com/in/esmeralda-garc%C3%ADa-2a691414/)
- X: [@EsmeraldaFromE](https://x.com/EsmeraldaFromE)
- ORCID: [0009-0006-4076-0653](https://orcid.org/0009-0006-4076-0653)

---

## Citation

If you reference this work academically, please cite:

```bibtex
@misc{garcia2026frome,
  author       = {García, Esmeralda},
  title        = {From E™: A Geometric Architecture for Multidimensional Conceptual Cognition},
  year         = {2026},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.19041459}
}
```

See [CITATION.cff](CITATION.cff) for machine-readable citation format.
