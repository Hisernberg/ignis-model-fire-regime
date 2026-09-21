# IGNIS Fire Regime Model — DBSCAN complex segmentation + K-means regime classifier

> Part of the **IGNIS** platform — NASA Space Apps Challenge 2026, challenge #9
> *Harmonization of MODIS and VIIRS Hot Spots*. **Private during judging.**

The original IGNIS model: StandardScaler->DBSCAN complex segmentation (63 complexes, silhouette 0.178) + K-means k=6 fire-regime classifier, trained on 138,118 real FIRMS detections across Amazon, Congo and Borneo. Powers the in-app regime panel.

## Contents
- `train_segmenter.py` — full reproducible training pipeline (real NASA FIRMS data)
- model artifacts (scikit-learn joblib bundles) + `metrics.json`
- `LICENSE` — MIT

## Hugging Face
The same model, with the full model card, lives at
**https://huggingface.co/Nabidnur/ignis-fire-regime-model** (private; request access or see the main repo).

## Main project
https://github.com/Hisernberg/ignis-spaceapps2026 — live app:
https://ignis-spaceapps2026.vercel.app

## Provenance
All training data derives from NASA FIRMS active-fire detections (public domain),
harmonized across MODIS (Terra/Aqua) and VIIRS (S-NPP/NOAA-20/NOAA-21) by the IGNIS
pipeline. No synthetic data is used for supervised labels.
