# ❤️ Heart Disease Prediction using Machine Learning

## 📌 Project Overview

Heart disease is one of the leading causes of death worldwide. Early prediction can help healthcare professionals identify high-risk patients and provide timely treatment.

In this project, multiple Machine Learning classification algorithms were developed and evaluated to predict whether a patient has heart disease using the **UCI Heart Disease (Cleveland) Dataset**. The models were compared using several evaluation metrics, followed by hyperparameter tuning to improve performance and select the best model.

---

## 🎯 Objective

The objective of this project is to build an accurate machine learning model that predicts the presence of heart disease based on various clinical features.

---

## 📂 Dataset

* **Dataset:** UCI Heart Disease (Cleveland) Dataset
* **Number of Records:** 303
* **Number of Features:** 13
* **Target Variable:** Heart Disease

  * **0** → No Heart Disease
  * **1** → Heart Disease

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Joblib

---

## 📊 Exploratory Data Analysis (EDA)

The following analyses were performed:

* Checked dataset structure and data types.
* Identified and handled missing values.
* Analyzed target class distribution.
* Generated a correlation heatmap.
* Visualized important relationships such as:

  * Age vs Heart Disease
  * Maximum Heart Rate vs Heart Disease
  * Chest Pain Type vs Heart Disease
* Examined Random Forest feature importance.

---

## ⚙️ Data Preprocessing

The dataset was prepared using the following preprocessing steps:

* Replaced missing values (`?`) with `NaN`.
* Converted categorical numeric columns to appropriate data types.
* Filled missing values using the median.
* Converted the target variable into binary classes.
* Split the dataset into training and testing sets.
* Applied Standard Scaling for models sensitive to feature scaling (Logistic Regression and Support Vector Machine).

---

## 🤖 Machine Learning Models

The following baseline models were trained and evaluated:

* Logistic Regression
* Support Vector Machine (SVM)
* Random Forest
* XGBoost

---

## 🔧 Hyperparameter Tuning

To improve model performance, hyperparameter tuning was performed using **RandomizedSearchCV**.

The following models were optimized:

* Random Forest
* XGBoost

Since this is a medical diagnosis problem, **Recall** was used as the optimization metric to reduce false negatives and maximize the detection of patients with heart disease.

---

## 📈 Model Performance

| Model                  |   Accuracy |  Precision |     Recall |   F1-Score |    ROC-AUC |
| ---------------------- | ---------: | ---------: | ---------: | ---------: | ---------: |
| Random Forest (Tuned)  | **91.80%** | **87.10%** | **96.43%** | **91.53%** | **96.21%** |
| Random Forest          |     88.52% |     83.87% |     92.86% |     88.14% |     95.18% |
| Logistic Regression    |     86.89% |     81.25% |     92.86% |     86.67% |     95.13% |
| XGBoost (Tuned)        |     86.89% |     83.33% |     89.29% |     86.21% |     95.45% |
| XGBoost                |     85.25% |     78.79% |     92.86% |     85.25% |     91.88% |
| Support Vector Machine |     85.25% |     80.65% |     89.29% |     84.75% |     94.37% |

---

## 🏆 Best Model

The **Tuned Random Forest** model achieved the best overall performance.

**Final Performance:**

* Accuracy: **91.80%**
* Precision: **87.10%**
* Recall: **96.43%**
* F1-Score: **91.53%**
* ROC-AUC: **96.21%**

---

## 💾 Model Saving

The best-performing model was saved using **Joblib** for future predictions.

```python
joblib.dump(best_rf, "heart_disease_model.pkl")
```

---

## 📁 Project Structure

```
Heart-Disease-Prediction/
│
├── Heart_Disease_Prediction.ipynb
├── processed.cleveland.data
├── heart_disease_model.pkl
├── READmd
├── requiremME.ents.txt/
```

---

## 📚 Key Learnings

During this project, I learned how to:

* Work with a real-world healthcare dataset.
* Handle missing values and preprocess medical data.
* Perform exploratory data analysis to identify patterns.
* Build and compare multiple machine learning classification models.
* Evaluate models using Accuracy, Precision, Recall, F1-Score, ROC-AUC, and Confusion Matrix.
* Apply RandomizedSearchCV for hyperparameter tuning.
* Select evaluation metrics based on the problem domain.
* Save a trained machine learning model for future use.

---

## 🚀 Future Improvements

Possible improvements for this project include:

* Training on larger and more diverse healthcare datasets.
* Applying advanced feature engineering techniques.
* Using Bayesian Optimization or Optuna for hyperparameter tuning.
* Deploying the model using Flask or Streamlit.
* Validating the model on external datasets to evaluate generalization performance.

---

## 📝 Conclusion

This project demonstrates a complete end-to-end machine learning workflow for heart disease prediction. Multiple classification algorithms were trained, evaluated, and compared, followed by hyperparameter tuning to improve performance.

Among all the evaluated models, the **Tuned Random Forest** model achieved the best overall performance and was selected as the final model. Since this is a medical diagnosis problem, priority was given to **Recall** during model optimization to minimize false negatives and improve the detection of patients with heart disease.

This project highlights the importance of combining proper data preprocessing, model evaluation, and domain-specific metric selection to build reliable machine learning solutions for healthcare applications.
