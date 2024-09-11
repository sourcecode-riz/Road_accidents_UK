# Big Data and Data Mining - Road Accident Analysis Report

**Author:** Muhammad Rizwan Arshad  
**Student ID:** 202255401

---

## Table of Contents
1. [Abstract](#abstract)
2. [Introduction](#introduction)
3. [Methodology](#methodology)
4. [Data Preprocessing](#data-preprocessing)
5. [Analysis](#analysis)
6. [Impacts of Apriori Algorithm](#impacts-of-apriori-algorithm)
7. [Clustering](#clustering)
8. [Outliers Detection](#outliers-detection)
9. [Models & Predictions](#models--predictions)
10. [Conclusion](#conclusion)
11. [References](#references)

---

## Abstract

Road accidents are complex events influenced by various factors presenting challenges for accident pattern analysis, prediction, and mitigation. This report uses UK traffic accident data from 2020 to enhance road safety measures. Predictive modeling and exploratory analysis were employed to uncover trends and generate actionable insights using various machine learning models.

---

## Introduction

Road accidents provide valuable insights into various aspects of safety. This report uses data-driven approaches to predict accidents and enhance safety measures. It focuses on utilizing machine learning models, like Support Vector Machine (SVM), Logistic Regression Model (LRM), and Random Forest Model (RFM), for accident severity prediction.

---

## Methodology

Data preprocessing involved handling missing values, outliers, and transforming data as required. The Apriori algorithm was employed to mine association rules, and models like SVM, LRM, and RFM were used to predict traffic accident severity. Computational limitations were considered in the model selection.

---

## Data Preprocessing

The dataset, sourced from the UK traffic accident database for 2020, was processed using SQLite. This involved the removal of duplicate columns, dealing with NaN values, and converting relevant columns to suitable formats (e.g., DateTime). 

---

## Analysis

Accidents were analyzed based on time, day, vehicle types, and categories.

### Accident Trends Over Time

- Accidents peaked at 8 AM and 5 PM, corresponding to rush hours.
- The highest number of accidents occurred on Fridays.

**Visuals:**
![Accidents by Time](./images/accidents_by_time.png)
![Accidents by Day](./images/accidents_by_day.png)

### Motorcycle Accident Analysis

- Motorcycles with engine capacities between 50cc and 125cc experienced the highest number of accidents.
- Fridays saw the highest accident counts.

**Visuals:**
![Motorcycle Accidents](./images/motorcycle_accidents.png)

### Pedestrian Accident Analysis

- Peak hours for pedestrian accidents were between 4 PM and 6 PM.
- 80% of pedestrian accidents occurred on weekdays.

**Visuals:**
![Pedestrian Accidents](./images/pedestrian_accidents.png)

---

## Impacts of Apriori Algorithm

The Apriori algorithm revealed associations between weather, light, and road conditions with accident severity. Below are some key rules:

- **Rule 1:** Fine weather without high winds is associated with slight accidents (Support: 0.6087, Confidence: 0.7787).
- **Rule 2:** Daylight conditions also showed strong associations with slight accidents.

**Visuals:**
![Apriori Rules](./images/apriori_rules.png)

---

## Clustering

The K-means clustering algorithm was used to analyze accident distribution by geographical region, focusing on Kingston upon Hull, Humberside, and East Riding of Yorkshire. 

**Visuals:**
![Geographical Clustering](./images/geographical_clustering.png)

---

## Outliers Detection

Outlier detection methods like IQR, Isolation Forest, and Local Outlier Factor were applied to detect anomalies in the accident dataset. These outliers were retained in the dataset since they represented real-world infrequent scenarios.

**Visuals:**
![Outlier Detection](./images/outlier_detection.png)

---

## Models & Predictions

Three machine learning models were used for accident severity prediction:

### Support Vector Machine (SVM)
SVM was configured with a polynomial kernel. Its results showed strong performance but slightly lower than the Random Forest model.

### Logistic Regression Model (LRM)
LRM demonstrated a simpler and interpretable approach, achieving satisfactory results.

### Random Forest Model (RFM)
RFM outperformed other models in accuracy, precision, recall, and F1-score.

**Performance Comparison:**
- **Accuracy:** RFM > LRM > SVM
- **Precision:** RFM > LRM > SVM
- **Recall:** RFM > LRM > SVM
- **F1-score:** RFM > LRM > SVM

**Visuals:**
![Model Performance](./images/model_performance.png)

---

## Conclusion

This study emphasized the value of data-driven approaches in predicting and mitigating road accidents. The Random Forest model provided the best predictive performance, while Apriori analysis offered valuable insights into accident patterns. Further research could refine the models and interventions for road safety.

---

## References

1. M. Z., J. R. J., & L. Y. Feng, "Towards big data analytics and mining for UK traffic accident analysis," 2020.
2. L. S. & H. G. Li, "Analysis of road traffic fatal accidents using data mining techniques," IEEE, 2017.
3. S. E. P., L. S. S., M. & K. A. Haynes, "Data analytics: Factors of traffic accidents in the UK," 2019.
