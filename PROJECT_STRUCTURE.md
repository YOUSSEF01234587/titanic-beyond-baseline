# Project Structure

## Overview

This document describes the file and directory structure of the Titanic: Beyond Baseline repository.

---

## Directory Layout

```
titanic-beyond-baseline/
│
├── notebook/                           # Core notebook
│   └── titanic-beyond-baseline.ipynb   # Main analysis notebook (212 cells, 105 code)
│
├── outputs/                            # Submission files
│   ├── submission.csv                  # Primary submission (0.76555)
│   ├── submission_weighted.csv         # Weighted ensemble submission
│   ├── submission_stacking.csv         # Stacking ensemble submission
│   ├── submission_f1_threshold.csv     # F1-optimized threshold submission
│   ├── submission_accuracy_threshold.csv # Accuracy-optimized threshold submission
│   └── submission_equal_average.csv    # Equal-weight ensemble submission
│
├── images/                             # Screenshots and diagrams
│   └── README.md                       # Instructions for adding images
│
├── docs/                               # Additional documentation
│
├── .gitignore                          # Git ignore rules
├── LICENSE                             # MIT License
├── README.md                           # Project overview and quick start
├── requirements.txt                    # Python pip dependencies
├── environment.yml                     # Conda environment specification
├── CITATION.cff                        # Citation metadata (CFF format)
├── CONTRIBUTING.md                     # Contribution guidelines
├── CODE_OF_CONDUCT.md                  # Community standards
└── PROJECT_STRUCTURE.md                # This file
```

---

## File Descriptions

### notebook/

Contains the main Jupyter notebook. This is the core deliverable of the project.

| File | Description |
|------|-------------|
| `titanic-beyond-baseline.ipynb` | Complete analysis: data loading, EDA, feature engineering (47 features), model training (7 models), evaluation, ensemble methods, and submission generation |

**Important**: This notebook should not be modified. It is designed to run end-to-end on Kaggle or locally.

### outputs/

Pre-generated submission files from the notebook. These can be directly submitted to Kaggle.

| File | Score | Description |
|------|-------|-------------|
| `submission.csv` | 0.76555 | Primary submission (weighted ensemble) |
| `submission_weighted.csv` | - | Weighted average ensemble |
| `submission_stacking.csv` | - | Stacking ensemble |
| `submission_f1_threshold.csv` | - | F1-optimized threshold |
| `submission_accuracy_threshold.csv` | - | Accuracy-optimized threshold |
| `submission_equal_average.csv` | - | Equal-weight ensemble |

### images/

Screenshots and diagrams for the README. Add images by running the notebook on Kaggle and saving outputs.

| File | Description |
|------|-------------|
| `README.md` | Instructions for adding screenshots |

### docs/

Additional documentation (API references, methodology deep-dives, etc.)

---

## Key Files

### Configuration Files

| File | Purpose |
|------|---------|
| `requirements.txt` | pip install targets |
| `environment.yml` | Conda environment definition |
| `.gitignore` | Files excluded from version control |
| `LICENSE` | MIT License |
| `CITATION.cff` | Citation metadata |

### Community Files

| File | Purpose |
|------|---------|
| `README.md` | Project overview and quick start |
| `CONTRIBUTING.md` | How to contribute |
| `CODE_OF_CONDUCT.md` | Community standards |
| `PROJECT_STRUCTURE.md` | This documentation |

---

## Notebook Structure

The notebook follows this pipeline:

```
Cell 1-2:     Title and introduction
Cell 3-4:     Imports and configuration
Cell 5:       Design system (13 helper functions + 8 auto-layout utilities)
Cell 6-10:    Data loading and initial inspection
Cell 11-25:   Exploratory data analysis (EDA)
Cell 26-45:   Feature engineering (47 features)
Cell 46-60:   Data preprocessing and model setup
Cell 61-100:  Model training (7 models with cross-validation)
Cell 101-130: Model evaluation and comparison
Cell 131-160: Ensemble methods (5 approaches)
Cell 161-180: Feature importance analysis
Cell 181-210: Prediction and submission generation
Cell 211-212: Summary and conclusions
```

---

## Data Flow

```
Input Data (Kaggle/Local)
    ↓
Data Loading (with fallback paths)
    ↓
Exploratory Data Analysis
    ↓
Feature Engineering (47 features)
    ↓
Model Training (7 models × 5-fold CV)
    ↓
Ensemble Construction (5 methods)
    ↓
Prediction Generation
    ↓
Submission Files (outputs/)
```

---

## Dependencies

### Core
- Python 3.10+
- numpy, pandas, scikit-learn, scipy

### Machine Learning
- xgboost, lightgbm, catboost

### Optimization
- optuna

### Visualization
- matplotlib, seaborn, plotly

### Explainability
- shap

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2024 | Initial release with 0.76555 Kaggle score |

---

## Notes

- The notebook is designed to be self-contained and reproducible
- Random seeds are set for reproducibility (SEED = 42)
- The design system in Cell 5 can be extracted and reused in other projects
- All visualizations use the auto-layout system for consistent styling
