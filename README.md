# Classification of Variable Star Light Curves using Machine Learning

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Lightkurve](https://img.shields.io/badge/Lightkurve-TESS-green)
![License](https://img.shields.io/badge/License-MIT-red)

## Project Overview

This project applies supervised machine learning techniques to classify variable stars using photometric light curves from the **Transiting Exoplanet Survey Satellite (TESS)** mission.

The workflow includes:

- Downloading and preprocessing TESS light curves
- Feature extraction
- Data preprocessing
- Model training and evaluation
- Confusion matrix analysis
- Feature importance using SHAP
- Performance comparison using standard classification metrics

---

## Classes

The current model classifies the following stellar objects:

- 🌌 Galaxy
- ✨ Quasar (QSO)
- ⭐ Star

---

## Dataset

The data are obtained from the **TESS Mission** using the Lightkurve package.

Example:

```python
import lightkurve as lk

search_result = lk.search_lightcurve(
    "RR Lyrae",
    mission="TESS"
)
```

---

## Machine Learning Pipeline

```
Raw TESS Light Curves
          │
          ▼
Data Cleaning
          │
          ▼
Feature Engineering
          │
          ▼
Train/Test Split
          │
          ▼
Machine Learning Model
          │
          ▼
Prediction
          │
          ▼
Model Evaluation
          │
          ▼
SHAP Explainability
```

---

## Repository Structure

```
variable-star-classification/

│
├── notebooks/
│   └── Variable_Star_Classification.ipynb
│
├── figures/
│   ├── confusion_matrix.png
│   ├── shap_summary.png
│   ├── shap_bar.png
│   └── feature_importance.png
│
├── data/
│   └── README.md
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/variable-star-classification.git
```

Move into the project

```bash
cd variable-star-classification
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Required Packages

```
numpy
pandas
matplotlib
scikit-learn
lightkurve
astropy
shap
scienceplots
seaborn
```

---

## Results

The trained classifier achieves high classification performance on the test dataset.

Evaluation includes:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- SHAP Feature Importance

Example confusion matrix:

<p align="center">
<img src="figures/confusion_matrix.png" width="500">
</p>

---

## Explainable AI

Model interpretability is performed using **SHAP (SHapley Additive exPlanations)**.

Visualizations include:

- SHAP Summary Plot
- SHAP Bar Plot
- Feature Importance Ranking

---

## Future Work

- Incorporate additional variable star classes
- Hyperparameter optimization
- Deep learning models (CNN/LSTM)
- Period detection using Lomb–Scargle periodograms
- Cross-mission validation with Gaia and ZTF

---

## Citation

If you use this repository in your research, please cite it appropriately.

---

## Author

**Sukdev Mahapatra**

M.Sc. Physics (Astroparticle Physics)

GitHub: https://github.com/YOUR_GITHUB_USERNAME

---

## License

This project is licensed under the MIT License.
