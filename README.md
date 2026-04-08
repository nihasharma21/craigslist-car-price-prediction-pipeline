# 🚗 Craigslist Car Price Prediction Pipeline

## 🔍 Problem
Used car listings on Craigslist are highly unstructured and inconsistent, making it difficult to estimate fair prices.  
This project builds a system to extract structured data, predict prices, and continuously evaluate model performance over time.

---

## 💡 What I built
- End-to-end pipeline to:
  - Scrape Craigslist listings  
  - Extract structured features using LLM + regex  
  - Predict prices using machine learning  
- Enhanced feature set with:
  - color, transmission, fuel_type, drive_type, vehicle_type, condition, title_status  
- Improved model using Random Forest with hyperparameter tuning  
- Built a model trending system to track performance over time  
- Added interpretability using:
  - Permutation Importance  
  - Partial Dependence Plots (PDP)  

---

## 📈 Key Insights & Analysis

### 1. Improved model performance
- Tuned model consistently outperforms baseline (Decision Tree)  
- Lower error across MAE, RMSE, and MAPE  

📸 *(Add screenshot: model_performance_trend.png)*
<img width="1118" height="607" alt="Improved Model performance over baseline" src="https://github.com/user-attachments/assets/6297ce5c-b5ae-447b-8f6e-cf88f49cae1a" />

---

### 2. Model stability over time
- Performance tracked across multiple data refresh cycles  
- Model remains stable as new listings are added  

📸 *(Add screenshot: cumulative_model_performance_trend.png)*

---

### 3. Feature importance (what drives price)
- Mileage and year are consistently the strongest predictors  
- Newly added features (condition, fuel type, etc.) add meaningful signal  

📸 *(Add screenshot: permutation_importance.png)*

---

### 4. How the model behaves (PDP)
- Mileage shows a clear negative relationship with price  
- Year shows a positive relationship  
- Model behavior remains consistent across datasets  

📸 *(Add screenshots: pdp_mileage_num.png, pdp_year_num.png, pdp_make.png)*

---

## 🧠 What I learned
- Moving from static modeling to continuous evaluation over time  
- Integrating LLM-based ETL with machine learning models  
- Balancing automation vs practical delivery in real pipelines  
- Thinking in terms of systems, monitoring, and real-world performance  

---

## 📁 Repository Structure

- notebooks/ → Model trending notebook (performance + interpretability analysis)  
- model_outputs/ → PDP plots, feature importance, and performance trends  
- results/ → Prediction outputs generated over time  
- data/ → Structured dataset used for training  
- model/ → Model training and improvements  
- cloud_function/ → Pipeline components  

---

## 🧪 How to run

1. Open the notebook:  
   `notebooks/model_trending.ipynb`

2. Run all cells to:
   - Load data  
   - Train model  
   - Compare performance  
   - Generate insights  

---

## 🎯 Why this matters

This project demonstrates:
- Ability to transform messy real-world data into structured insights  
- Model improvement beyond baseline  
- Continuous monitoring of model performance  
- Strong focus on analysis, decision-making, and business relevance  

---

## 🔗 Notebook

👉 Add your Colab link here  

---

## 📝 Note
This is a portfolio version of the project. The original implementation included automated pipelines using GCP and GitHub Actions.
