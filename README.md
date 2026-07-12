<div align="center">

# JangKeun Kim, Ph.D.

**Computational biologist working on evaluation, grounding, and post-training for AI in the life sciences**

**Weill Cornell Medicine · spaceflight, single-cell, and perturbation biology**

[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=07hptXkAAAAJ)
[![ORCID](https://img.shields.io/badge/ORCID-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0002-8733-9925)
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-FFD21E?style=for-the-badge)](https://huggingface.co/jang1563)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jangkeun-kim-16a74b19b/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jak4013@med.cornell.edu)

</div>

---

I build the evidence and evaluation layer for AI in biology: experiments that generate hard biological data, benchmarks that measure what models actually know, and retrieval or post-training systems that make their limits explicit.

## Selected work

**Evaluation**
- [`grounding-atlas`](https://github.com/jang1563/grounding-atlas) measures whether biological properties recoverable from model states are also expressed in model outputs across biological representations.
- [`verify-or-trust`](https://github.com/jang1563/verify-or-trust) studies how a general model should trust, verify, or defer when using fallible perturbation-model outputs.
- [`SpaceOmicsBench`](https://github.com/jang1563/SpaceOmicsBench) is a multi-omics benchmark for spaceflight data: 21 ML tasks, 9 modalities, and a 100-question model evaluation.
- [`narrow-model-safety-eval`](https://github.com/jang1563/narrow-model-safety-eval) evaluates what representations from ESM-2 and ProteinMPNN encode and separate.

**Negative evidence**
- [NullAtlas / NegBioDB](https://huggingface.co/datasets/jang1563/NegBioDB) is a negative-results program selected for Anthropic's AI for Science program. Its current public release contains five domains and more than 64 million confirmed negative records for retrieval and verification research.

**Post-training**
- I build and diagnose SFT, DPO, GRPO, and QLoRA workflows for biological evaluation tasks. A recurring result is that some evidence is better supplied through retrieval and deterministic checks than treated as a weight-update problem.

---

At Weill Cornell Medicine, I lead spaceflight research and co-founded the SOMA consortium across more than 100 institutions in 25+ countries. I came to AI evaluation from drug discovery, single-cell genomics, and Perturb-seq. I hold a Ph.D. from KAIST and am an inventor on two licensed patents.
