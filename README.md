# 📘 The Urban Resilience Index

### **A Multi-Output Machine Learning Framework for Predictive Wellness Modeling**

### Dataset & Project Documentation

## 🌍 Introduction

This repository contains the dataset, methodology, and preprocessing
workflow developed for the research paper:

**"The Urban Resilience Index: A Multi-Output Machine Learning Framework
for Predictive Wellness Modeling."**

The study introduces a comprehensive machine learning system capable of
predicting multiple wellness and resilience outcomes simultaneously,
ultimately generating a composite metric called the **Urban Resilience
Index (URI)**.

## 📂 Dataset Description

### File Included

    stress_detection_data.csv

### Dataset Summary

This dataset contains demographic, behavioral, environmental, and
psychological information, including multi-output targets: 
Stress_Level
- Resilience_Score
- Wellness_Status
- Environmental_Risk_Level

## 📊 Data Structure

Includes categorical, numerical, binary, and multi-output target
variables.

## 🧼 Preprocessing Workflow

1.  Load dataset
2.  Encode categorical features
3.  Handle missing values
4.  Split features & targets
5.  Train-test split
6.  Apply ML models

## 🧠 Machine Learning Models

Includes Random Forest, Gradient Boosting, XGBoost, LightGBM, CatBoost,
and Neural Networks for multi-output prediction.

## 📈 The Urban Resilience Index (URI)

Ranges from 0--100: - 0--30 → Low resilience\
- 31--60 → Moderate resilience\
- 61--100 → High resilience

## 🧪 Example Code

``` python
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split

df = pd.read_csv("stress_detection_data.csv")
categorical = df.select_dtypes(include=['object']).columns
le = LabelEncoder()
for col in categorical:
    df[col] = le.fit_transform(df[col])

targets = ["Stress_Level", "Resilience_Score", "Wellness_Status"]
X = df.drop(targets, axis=1)
y = df[targets]

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

## 📄 Citation
 S. Ahmed, S. Talukder, M. R. Khanom, S. Chakraborty, and M. A. Based,
“The Urban Resilience Index: A Multi-Output Machine Learning Framework for Predictive Wellness Modeling,” 2025.

## 📬 Contact

**Author:** 
Sabbir Ahmed

Sanjid Talukder

MST Romana Khanom

Swadhin Chakraborty

Engr. MD. Abdul Based 

**Email:** sanjidtalukder@gmail.com
