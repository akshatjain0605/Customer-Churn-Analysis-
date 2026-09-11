# 📉 Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-lightgrey)

---

## 🏢 Project Overview

This project predicts **customer churn** for a telecom-style customer base using historical account, service, and demographic data.
It combines **data cleaning, feature encoding, and machine learning classification** with an **interactive Power BI dashboard** to help identify at-risk customers and support data-driven retention strategies.

---

## 📌 Objectives

This project focuses on:
- Cleaning and preparing raw customer churn data
- Encoding categorical variables for model readiness
- Training a classification model to predict churn
- Identifying key drivers behind customer attrition
- Visualizing churn trends and risk segments in Power BI

---

## 🧠 Dataset Information

The dataset (`vw_churndata.csv`) contains **6,000+ customer records** with 30+ features, including:

| Feature | Description |
|----------|-------------|
| Customer_ID | Unique customer identifier |
| Gender, Age, Married | Customer demographics |
| State | Customer location |
| Tenure_in_Months | Duration of customer relationship |
| Value_Deal | Subscribed plan/deal type |
| Phone_Service, Multiple_Lines | Phone service details |
| Internet_Service, Internet_Type | Internet service details |
| Online_Security, Online_Backup, Device_Protection_Plan | Add-on services |
| Streaming_TV, Streaming_Movies, Streaming_Music | Entertainment add-ons |
| Contract, Paperless_Billing | Account and billing details |
| Churn_Category, Churn_Reason | Reason for churn (target-related) |

A separate file (`vw_joindata.csv`) containing new/unseen customer records is used to generate churn predictions for the current customer base, saved to `Predictions.csv`.

---

## ⚙️ Technologies Used

- 🐍 **Python 3**
- 📊 **Pandas, NumPy** – Data cleaning and manipulation
- 🤖 **Scikit-learn** – Label encoding, model training, and evaluation
- 📈 **Matplotlib, Seaborn** – Feature importance and visualization
- 📊 **Power BI** – Interactive churn dashboard
- 📓 **Jupyter Notebook** – Development environment

---

## 🔍 Analysis & Modeling

The following steps were performed:
- **Data Cleaning** – Removed non-predictive identifiers (`Customer_ID`, `Churn_Category`, `Churn_Reason`)
- **Categorical Encoding** – Label-encoded 15+ categorical features (Gender, Contract, Internet_Type, etc.)
- **Model Training** – Built a **Random Forest Classifier** on the processed dataset
- **Model Evaluation** – Assessed performance using a confusion matrix and classification report
- **Feature Importance** – Ranked features by contribution to churn prediction
- **Batch Prediction** – Applied the trained model to new customer data to flag likely churners

**Key Insights:**
- Contract type and tenure are strong indicators of churn risk
- Customers without add-on services (security, backup, protection plans) show higher churn tendency
- The model successfully flags high-risk customers for proactive retention outreach

---

## 📊 Power BI Dashboard

An interactive Power BI dashboard was built on top of the churn data and model predictions to visualize:
- Overall churn rate and customer segments
- Churn breakdown by contract type, tenure, and services
- High-risk customer lists for targeted retention campaigns

---

## 📈 Results

- Cleaned and processed **6,000+ customer records** for modeling
- Trained a **Random Forest Classifier** to predict customer churn
- Generated churn predictions for **380+ new customers**
- Delivered an interactive Power BI dashboard for ongoing churn monitoring
- Established a repeatable pipeline for churn prediction and retention analysis
