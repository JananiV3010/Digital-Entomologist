# Digital Entomologist: Automated Phenotyping of Anopheles Vectors via Deep Learning

> Automating the taxonomic classification of malaria-vector mosquitoes to address global shortages in trained entomologists.

---

## Overview

Manual identification of *Anopheles* mosquito species requires years of expert training, a resource that is critically scarce in malaria-endemic regions. This project builds a **computer vision framework** that automates species-level classification from specimen images, making vector surveillance accessible to non-experts.

---

## Results

| Metric | Score |
|---|---|
| Hamming Accuracy | **99.65%** |
| Sensitivity | **96.68%** |
| Training Speedup | **30× faster** (GPU caching strategy) |
| Best Architecture | **MobileNet-V3** (edge deployment optimized) |

---

## Architecture & Approach

**Architectures Benchmarked:**
- ResNet-50
- Vision Transformer (ViT)
- EfficientNet
- ConvNeXt
- MobileNet-V3 *(selected for edge deployment)*

**Dataset:** 2,400+ labeled *Anopheles* specimens

**Key Engineering Decisions:**
- MobileNet-V3 selected over heavier Transformer-based models for edge deployment suitability without sacrificing accuracy
- Local GPU caching strategy engineered to resolve cloud storage latency — reduced training epoch duration by **30×**
- **Translator Module** built to convert numerical model outputs into human-readable entomological reports for non-expert users

---

## Repository Structure

```
digital-entomologist/
│
├── data/                    # Dataset loading and preprocessing
├── models/                  # Architecture implementations
│   ├── resnet50.py
│   ├── vit.py
│   ├── efficientnet.py
│   ├── convnext.py
│   └── mobilenet_v3.py      # Final selected model
├── training/                # Training loops and config
├── evaluation/              # Benchmarking and metrics
├── translator/              # Translator Module (output → readable reports)
├── notebooks/               # Exploratory analysis
├── requirements.txt
└── README.md
```

---

## Getting Started

```bash
git clone https://github.com/JananiV3010/digital-entomologist.git
cd digital-entomologist
pip install -r requirements.txt
```

---

## Tech Stack

`Python` `PyTorch` `OpenCV` `scikit-learn` `MobileNet-V3` `Google Colab` `Kaggle`

---

## Why This Matters

Malaria kills over 600,000 people annually. Accurate vector surveillance (knowing *which* mosquito species are present) is critical for targeted interventions. This tool democratizes that capability for field workers without specialized entomological training.

---

## Author

**Janani Vaiyapuriappan** — MSE Biomedical Engineering, Johns Hopkins University  
[LinkedIn](https://www.linkedin.com/in/janani-vaiyapuriappan/) · [GitHub](https://github.com/JananiV3010)

---

*Course project — AI-ML in Global Health, Johns Hopkins University (Fall 2025)*
