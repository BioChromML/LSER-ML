# LSER-ML: Machine Learning Models for IAM Chromatographic Retention

## Overview
This repository contains the dataset and modeling code for predicting the chromatographic hydrophobicity index of immobilized artificial membrane chromatography (CHI_IAM) using Abraham solvation descriptors combined with machine learning algorithms. The dataset comprises 993 structurally diverse compounds. The best-performing model (SVR-RBF) achieved R²test = 0.853 and RMSEtest = 4.609.

## Repository Structure

    ├── data/
    │   └── dataset.xlsx
    ├── modeling.ipynb
    └── requirements.txt

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/BioChromML/LSER-ML.git
cd LSER-ML
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the notebook:
```bash
jupyter notebook code.ipynb
```

4. In the first cell, update the `path` variable to point to your local data file:
```python
path = "data/dataset.xlsx"
```

## Models
## Models

| Model | R²train | RMSEtrain | Q²cv | Q²cv (SD) | RMSEcv | R²test | RMSEtest |
|-------|---------|-----------|------|-----------|--------|--------|---------|
| **LSER** |
| MLR | 0.704 | 8.873 | 0.698 | 0.032 | 8.921 | 0.673 | 6.850 |
| SVR-linear | 0.700 | 8.936 | 0.695 | 0.026 | 8.972 | 0.668 | 6.902 |
| kNN | 0.811 | 7.090 | 0.683 | 0.061 | 9.117 | 0.792 | 5.457 |
| SVR-RBF | 0.821 | 6.907 | 0.756 | 0.063 | 7.967 | 0.780 | 5.613 |
| DT | 0.874 | 5.796 | 0.622 | 0.074 | 9.919 | 0.740 | 6.101 |
| RF | 0.947 | 3.766 | 0.741 | 0.056 | 8.217 | 0.834 | 4.874 |
| LightGBM | 0.881 | 5.641 | 0.735 | 0.046 | 8.356 | 0.774 | 5.697 |
| **LSER + ionization descriptors** |
| MLR | 0.762 | 7.943 | 0.752 | 0.036 | 8.044 | 0.668 | 6.931 |
| SVR-linear | 0.756 | 8.051 | 0.742 | 0.032 | 8.218 | 0.681 | 6.788 |
| kNN | 0.816 | 6.993 | 0.697 | 0.035 | 8.906 | 0.829 | 4.967 |
| SVR-RBF | **0.884** | **5.546** | **0.811** | **0.048** | **6.989** | **0.853** | **4.609** |
| DT | 0.891 | 5.381 | 0.634 | 0.044 | 9.801 | 0.781 | 5.631 |
| RF | 0.971 | 2.778 | 0.778 | 0.028 | 7.619 | 0.851 | 4.648 |
| LightGBM | 0.928 | 4.383 | 0.777 | 0.048 | 7.605 | 0.809 | 5.256 |

## Citation
Once published, please cite:
> Nisterenko W. et al. (2026) *Revisiting the LSER Approach in the Era of Machine Learning.* DOI: (to be added)

## License
MIT
