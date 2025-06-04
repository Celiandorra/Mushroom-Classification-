# 🍄 Mushroom Classification with Explainable AI

## Overview

This project presents a comparative analysis of **machine learning** and **deep learning** models for classifying mushrooms as **edible** or **poisonous**, based on their physical characteristics.

A key focus is placed on **model explainability** using **SHAP (SHapley Additive exPlanations)** to understand the influence of each feature in the model's decision-making process.

> 🔗 [Project Repository](https://github.com/Celiandorra/Mushroom-Classification-)

## Dataset

- **Source:** [Kaggle - Mushroom Classification Dataset](https://www.kaggle.com/datasets/uciml/mushroom-classification)
- **Target Variable:** `class` (0 = edible, 1 = poisonous)
- **Features:** 22 physical and morphological features (e.g., cap shape, gill color, stem height)

---

## Models Used

### Traditional Machine Learning
- **Logistic Regression (LR)**  
  - Baseline model, interpretable, but underperforms due to linear assumptions.

- **k-Nearest Neighbors (KNN)**  
  - Non-parametric, moderate performance, sensitive to data scaling and size.

- **Random Forest (RF)**  
  - Best traditional model with near-perfect accuracy and strong interpretability.

### Deep Learning
- **Multi-Layer Perceptron (MLP)**  
  - Captures non-linear relationships, moderate performance, less effective than RF.

- **Artificial Neural Network (ANN)**  
  - High-performing, requires extensive hyperparameter tuning and regularization.

- **TabNet**  
  - Attention-based architecture tailored for tabular data, excellent performance with interpretability.

---

## Explainability with SHAP

To demystify model predictions, SHAP is used to:
- Assess **global feature importance**
- Analyze **local instance-based predictions**
- Visualize **force plots** and **waterfall plots**

### Most Influential Features
- Cap Shape
- Cap Diameter
- Stem Height & Width
- Gill Attachment
- Stem Color

---

## Evaluation Metrics

Models were evaluated using:
- Accuracy
- Precision & Recall
- F1-Score
- ROC-AUC
- SHAP-based feature insights

### Summary of Results

| Model            | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|------------------|----------|-----------|--------|----------|----------|
| Logistic Regression | 0.64     | 0.65      | 0.64   | 0.64     | 0.70     |
| KNN              | 0.72     | 0.73      | 0.72   | 0.72     | 0.72     |
| Random Forest    | 0.99     | 0.99      | 0.99   | 0.99     | 1.00     |
| MLP              | 0.74     | 0.82      | 0.68   | 0.74     | 0.84     |
| TabNet           | 0.98     | 0.98      | 0.98   | 0.98     | 1.00     |
| ANN              | 0.97     | 0.96      | 0.97   | 0.97     | 1.00     |

---

## ⚙Tools & Libraries

- `Python`
- `Scikit-learn`
- `TensorFlow / Keras`
- `Optuna` (for ANN tuning)
- `SHAP`
- `Pandas`, `NumPy`
- `Matplotlib`, `Seaborn`

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Celiandorra/Mushroom-Classification-
   cd Mushroom-Classification-
    ```

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the analysis:

   ```bash
   python main.py
   ```

Or open and explore the notebooks in the `notebooks/` folder for a more detailed walkthrough.

---

## Project Structure

```
Mushroom-Classification-/
├── data/                 # Raw dataset files
├── notebooks/            # EDA, model training, and SHAP analysis
├── models/               # Trained model files (if saved)
├── shap_analysis/        # SHAP plots & feature visualizations
├── main.py               # Entry point script
├── requirements.txt      # Project dependencies
└── README.md
```

---

## Author
**Dorra Ben Abdallah**

Business Analytics & IT | Machine Learning Enthusiast
🔗 [GitHub](https://github.com/Celiandorra)



