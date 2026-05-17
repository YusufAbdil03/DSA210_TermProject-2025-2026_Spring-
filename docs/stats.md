---
layout: default
title: Statistical Analysis
nav_order: 3
---

# Statistical Analysis & Hypothesis Testing

In this section, we apply rigorous statistical methods to test our core hypothesis: Does the financial disparity within a league significantly impact its global digital popularity? To ensure a comprehensive analysis, we evaluated the "Top 5" European leagues alongside the Turkish Süper Lig.

## 1. Global Analysis: One-Way ANOVA (Group Comparison)
We categorized the leagues into three structural groups based on their financial distribution and competitive balance. 

**Hypotheses:**
* **H0 (Null Hypothesis):** There is no significant difference in average fan interest between the defined league groups.
* **H1 (Alternative Hypothesis):** At least one league group shows a statistically significant difference in average fan interest.

**Significance Level (alpha):** 0.05

**Test Results:**
* **F-Statistic:** 5.4772
* **P-value:** 0.0066

*(Görsel 1: ANOVA veya Hipotez Testi Genel Grafiği buraya gelecek)*

**Final Decision & Interpretation:**
Since the p-value (0.0066) is significantly lower than our alpha (0.05), we strongly **reject the null hypothesis (H0)**. This result provides strong statistical evidence that the structural differences between these league groups lead to significantly different levels of global digital engagement.

## 2. Overall Correlation Overview
Before diving into the micro-dynamics of each league, we established the baseline correlation between financial disparities and fan engagement across our entire 10-year dataset.

*(Görsel 2: Genel Korelasyon / Dağılım Grafiği buraya gelecek)*

## 3. League-Specific Trends
To truly understand the socio-economic impact of financial gaps, we isolated the financial difference between the top 2 clubs and compared it against Google Interest for each of the 6 leagues individually.

### English Premier League
*(Görsel 3: Premier League Grafiği buraya gelecek)*

### Spanish La Liga
*(Görsel 4: La Liga Grafiği buraya gelecek)*

### Italian Serie A
*(Görsel 5: Serie A Grafiği buraya gelecek)*

### German Bundesliga
*(Görsel 6: Bundesliga Grafiği buraya gelecek)*

### French Ligue 1
*(Görsel 7: Ligue 1 Grafiği buraya gelecek)*

### Turkish Süper Lig
*(Görsel 8: Süper Lig Grafiği buraya gelecek)*

## Conclusion of Statistical Testing
This comprehensive 6-league breakdown mathematically bridges the gap between our Exploratory Data Analysis (EDA) and our Machine Learning phase. While local league dynamics may vary slightly, this section conclusively proves that financial imbalance is a statistically significant factor in modern football's global ecosystem.
