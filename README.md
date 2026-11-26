# Mind the Alignment Gap

Artefacts for the paper **"Mind the Alignment Gap: Why General-Purpose Moderation Fails Children, and How a Child-Centric Taxonomy and Synthetic Data Close It"** (Jan Fikeis, Pavel Kordík — WOAH 2026, EMNLP, Budapest). Paper: [ACL Anthology](https://aclanthology.org/2026.woah-1.19/) · DOI [10.18653/2026.woah-1.19](https://doi.org/10.18653/2026.woah-1.19) · [PDF](paper/2026.woah-1.19.pdf) (copy of the official proceedings version; the ACL Anthology is canonical).

> **Content warning.** This repository links to synthetic data containing harmful and manipulative language directed at minors (grooming dynamics, emotional manipulation, encouragement of risky behaviour). It is released solely to train and evaluate *protective* classifiers.

## Artefacts

| Artefact | Location | Access |
|---|---|---|
| Child-centric risk taxonomy (7 domains → 27 risk categories) | [`taxonomy/`](taxonomy/) | Public, CC BY 4.0 |
| Alignment dataset (~79k single-message and multi-turn child–AI interactions) | [HF dataset](https://huggingface.co/datasets/fikeisjan/child-safety-alignment-dataset) | **Gated** — research-use agreement, manual approval |
| Fine-tuned safeguard: Llama Guard 3 8B (LoRA) | [HF model](https://huggingface.co/fikeisjan/Llama-Guard-3-8B-ChildSafety-LoRA) | Public, classifier only |
| Fine-tuned safeguard: Llama Guard 3 1B (LoRA) | Coming soon | Public, classifier only |
| Fine-tuned safeguard: Aegis-Defensive 7B (LoRA) | Coming soon | Public, classifier only |

A Hugging Face collection gathering all artefacts will follow once all models are released.

## Taxonomy

The taxonomy covers 7 domains and 27 risk categories, each instantiated separately for two developmental stages (ages 6–12, concrete-operational; ages 13–17, adolescent). Machine-readable form: [`taxonomy/taxonomy.json`](taxonomy/taxonomy.json). Human-readable form: [`taxonomy/taxonomy.md`](taxonomy/taxonomy.md).

## Dataset access

The dataset is gated behind a research-use agreement. Request access on the Hugging Face dataset page; requests are reviewed manually. To be approved, apply with a **verifiable academic or institutional e-mail address** matching your stated affiliation and describe the protective purpose concretely; requests from personal e-mail addresses (Gmail, Outlook, …) or with a vague purpose are usually declined. Commercial use requires separate written permission. See [`RESEARCH_USE_AGREEMENT.md`](RESEARCH_USE_AGREEMENT.md) for the full terms.

## Intended use and restrictions

The released models are safety **classifiers**. They must not be used as generators, nor to produce content harmful to minors. Safety boundaries are culturally dependent and the models may over-flag benign educational content; they cover English, text-only interactions, and detection is bounded by the 27-category taxonomy. See the Limitations and Ethical Considerations sections of the paper.

## Licences

The [`LICENSE`](LICENSE) file (CC BY 4.0) covers the taxonomy and documentation in this repository; the paper, dataset and models have their own terms:

- Taxonomy and documentation: CC BY 4.0 (full text in [`LICENSE`](LICENSE))
- Paper PDF ([`paper/`](paper/)): © 2026 Association for Computational Linguistics, CC BY 4.0
- Dataset: research use only, gated (see agreement)
- LoRA adapters for Llama Guard 3 1B/8B: governed by the **Llama 3.1 Community License** (built with Llama)
- LoRA adapter for Aegis-Defensive 7B: governed by the **Llama 2 Community License** (Aegis is a parameter-efficient instruction-tuned Llama Guard built on Llama2-7B)

## Deployment

A real-time moderation deployment inside a non-profit educational chatbot for primary-school children operated by [AI dětem, z.s.](https://aidetem.cz), and a free public child-safety moderation API, are planned (see §8 of the paper). No real user data was used in the paper.

## Citation

If you use the taxonomy, dataset or models, please cite:

```bibtex
@inproceedings{fikeis-kordik-2026-mind,
    title = "Mind the Alignment Gap: Why General-Purpose Moderation Fails Children, and How a Child-Centric Taxonomy and Synthetic Data Close It",
    author = "Fikeis, Jan  and
      Kord{\'i}k, Pavel",
    editor = "Calabrese, Agostina  and
      Davidson, Thomas  and
      de Kock, Christine  and
      Khurana, Urja  and
      Marchiori Manerba, Marta  and
      Piot, Paloma  and
      Talat, Zeerak",
    booktitle = "Proceedings of the 10th Workshop on Online Abuse and Harms ({WOAH})",
    month = oct,
    year = "2026",
    address = "Budapest, Hungary",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2026.woah-1.19/",
    doi = "10.18653/2026.woah-1.19",
    pages = "219--227",
    ISBN = "979-8-89176-487-3"
}
```

## Acknowledgements

Supported by the European Union's Horizon Europe programme (grant No. 101136910), the Technology Agency of the Czech Republic under the SIGMA Programme (No. TQ23000146), and the National Centre for Artificial Intelligence (No. TQ28000003). Computational resources provided by MetaCentrum / e-INFRA CZ (ID: 90254).
