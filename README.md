# Heart Disease Prediction Project

## 📌 Overview
This project uses machine learning techniques to predict the presence of heart disease based on clinical data.  
The dataset is sourced from the **UCI Machine Learning Repository** (Heart Disease dataset, ID = 45).

The workflow includes:
- Data loading & preprocessing
- Feature selection (Random Forest importance, RFE, Chi-Square test)
- Model training & evaluation (Logistic Regression, Decision Tree, Random Forest, SVM)
- Hyperparameter tuning (GridSearchCV & RandomizedSearchCV)
- Clustering analysis (K-Means, Hierarchical Clustering)
- Model performance comparison using multiple metrics

---

## ⚙️ Installation
Clone the repository and install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage
Run the notebook to reproduce the analysis:

```bash
jupyter notebook heart_disease_full.ipynb
```

---

## 📊 Evaluation Metrics
Models were evaluated using:
- Accuracy
- Precision (weighted)
- Recall (weighted)
- F1-score (weighted)
- ROC AUC (OvR, multi-class)
- Confusion Matrix
- Adjusted Rand Index (for clustering)

See `evaluation_metrics.txt` for detailed explanations.

---

## 🏆 Results Summary
- **Decision Tree** → Highest **F1-score** and **Precision**, making it suitable when balancing false positives & false negatives is important.  
- **Logistic Regression** → Best **ROC AUC**, meaning it is strongest at distinguishing between classes.  
- **Random Forest & SVM** → Competitive in **Accuracy** and **Recall**.  
- **Clustering (K-Means, Hierarchical)** → Showed limited alignment with true diagnostic categories (low ARI).  

**Conclusion:**  
The best model depends on the application’s priorities:  
- If balance between Precision & Recall is most important → **Decision Tree**  
- If discrimination between positive and negative cases is key → **Logistic Regression**  
- For robust overall performance → **Random Forest** or **SVM**  

Further validation with cross-validation or larger datasets is recommended.

---

## 📂 Project Structure
```
heart_disease_full.ipynb   # Main analysis notebook
evaluation_metrics.txt     # Explanation of evaluation metrics
requirements.txt           # Dependencies
README.md                  # Project documentation
```
