# Competitive Balance and Fan Engagement in Football

---

## Overview
This project aims to analyze the socio-economic impact of financial disparity in modern football. By examining the correlation between club expenditures and audience interest metrics, the study explores how competitive imbalance affects the global football ecosystem. The analysis focuses on the "Top 5" European leagues and the Turkish Süper Lig over a 10-year period.

---

## Motivation
Football has been my biggest passion since childhood, both as a player and a fan. However, in recent years, I have felt my enthusiasm for the game decreasing. I believe the main reason is the massive financial gap between clubs. Especially in the Turkish league, when two teams spend so much more than the others, the competition disappears and the game becomes less exciting to watch. 

To provide a structured analysis, I have categorized the six leagues into three distinct groups based on their competitive landscapes:

| GROUPS | DESCRIPTION |
| :--- | :--- |
| **Dominant Leagues** | Systems where a single club maintains long-term dominance (e.g., Bundesliga, Ligue 1). |
| **Top-Heavy Leagues** | Systems generally dominated by 2, and sometimes 3, major powerhouses (e.g., La Liga, Süper Lig). |
| **Balanced Leagues** | Systems with high parity and multiple title contenders (e.g., Premier League, Serie A). |

---

## Data Sources & Collection Plan
The project integrates financial performance data with digital engagement metrics to create a multi-dimensional dataset.

### 1. Primary Financial & Performance Data
* **Source:** Official records from **Transfermarkt** and **FBref**.
* **Data Points:** Annual transfer expenditures, final league points, and championship margins.
* **Collection Method:** Data will be extracted using Python scripts and official CSV exports to ensure historical accuracy.

### 2. Fan Engagement (Enrichment Data)
* **Digital Interest:** Tracking search volume trends via the Google Trends API (pytrends).
* **Media Reach:** Analyzing publicly available broadcasting ratings and stadium attendance reports to measure physical and digital loyalty.

---

## Data Characteristics
* **Temporal Scope:** A longitudinal study covering 10 full seasons (2015–2025).
* **Sample Density:** With an average of 20 teams per league, the core dataset includes approximately 1,200 unique samples.
* **Structure:** The data will be structured as a comprehensive time-series, allowing for the analysis of seasonal fluctuations in fan interest relative to league predictability.

---

## Analysis & Methodology Plan
1. **Data Preprocessing:** Cleaning and merging financial datasets with Google Trends scores using Pandas to create a unified "Year-League" master table.
2. **Exploratory Data Analysis (EDA):** Visualizing the "Spending Gap" vs. "Audience Interest" using scatter plots and line charts to identify visible trends.
3. **Correlation Analysis:** Applying statistical tests (Pearson/Spearman) to measure the strength of the relationship between league parity and digital engagement.
4. **Hypothesis Testing:** Testing whether "Balanced Leagues" maintain significantly higher and more stable interest levels compared to "Dominant Leagues."
5. **Predictive Modeling:** Attempting to build a Machine Learning regression model to forecast future fan engagement based on mid-season financial and competitive metrics.

---

## Expected Findings
* A strong negative correlation is expected between "Championship Point Gaps" and "Digital Search Interest."
* It is anticipated that financial dominance by 1 or 2 teams leads to a decline in audience engagement from neutral fans.
* The study expects to show that "Balanced Leagues" are more resilient to digital interest drops compared to "Dominant Leagues" leagues.

---

## Progress Report 1: Statistical Analysis & Hypothesis Testing

In this phase, we moved beyond exploratory visualizations and applied rigorous statistical testing to evaluate the relationship between the Financial Gap (market value difference between the top 2 teams) and Digital Engagement across the six leagues.

### Methodology:
* **Correlation Analysis:** We conducted Pearson Correlation tests individually for each league to measure the linear relationship between financial disparity and search interest. A significance level of $\alpha = 0.05$ was established.
* **Group Comparison (ANOVA):** To test the core hypothesis regarding league structures, we grouped the leagues into three categories (Balanced, Dominant, Top-Heavy) and performed a One-Way ANOVA test to determine if the mean digital interest significantly differed across these groups.

### Key Findings & Results:
* **Rejection of the Null Hypothesis:** The ANOVA test yielded a highly significant result ($p\text{-value} = 0.0066$, which is $< 0.05$). This allowed us to confidently reject the null hypothesis ($H_0$), mathematically proving that the structural type of a league (how competitive it is) has a statistically significant impact on its average global engagement.
* **League-Specific Nuances:** The Pearson tests revealed that the impact of financial disparity is highly context-dependent. While Top-Heavy leagues (like the Süper Lig) showed negative correlations indicating stagnation when the gap widened, Balanced and Dominant leagues exhibited different behaviors, proving that the relationship is not universally linear.

---

## Progress Report 2: Machine Learning & Predictive Modeling

To deeply investigate whether financial disparity can accurately predict digital interest, a comprehensive machine learning pipeline was developed.

### Methodology & Data Preparation:
* **Scaling:** The dataset was normalized using `MinMaxScaler` to ensure proper functionality for distance-based algorithms.
* **Validation:** A `Train-Test Split (80/20)` was implemented to evaluate the models' generalization performance on unseen data.

### Model Selection:
Three algorithms with varying complexities were evaluated to capture different types of underlying patterns:
1. **Linear Regression:** To test for simple, global linear trends.
2. **K-Nearest Neighbors (KNN):** To capture local similarities among leagues with comparable financial structures.
3. **Decision Tree Regressor:** To account for non-linear, threshold-based jumps in popularity.

### Results & Interpretation:
* **Linear Underfitting:** The Linear Regression model yielded negative R-Squared scores, failing to capture the high variance of the data. This mathematically proves that global audience engagement is not a simple straight-line function of the financial gap.
* **Non-Linear Dynamics:** The Decision Tree and KNN models adapted much better to the dataset. The step-wise structure of the Decision Tree predictions illustrates that audience interest operates on specific financial thresholds (e.g., the sudden emergence of a "super club" or a critical gap limit) rather than continuous linear scaling.
* **Conclusion:** The ML analysis confirms that while financial disparity is an influential factor, predicting digital interest solely through the financial gap is insufficient due to the complex, non-linear nature of the global football ecosystem.
