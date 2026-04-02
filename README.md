# Diabetic Neuropathy — Nodal Protein Periodicity

Analysis of dSTORM autocorrelation maps to quantify paranodal protein
periodicity (Caspr1, PanNF) in diabetic neuropathy and correlate structural
measures with clinical severity scores.

**Associated publication:** [add citation after acceptance]  
**BioImage Archive accession:** [add after submission]  
**Code DOI:** [add Zenodo DOI after GitHub release]

---

## Project structure

```
Neuropathy/
├── code/                        # All analysis scripts and notebooks
│   ├── acf_pipeline/            # TIFF → ACF → quality scores
│   ├── feature_analysis/        # Midline profile feature extraction
│   ├── clinical_correlation/    # Spearman correlations + figures
│   ├── utils/                   # Shared helpers
│   ├── notebooks/               # Clean, documented notebooks
│   └── _archive/                # Old versions (do not use)
├── data/
│   ├── raw_data/                # ACF correlation TIFFs (READ-ONLY)
│   ├── raw_images/              # Raw dSTORM images (READ-ONLY)
│   ├── metadata/                # Clinical data, harmonised tables
│   └── processed/               # Derived outputs (reproducible)
├── results/
│   ├── figures/publication/     # Final publication figures (PNG + PDF)
│   ├── figures/diagnostics/     # QC and exploratory scatter plots
│   └── tables/                  # CSV correlation tables
├── docs/                        # Data dictionary, methods notes
├── envs/                        # Conda environment files
└── _archive/                    # Old scripts and documents
```

---

## Quick start

```bash
conda env create -f envs/acf_env.yml
conda activate acf_env

# Run ACF pipeline on TIFFs
jupyter lab code/acf_pipeline/acf_v4_final.ipynb

# Run clinical correlation analysis
jupyter lab code/clinical_correlation/feature-ACF-correlation-clean.ipynb
```

---

## Data

Raw dSTORM images and autocorrelation maps: **BioImage Archive** [accession]  
Clinical data: available from corresponding author (ethics-restricted)

**Pixel size:** ~20.4 nm/px (estimated; see `docs/pixel_size_calibration.md`)  
All primary features are ratio-based and pixel-size independent.

---

## Key results

| Marker | Measure | Clinical score | Spearman ρ | p |
|--------|---------|----------------|-----------|---|
| Caspr1 | Periodicity mean | NPSI | +0.66 | 0.002 * |
| Caspr1 | Periodicity mean | SAS  | +0.55 | 0.016 * |
| PanNF  | Periodicity SD   | NIS-LL | +0.60 | 0.015 * |

Group 1 (diabetic neuropathy) only. Controls excluded.

---

## See also

- `docs/data_dictionary.md` — all variables defined with units
- `docs/methods.md` — analysis decisions and caveats
- `docs/pixel_size_calibration.md` — pixel size estimation notes
