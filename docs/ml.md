---
layout: default
title: Machine Learning
nav_order: 4
---

# Machine Learning & Predictive Modeling

In this phase of the project, we aimed to build a robust predictive pipeline. Initially, our goal was to predict global digital interest based solely on domestic financial gaps. However, after evaluating the initial model's performance, we pivoted our strategy to a more highly correlated physical metric: **Stadium Attendance**.

## 1. Initial Attempt: Predicting Digital Interest
Our first model attempted to use the financial gap between the top two clubs in a league to predict the `League_Google_Interest`. We tested Linear Regression, K-Nearest Neighbors (KNN), and Decision Tree algorithms. 

As seen in our results, this approach yielded negative $R^2$ scores. This was a crucial finding: it empirically proved that global digital popularity is influenced by complex, non-linear external factors and cannot be predicted by a single domestic financial metric.

*(Görsel 1 buraya gelecek)*

## 2. Pivot & Optimization: Predicting Stadium Attendance
Based on project feedback and our findings, we shifted our target variable. Our new objective was to predict the **Average Stadium Attendance** using:
1. **Total Market Value:** Representing overall league quality.
2. **Google Interest:** Representing digital popularity.

*(Görsel 2: Decision Tree Structure buraya gelecek)*

## 3. Final Results
This alternative model demonstrated remarkable predictive power. Our **Decision Tree Regressor** perfectly captured the non-linear relationships in the data, achieving an impressive **$R^2$ Score of 0.8143**. 

*(Görsel 3: Final Prediction Graph buraya gelecek)*

This successfully proves that when combined, financial power and digital presence can highly accurately predict physical fan loyalty.
