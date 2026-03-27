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
