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
| Model | R²train | Q²cv | R²test |
|-------|---------|------|--------|
| MLR | 0.762 | 0.752 | 0.668 |
| SVR-linear | 0.756 | 0.742 | 0.681 |
| kNN | 0.816 | 0.697 | 0.829 |
| SVR-RBF | **0.884** | **0.811** | **0.853** |
| Decision Tree | 0.891 | 0.634 | 0.781 |
| Random Forest | 0.971 | 0.778 | 0.851 |
| LightGBM | 0.928 | 0.777 | 0.809 |

## Citation
Once published, please cite:
> Nisterenko W. et al. (2026) *Revisiting the LSER Approach in the Era of Machine Learning.* DOI: (to be added)

## License
MIT
