<div align="center">

# JangKeun Kim, Ph.D.

**Computational biologist working on evaluation, grounding, and post-training for AI in the life sciences**

**Director of Spaceflight Research, Weill Cornell Medicine**

[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=07hptXkAAAAJ)
[![ORCID](https://img.shields.io/badge/ORCID-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0002-8733-9925)
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-FFD21E?style=for-the-badge)](https://huggingface.co/jang1563)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jangkeun-kim-16a74b19b/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jak4013@med.cornell.edu)

</div>

---

Most of my work is about whether we can trust what a model says about biology. The projects here are mostly evaluations and datasets: measuring where a model's biology actually holds, assembling the negative evidence that a literature biased toward positive results never recorded, and the post-training that turns those into a signal a model can use.

## Selected work

**Evaluation**
- [`grounding-atlas`](https://github.com/jang1563/grounding-atlas) tests whether a model knows a molecule by its content or only by its name, across 17 representations.
- [`verify-or-trust`](https://github.com/jang1563/verify-or-trust) and [`causalatlas`](https://github.com/jang1563/causalatlas) ask whether a model reasoning over a fallible perturbation model (GEARS, Arc STATE) knows when to trust it. Even the strongest models tend to over-verify rather than read the prediction's reliability.
- [`GeneLab_benchmark`](https://github.com/jang1563/GeneLab_benchmark) finds that gene-expression foundation models do not transfer across spaceflight missions, where a simple classical baseline reaches AUROC 0.948.
- [`SpaceOmicsBench`](https://github.com/jang1563/SpaceOmicsBench) is a multi-omics benchmark for spaceflight data: 21 ML tasks, 9 modalities, and a 100-question model evaluation.
- [`narrow-model-safety-eval`](https://github.com/jang1563/narrow-model-safety-eval) looks at what two widely used protein models, ESM-2 and ProteinMPNN, encode and separate.
- [`LabCraft-Eval`](https://github.com/jang1563/LabCraft-Eval) is a deterministic, non-LLM-judge grader for whether an agent can actually run a molecular-biology protocol.

**Negative evidence**
- NullAtlas, with its data layer NegBioDB, is a thirty-domain negative-results program (32.9M confirmed negatives released so far), selected for Anthropic's AI for Science program and shipped as a Model Context Protocol tool. Asked for a drug's prior failed trials, ungrounded models fabricate most of what they cite; grounded against it, they stop.

**Post-training**
- [`BioReview_Training`](https://github.com/jang1563/BioReview_Training) is a QLoRA fine-tuning pipeline for biomedical peer review.
- NegBioRL is a verifiable-reward RL environment (SFT, DPO, GRPO). The useful result there was a negative one: this signal has to be retrieved at inference, not trained into the weights.

---

I am Director of Spaceflight Research at Weill Cornell Medicine, where I co-founded the SOMA consortium across 100+ institutions and 25+ countries. I came to this from drug discovery, carrying two targets to licensed patents, and from single-cell and Perturb-seq biology. PhD from KAIST.
