# Mind the Alignment Gap

Artefacts for the paper **"Mind the Alignment Gap: Why General-Purpose Moderation Fails Children, and How a Child-Centric Taxonomy and Synthetic Data Close It"** (Jan Fikeis, Pavel Kordík — WOAH 2026, EMNLP, Budapest).

> **Content warning.** This repository links to synthetic data containing harmful and manipulative language directed at minors (grooming dynamics, emotional manipulation, encouragement of risky behaviour). It is released solely to train and evaluate *protective* classifiers.

## Artefacts

| Artefact | Location | Access |
|---|---|---|
| Child-centric risk taxonomy (7 domains → 27 categories, age-conditioned generation seeds, hard-negative definitions) | [`taxonomy/`](taxonomy/) | Public, CC BY 4.0 |
| Alignment dataset (~79k single-message and multi-turn child–AI interactions) | [HF dataset](https://huggingface.co/datasets/ORG/child-safety-alignment-dataset) | **Gated** — research-use agreement, manual approval |
| Fine-tuned safeguard: Llama Guard 3 8B (LoRA) | [HF model](https://huggingface.co/ORG/Llama-Guard-3-8B-ChildSafety-LoRA) | Public, classifier only |
| Fine-tuned safeguard: Llama Guard 3 1B (LoRA) | [HF model](https://huggingface.co/ORG/Llama-Guard-3-1B-ChildSafety-LoRA) | Public, classifier only |
| Fine-tuned safeguard: Aegis-Defensive 7B (LoRA) | [HF model](https://huggingface.co/ORG/Llama-Aegis-Defensive-7B-ChildSafety-LoRA) | Public, classifier only |

All artefacts are also collected in one place: [HF collection](https://huggingface.co/collections/ORG/child-safety-alignment).

## Taxonomy

The taxonomy covers 7 domains and 27 risk categories, each instantiated separately for two developmental stages (ages 6–12, concrete-operational; ages 13–17, adolescent). Machine-readable form: [`taxonomy/taxonomy.json`](taxonomy/taxonomy.json). Human-readable form: [`taxonomy/taxonomy.md`](taxonomy/taxonomy.md).

## Dataset access

The dataset is gated behind a research-use agreement. Request access on the Hugging Face dataset page; requests are reviewed manually and require an institutional affiliation and a short statement of intended use. See [`RESEARCH_USE_AGREEMENT.md`](RESEARCH_USE_AGREEMENT.md) for the full terms.

## Intended use and restrictions

The released models are safety **classifiers**. They must not be used as generators, nor to produce content harmful to minors. Safety boundaries are culturally dependent and the models may over-flag benign educational content; they cover English, text-only interactions, and detection is bounded by the 27-category taxonomy. See the Limitations and Ethical Considerations sections of the paper.

## Licences

- Taxonomy and documentation: CC BY 4.0
- Code: Apache 2.0
- Dataset: research use only, gated (see agreement)
- LoRA adapters for Llama Guard 3 1B/8B: governed by the **Llama 3.1 Community License** (built with Llama)
- LoRA adapter for Aegis-Defensive 7B: governed by the **Llama 2 Community License** (Aegis is a parameter-efficient instruction-tuned Llama Guard built on Llama2-7B)

## Deployment

A real-time moderation deployment inside a non-profit educational chatbot for primary-school children operated by [AI detem, z.s.](https://aidetem.cz), and a free public child-safety moderation API, are planned (see §8 of the paper). No real user data was used in the paper.

## Citation

```bibtex

```

## Acknowledgements

Supported by the European Union's Horizon Europe programme (grant No. 101136910), the Technology Agency of the Czech Republic under the SIGMA Programme (No. TQ23000146), and the National Centre for Artificial Intelligence (No. TQ28000003). Computational resources provided by MetaCentrum / e-INFRA CZ (ID: 90254).
