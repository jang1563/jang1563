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
- [`agentic-drug-discovery-system`](https://github.com/jang1563/agentic-drug-discovery-system) packages CTDBench v0.2, verifier contracts, and an audited retrospective discovery slice focused on sickle cell disease.
- [`LabCraft-Eval`](https://github.com/jang1563/LabCraft-Eval) is an Inspect AI environment for evaluating tool-using agents on molecular microbiology protocols in a seeded laboratory simulator, with deterministic trajectory scoring.
- [`SpaceOmicsBench`](https://github.com/jang1563/SpaceOmicsBench) is a multi-omics benchmark for spaceflight data: 21 ML tasks, 9 modalities, and a 100-question model evaluation.

**Negative evidence**
- **NegBioDB / NullAtlas** is a private, release-gated biomedical negative-results research program supported by Anthropic's AI for Science program. Its public [`negbiodb-safety-calibration`](https://github.com/jang1563/negbiodb-safety-calibration) companion reports aggregate, non-record-level calibration results across five biomedical domains.

**Post-training**
- I build and diagnose SFT, DPO, GRPO, and QLoRA workflows for biological evaluation tasks. A recurring result is that some evidence is better supplied through retrieval and deterministic checks than learned through weight updates.
- A bounded public example, [`BioReview_Training`](https://github.com/jang1563/BioReview_Training), packages QLoRA SFT and held-out evaluation for biomedical peer review; its committed v3 test summaries report an F1 score of 0.704 for the 8B+9B ensemble.

---

At Weill Cornell Medicine, I lead spaceflight research and co-founded the SOMA consortium, which spans more than 100 institutions across 25+ countries. I came to AI evaluation from drug discovery, single-cell genomics, and Perturb-seq. I hold a Ph.D. from KAIST and am an inventor on two licensed patents.
