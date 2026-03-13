# 🌱 Soil Fertility Prediction and Crop Recommendation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=flat&logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-yellow?style=flat&logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat&logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

> A machine learning system that predicts soil fertility and recommends suitable crops based on soil nutrient analysis — helping farmers make smarter, data-driven decisions for better agricultural productivity.

---

## 📌 Overview

Soil health is the foundation of agriculture. Yet most farmers rely on manual testing which is time-consuming and expensive. This project automates **soil fertility classification** and **crop recommendation** using machine learning, making precision agriculture accessible and practical.

Given a soil sample's chemical and physical properties, the system:
- Predicts whether the soil is **Fertile** or **Non-Fertile**
- Recommends suitable **crops and fertilizers** based on nutrient composition
- Compares multiple ML models to identify the most accurate approach

---

## 🏆 Results

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| **Random Forest** | **100%** | — | — | — |
| **Support Vector Machine (SVM)** | **95%** | 0.90 | 0.90 | 0.90 |
| Naïve Bayes | 85% | — | — | — |

- **SVM** delivered the most consistent and balanced performance across all metrics
- **Random Forest** achieved perfect accuracy through its ensemble approach
- **Naïve Bayes** served as a reliable baseline model

---

## 📂 Project Structure

```
Soil-Fertility-Crop-Prediction/
│
├── SVM_soil_fertility_prediction.ipynb          # SVM model — training, evaluation & results
├── naive_bayes_soil_fertility_prediction.ipynb  # Naïve Bayes model implementation
├── combining_of_models.ipynb                    # Model comparison & performance analysis
├── fertile_recommendation_dataset.csv           # Dataset (100 samples, 17 features)
└── README.md                                    # Project documentation
```

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| **Source** | [Kaggle – Explainable AI for Soil Fertility Prediction](https://www.kaggle.com/datasets/harshivchandra/explainable-ai-for-soil-fertility-prediction) |
| **Samples** | 100 soil records |
| **Features** | pH, EC, OC, OM, N, P, K, Zn, Fe, Cu, Mn, Clay, CaCO3, CEC, Sand, Silt |
| **Target** | Fertile (1) / Non-Fertile (0) |

---

## ⚙️ Methodology

### Data Preprocessing
- Label encoding: Fertile → 1, Non-Fertile → 0
- Feature scaling using **Z-Score Standardization** (mean=0, std=1)
- **Min-Max Normalization** applied for distance-based models
- 80/20 train-test split with `random_state=42` for reproducibility
- Stratified K-Fold Cross Validation for robust evaluation

### Models Used

**1. Support Vector Machine (SVM)**
- RBF kernel to handle non-linear relationships between soil features
- Optimizes hyperplane margin for clean class separation
- Regularization parameter C for balanced generalization

**2. Naïve Bayes**
- Probabilistic classifier using Bayes' theorem
- Gaussian likelihood for continuous soil nutrient features
- Fast and interpretable baseline

**3. Random Forest**
- Ensemble of decision trees with bootstrap sampling
- Gini Impurity for node splitting
- Aggregated voting for final classification

### Evaluation Metrics
- Accuracy, Precision, Recall, F1 Score
- Confusion Matrix
- Stratified K-Fold Cross Validation

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.8+ |
| ML Library | Scikit-learn |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Bhargava102005/Soil-Fertility-Crop-Prediction.git
cd Soil-Fertility-Crop-Prediction
```

### 2. Install Dependencies
```bash
pip install scikit-learn pandas numpy matplotlib seaborn jupyter
```

### 3. Run the Notebooks
```bash
jupyter notebook
```
Open any `.ipynb` file and run all cells sequentially.

---

## 💡 Key Takeaways

- Hands-on experience with end-to-end ML pipeline: data preprocessing → model training → evaluation
- Comparative analysis of classification algorithms on a real-world agricultural dataset
- Feature importance analysis revealed **pH, Nitrogen, and Potassium** as the top predictors of soil fertility
- Built a practical recommendation system with real-world agricultural impact

---

## 👥 Team

| Name | Role |
|------|------|
| **Kanamarlapudi Bhargava Mani Rohith** | ML Model Development & Evaluation |
| **Mopuri Abhishiktha** | Data Preprocessing & Analysis |
| **Sai Venkata Ganesh Vattikonda** | Feature Engineering & Visualization |

**Institution:** School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, Coimbatore  
**Mentor:** Dr. Kritesh Kumar Gupta, Assistant Professor

---

## 📜 License

This project is developed for academic and educational purposes.  
Dataset sourced from Kaggle under their respective terms of use.

---

<p align="center">Made with ❤️ for smarter, sustainable agriculture 🌾</p>
