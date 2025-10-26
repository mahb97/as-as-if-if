# as-as-if-if — Joyce-aware simile extraction for *Dubliners*

> Weakly supervised, strongly linguistics-led simile detection and categorisation across *Dubliners*. Built to support rigorous, reproducible analysis and invite close reading rather than metrics alone.

## Why this exists

A lot of NLP work on “style” treats language as generic signal. This project starts from linguistics and literary scholarship and asks models to keep up. It operationalises a Joyce-aware pipeline that finds and classifies similes (and near-similes) in *Dubliners*, then makes errors legible so that interpretation stays central. The approach follows my Comparative Suspension Theory (CST) framing and uses categories designed for Joycean figuration: **Standard**, **Quasi**, **Quasi-Fuzzy**, **Framed**, and **Silent**.

## What this repo contains

- A prototype **simile extractor + classifier** tailored to Joycean comparators (e.g., *as*, *like*, *as if*, framed and silent comparatives).
- A **weak-supervision recipe**: spreadsheet seeds → label functions → silver labels over the full text.
- A simple, readable **modelling stack** (feature rules + linear models) and error analysis that supports close reading.
- A working notebook (`LoRA_(PEFT_QLoRA)_.ipynb`) used for rapid experiments; the core method here does **not** require GPUs.

---

## Quick start

### 1) Environment

```bash
# python 3.10+
pip install -U pandas numpy scikit-learn nltk spacy beautifulsoup4 tqdm jupyter
python -m spacy download en_core_web_sm
