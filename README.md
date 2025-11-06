Predict and Recommend Healthier Indian Dishes using Machine Learning

This project uses machine learning and NLP to classify Indian dishes as healthy or unhealthy and suggest healthier alternatives through an interactive recommender system called NutriSwap.

## 🎯 Objective

To develop an AI-based nutritional recommendation system that:

Predicts a dish’s healthiness using ingredient and cooking features

Generates a health score (0–1) using Logistic Regression

Suggests similar but healthier alternatives using cosine similarity

## 🗂️ Dataset
 
Name: Indian Food 101 (Kaggle)

Attributes: dish name, ingredients, diet, flavor, region, cooking time

## ⚙️ Data Processing

Target Label: Created healthy (0/1) using a rule-based is_healthy_classifier()

Penalized: ghee, oil, sugar, fried, maida, cream

Rewarded: vegetables, lentils, yogurt

Cleaning & Encoding: Removed missing values, applied LabelEncoder

Feature Engineering:

healthy_ingredient_count, time_score, popularity_score

TF-IDF on ingredients (20 features)

Scaling: Standardized all numerical features

## 🧠 Model Training
Model	Accuracy	Remark
Logistic Regression	🥇 84.3%	Best model
SVM	82.4%	Close performance
MLP	72.5%	Overfit
KNN	70.6%	Poor generalization

✅ Final Model: Logistic Regression (ROC-AUC: 0.917)

## 📊 Evaluation

Excellent precision/recall for Unhealthy dishes (89%)

Good performance on Healthy dishes (71%)

Visualized via confusion matrix, ROC curve, and region-wise health scores

💡 The “NutriSwap” Recommender

Generates continuous health scores using predict_proba()

Finds similar dishes using cosine similarity

Filters for healthier options and ranks by health, similarity, and popularity

Example:
Input: Rasgulla (0.00) → Suggestions: Shufta, Pinaca, Dahi Vada

## 🧩 Tech Stack

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
Techniques: Logistic Regression, TF-IDF, Cosine Similarity
Environment: Google Colab, Kaggle Dataset

## 🚀 Future Scope

Add nutritional macros (calories, protein, fat, carbs)

Develop a web UI for interactive recommendations

Explore ensemble models (Random Forest, XGBoost)
