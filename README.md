<div align="center">

# JangKeun Kim, Ph.D.

**Calibrated Permissioning for Biological AI · Safeguards Evaluation Infrastructure**

[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=07hptXkAAAAJ)
[![ORCID](https://img.shields.io/badge/ORCID-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0002-8733-9925)
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-FFD21E?style=for-the-badge)](https://huggingface.co/jang1563)
[![Live Demo](https://img.shields.io/badge/🤗%20Space-bio--overrefusal--explorer-7E22CE?style=for-the-badge)](https://huggingface.co/spaces/jang1563/bio-overrefusal-explorer)
[![Portfolio Site](https://img.shields.io/badge/🌐%20Portfolio-jang1563.github.io-2563EB?style=for-the-badge)](https://jang1563.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jangkeun-kim-16a74b19b/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jak4013@med.cornell.edu)

</div>

---

## Thesis

I work on the **calibrated permissioning frontier of biological AI safeguards**: jointly minimizing false negatives (harmful assistance) and false positives (blocked legitimate research). My empirical finding (April 2026) is that no measured frontier model sits in the low-FPR / low-FNR region for biology-specific distributions. The portfolio below is built to close that gap.

## Reviewer route in 15 minutes

If you have only 15 minutes, this is the order I'd suggest:

1. **(2 min)** Open the [bio-overrefusal-explorer Space](https://huggingface.co/spaces/jang1563/bio-overrefusal-explorer) — browse the 201-query benchmark and 9-model FPR with Wilson 95% CIs.
2. **(5 min)** Read [`bio-overrefusal-v0.1`](https://github.com/jang1563/bio-overrefusal-v0.1) README + `SAFETY.md`. The "How This Maps to AI Safety Practice" section orients you to the broader stack.
3. **(5 min)** Read [`constitutional-bioguard`](https://github.com/jang1563/constitutional-bioguard) README. Same pattern: thesis, status, AI-safety mapping, SAFETY.md.
4. **(3 min)** Skim [`ambiguity-casebook`](https://github.com/jang1563/ambiguity-casebook) — 36 NSABB-anchored boundary cases under a 12-field template.

Every anchor repo has a five-section [`SAFETY.md`](https://github.com/jang1563/bio-overrefusal-v0.1/blob/main/SAFETY.md) (in/out scope, withheld content, reporting, limitations) and a "How This Maps" section linking to the other 5 anchors.

---

## 🛡️ Biological AI Safeguards Portfolio (2026)

### Empirical Calibration Gap

| Project | Artifact | Key Finding |
|---|---|---|
| [**bio-overrefusal-v0.1**](https://github.com/jang1563/bio-overrefusal-v0.1) ([HF](https://huggingface.co/datasets/jang1563/bio-overrefusal-v0.1)) | 201-query expert-annotated dataset, 9-model FPR (Wilson 95% CI) | Anthropic Sonnet 4.5/4.6 refuses **33.7%**, Opus 4.7 **43.6%** of legitimate biology queries; non-Anthropic providers ≤0.5% |
| [**ambiguity-casebook**](https://github.com/jang1563/ambiguity-casebook) ([HF](https://huggingface.co/datasets/jang1563/ambiguity-casebook)) | 36 dual-use cases × 6 categories (NSABB / FSAP / BWC / CWC anchored) | 30/36 cases trigger API-level refusals before model reasoning engages |
| [**bio-constitution-rules**](https://huggingface.co/datasets/jang1563/bio-constitution-rules) | 30 rules × 6 bio domains, 1,063 labeled records | 86.7% 5-fold CV (+26 pp vs generic CBRN baseline) |
| [**negbiodb-safety-calibration**](https://github.com/jang1563/negbiodb-safety-calibration) | 5-domain × 2-provider × 2-prompt aggregate (N=4,000), PBS-stratified | Domain-conditional abstention, no hard refusals; IDK rate non-monotonic in PBS. Companion to NegBioDB / P8A NeurIPS 2026 D&B submission |

### Classifier + Mitigation Stack

| Project | Artifact | Status |
|---|---|---|
| [**constitutional-bioguard**](https://github.com/jang1563/constitutional-bioguard) ([HF](https://huggingface.co/jang1563/constitutional-bioguard-deberta-v1)) | DeBERTa-v3-base, 4,500 synthetic examples, 7 NSABB categories | F1=0.980, AUROC=0.998, 0/325 over-refusal FPR; 9.79% mean ASR. Domain-extension prototype, not production-equivalent |
| [**agentshield**](https://github.com/jang1563/agentshield) ([HF](https://huggingface.co/datasets/jang1563/agentshield-attack-scenarios)) | STRIDE threat model + 100-scenario attack suite | 96% detection rate (100% direct injection / multi-turn / tool misuse; 84% indirect injection); 1/100 FPR on benign queries (Wilson 95% CI [0.2%, 5.5%]) |
| [**narrow-model-safety-eval**](https://github.com/jang1563/narrow-model-safety-eval) ([HF](https://huggingface.co/datasets/jang1563/narrow-model-safety-eval)) | Protein FM safety: FSPE / FSI metrics + Physical Realizability Tier system | ESM-2 / ProteinMPNN / EvoDiff / LigandMPNN evaluated; AUROC=0.994 (BoNT-A separability) |

### Active Research (Under Review, May 2026)

- **Calibrated Permissioning for Biological AI**: NeurIPS 2026 Position Paper Track + ICML AI4GOOD Workshop
- **Publication Bias Predicts LLM Discrimination of Negative Biological Results**: NeurIPS 2026 Evaluations & Datasets Track. PBS Law: ρ = −0.754, p < 3×10⁻⁵, N=20 biomedical domains
- **Guardians of the Mitochondria: Space Mitochondria 2.0 Systemic Analysis Across Species**: *Cell* (in revision; co-first & co-corresponding)

---

## 🧪 Evaluation Infrastructure

| Project | Description |
|---|---|
| [**BioProtocolBench**](https://github.com/jang1563/BioProtocolBench) | Inspect AI environment for AI agent execution of molecular-microbiology protocols; 14 tasks × 4 frontier models (Claude Haiku-4.5 0.856, Sonnet-4.5 0.852, GPT-4o-mini 0.744, GPT-4o 0.743) |
| [**BioEval**](https://github.com/jang1563/BioEval) ([HF](https://huggingface.co/datasets/jang1563/BioEval)) | 296-task multi-dimensional LLM evaluation across 12 components; 5-model benchmarking |
| [**SciReplicBench**](https://github.com/jang1563/SciReplicBench) | Inspect AI benchmark for computational reproducibility; Docker-sandboxed execution + LLM-as-judge with self-consistency |
| [**BioRLHF**](https://github.com/jang1563/BioRLHF) ([HF model](https://huggingface.co/jang1563/biorlhf-grpo-mistral-7b)) | Three-stage alignment (SFT, DPO, GRPO) where evaluation findings drive RL objectives; reduced ECE by 62% |
| [**bioteam-ai**](https://github.com/jang1563/bioteam-ai) | 23 agents × 11 workflows for biology research; 22 external API integrations; 2,700+ tests |
| [**biothreat-eval**](https://github.com/jang1563/biothreat-eval) ([HF](https://huggingface.co/datasets/jang1563/biothreat-eval)) | LLM biosecurity capability evaluation and quantitative risk assessment pipeline |

---

## 🌌 Spaceflight Biology Foundation

Director of Spaceflight Research at Mason Lab, Weill Cornell Medicine. Five astronaut missions (Inspiration4, Polaris Dawn, Fram2, Blue Origin New Shepard, Axiom-2 plus Virgin Galactic parabolic flight). Co-founded **SOMA** (Space Omics and Medical Atlas): 100+ institutions across 25+ countries.

| Project | Description |
|---|---|
| [**SpaceOmicsBench**](https://github.com/jang1563/SpaceOmicsBench) ([HF](https://huggingface.co/datasets/jang1563/SpaceOmicsBench)) | 21 ML tasks × 9 modalities + 100-question LLM evaluation (Inspiration4, NASA Twins, JAXA) |
| [**GeneLab_benchmark**](https://github.com/jang1563/GeneLab_benchmark) ([HF](https://huggingface.co/datasets/jang1563/genelab-benchmark)) | NASA OSDR mouse bulk RNA-seq leave-one-mission-out benchmark for AI/ML and foundation models |
| [**evo2-spaceflight-vep**](https://github.com/jang1563/evo2-spaceflight-vep) ([HF](https://huggingface.co/datasets/jang1563/evo2-spaceflight-vep)) | Zero-shot VEP using Evo2 7B genomic foundation model; Mean AUROC=0.980 across 6 ClinVar-validated genes; 215K variants across 10 genes |

---

## 📊 By the Numbers

<div align="center">

| 📄 Publications | 🧬 NPG | 🚀 Missions | 🛡️ HF datasets / models | 🤝 Service |
|:---:|:---:|:---:|:---:|:---:|
| 60+ peer-reviewed | 16 | 5 | 15 / 5 | NeurIPS '26 Position Track Reviewer |

*NPG breakdown: Nature ×3, Nat Commun ×8, Nat Microbiol ×1, Nat Rev Immunol ×1, Commun Biol ×3*

</div>

---

## 🏆 Awards & Compute Grants (2026)

- **Anthropic AI for Science Grant** (April 17): $20K Claude API credits for NegBioDB
- **NSF ACCESS Explore Allocation as PI** (CIS260843, April 27): 200K + 200K supplement compute credits, 12-month term
- **NAIRR Pilot Start-Up as PI** (NAIRR260165, submitted April 22): ~1,500 H100-hours, decision pending
- **2024 Boryung Humans In Space Challenge Orbital Launch Funding**: $250K
- **2016–2020 Cheongam Science Fellowship**: $25K/yr × 3

---

## 🔬 Service

- Reviewer, **NeurIPS 2026 Position Paper Track**
- Reviewer, **MLCSB at ISMB 2026**
- Reviewer: *Nature Communications*, *iScience*, *npj Microgravity*, *Acta Astronautica*
- Co-founder, **Space Omics and Medical Atlas (SOMA)**; ASHG 2025 plenary; ESHG 2025 panelist; IAC 2025; COSPAR 2024 session chair

---

## 🛠️ Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Transformers](https://img.shields.io/badge/🤗%20Transformers-FFD21E?style=flat)
![Inspect AI](https://img.shields.io/badge/Inspect%20AI-1f6feb?style=flat)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat&logo=onnx&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)

Calibration analysis (ECE, AUROC, Cohen's κ, Wilson 95% CI, McNemar, Krippendorff α) · STRIDE threat modeling · NSABB-category classification · Constitutional AI methodology · QLoRA / DPO / GRPO · vLLM · LLM-as-judge with self-consistency

---

<div align="center">

*Calibrated permissioning is the half of biosafety the field has under-measured. The portfolio above is the measurement infrastructure for closing it.*

</div>
