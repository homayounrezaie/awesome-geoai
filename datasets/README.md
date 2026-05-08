# Datasets

This folder contains the geospatial dataset catalog in three formats.

## Files

```text
Geospatial-Datasets.md       # human-readable dataset catalog with notes and sources
geospatial_datasets.csv      # spreadsheet-friendly dataset table
geospatial_datasets.json     # machine-readable dataset registry
```

## Current Coverage

The CSV/JSON registry currently contains **94 dataset records** parsed from the Markdown catalog.

Availability fields currently tracked:

```text
github
huggingface
kaggle
earthengine
nasa_earthdata
zenodo
```

Platform-link audit, 2026-05-08:

```text
dataset records: 94
GitHub-linked records: 50
Hugging Face-linked records: 28
Kaggle-linked records: 5
unique GitHub/Hugging Face/Kaggle links checked: 79
GitHub/Kaggle broken links found: 0
Hugging Face links returning gated/API 401 during script check: 9
```

The Hugging Face `401` responses are kept because the dataset pages are known catalog entries, but programmatic access may require authentication, agreement, or xet-backed access.

Categories:

```text
Pre-Training & Foundation Model Scale Datasets
Scene Classification
Semantic Segmentation & Land Cover
Object Detection
Change Detection
Instance Segmentation & Building Footprints
Agricultural & Crop Mapping
SAR (Synthetic Aperture Radar)
Cloud Detection & Atmospheric
Time Series & Temporal
Foundation Model Embeddings (Pre-computed)
Benchmarks & Multi-Task Evaluation
Large-Scale Additions From GitHub, Kaggle, and Hugging Face
```

## Important Note

The Markdown file is the source of richer dataset descriptions. The CSV and JSON are for filtering, scripts, dashboards, and quick analysis.

## Sources

- Local catalog: [Geospatial-Datasets.md](Geospatial-Datasets.md)
- Dataset project pages, papers, GitHub repositories, Hugging Face datasets, and Zenodo records linked in the catalog
- Awesome Remote Sensing Foundation Models dataset and benchmark sections: https://github.com/Jack-bo1220/Awesome-Remote-Sensing-Foundation-Models
- TorchGeo dataset references: https://torchgeo.readthedocs.io/
- Hugging Face Datasets: https://huggingface.co/datasets
- Kaggle Datasets: https://www.kaggle.com/datasets
- Google Earth Engine Data Catalog: https://developers.google.com/earth-engine/datasets
