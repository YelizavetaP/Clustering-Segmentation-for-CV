# Clustering-Segmentation-for-CV

ГРУПА ВИМОГ 2 — cluster a set of remote-sensing (ДЗЗ) Earth-surface images
(≥ 10 instances) by visual features (crops / forests / buildings, etc.) using
classical ML clustering. **No deep learning.**

## Structure

```
data/raw/        # source ДЗЗ images (download ≥ 10 here)
results/         # cluster_assignments.csv and other outputs
results/figures/ # saved plots (dendrogram, cluster grids)
notebooks/       # experiments.ipynb — full pipeline
```

## Setup

```bat
python -m venv venv
venv\Scripts\activate.bat
pip install -r requirements.txt
```

## Workflow

1. Download ≥ 10 ДЗЗ images into `data/raw/` (Copernicus Browser, NASA Earthdata,
   EOS LandViewer, Kaggle — see `task4.pdf`).
2. Run `notebooks/experiments.ipynb`:
   load → analyze/enhance → feature extraction → clustering (K-Means + hierarchical)
   → visualize → save results.
