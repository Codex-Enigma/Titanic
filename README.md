# 🚢 Titanic Survival Prediction - Internship Assessment Project

## 📌 Project Overview
The objective of this project is to build a machine learning model that predicts the survival of Titanic passengers based on passenger features like age, sex, fare, class, and family relations.

This project demonstrates:
- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model Building using Scikit-Learn Pipelines and Logistic Regression
- Model Evaluation
- Custom Prediction Function for new passenger data

---

## 📂 Dataset Information
- **Source:** Dataset provided in the internship assessment (based on Kaggle's Titanic dataset).
- **Known Flaw:** 
  - The dataset is biased — only females survived and males did not.
  - This makes the model heavily depend on the 'Sex' feature.
  - The flaw is documented and acknowledged.

---

## 🛠️ Tech Stack & Libraries
- **Python**
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, ydata-profiling (for automated EDA report generation)
- **Jupyter Notebook** for EDA and Model building

Install all dependencies using the following command:
```bash
pip install -r requirements.txt
```

## 🚀 How to Run the Project
🔄 Clone the Repository
```bash
git clone <https://github.com/Codex-Enigma/Titanic>
cd Titanic
```

Run the Jupyter Notebook
```bash
jupyter notebook titanic.ipynb
```

---
## 🧠 Project Highlights & Innovation
✅ Data Cleaning and Handling Missing Values

✅ EDA using Matplotlib and Seaborn

✅ Feature Engineering: Title extraction, family size, deck knowledge

✅ Scikit-Learn Pipelines and ColumnTransformers

✅ Logistic Regression Model

✅ Cross-Validation for model robustness

✅ Custom prediction function for single passenger input

✅ Readable, modular, and well-commented code

✅ Acknowledgment of dataset flaw

---

## 📈 Model Evaluation Metrics
Accuracy Score
Precision, Recall, F1-Score
Cross-validation score for generalization

## 📊 Sample Classification Report:
```bash
Classification Report:
               precision    recall  f1-score   support

           0       1.00      1.00      1.00        50
           1       1.00      1.00      1.00        34

    accuracy                           1.00        84
   macro avg       1.00      1.00      1.00        84
weighted avg       1.00      1.00      1.00        84
```

---
## 🔍 Exploratory Data Analysis (EDA) Highlights

🔹 Count plots of survivors by gender and class

🔹 Generated an automated EDA report using **ydata-profiling** to summarize data insights, missing values, and  feature distributions.

🔹Age distribution

🔹Fare distribution (Box plot)

🔹Correlation heatmap

🔹Survival Count by Gender

🔹Title Extraction Impact

🔹Embarked Location Analysis
  
🔹IsAlone Feature

 ## 📌 Insights from EDA:
🔹 Gender Bias: Females have a 100% survival rate, males have 0%.

🔹 Pclass Distribution: Higher-class passengers had higher survival chances.

🔹 Age Distribution: Younger passengers showed better survival chances.

🔹 Fare Analysis: Higher fare correlates with higher survival.

🔹 Family Size Impact: Family presence influences survival.

🔹 Dataset Bias: The model is highly biased due to gender imbalance.

---

## 🖥️ Example Prediction for a New Passenger
Use the following function inside the notebook:
```bash
predict_passenger(pipeline, {
    'Pclass': 3, 'Sex': 'male', 'Age': 22, 'SibSp': 1, 'Parch': 0, 
    'Fare': 7.25, 'Embarked': 'S', 'FamilySize': 2, 'IsAlone': 0, 
    'Title': 'Mr', 'Is_Deck_Known': 0
})
```
```bash
Sample Output:
Prediction: Did Not Survive
```
