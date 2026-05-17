# Competitive Balance and Fan Engagement in Football
**DSA210 Term Project — Spring 2025-2026** *Created by Yusuf*

---

## Overview
This project delivers a multi-dimensional, data-driven analysis of the socio-economic impact of financial disparity in modern football. By fusing financial metrics (club market values and expenditures) with dual-layered fan engagement metrics (digital search interest and physical stadium attendance), this study explores how structural competitive imbalances shape the global football ecosystem. The spatial scope covers the European "Top 5" leagues (English Premier League, Spanish La Liga, Italian Serie A, German Bundesliga, French Ligue 1) alongside the Turkish Süper Lig over a 10-year longitudinal period (2015–2025).

---

## Motivation
Football has been my biggest passion since childhood, both as an active player and a dedicated fan. However, in recent years, I have felt my enthusiasm for the game steadily decreasing. I believe the core catalyst behind this shift is the massive, compounding financial gap between clubs. Especially observed in the Turkish domestic league, when a tiny pocket of teams spend exponentially more than the rest of the matrix, genuine competition evaporates, matches become highly predictable, and the game loses the raw excitement that defines its essence. 

To transition this personal observation into a structured empirical study, I categorized the six leagues into three distinct operational frameworks based on their structural competitive landscapes:

| Macro Group | Leagues Covered | Structural Description |
| :--- | :--- | :--- |
| **Dominant Leagues** | Bundesliga, Ligue 1 | Ecosystems where a single absolute club maintains long-term, unyielding domestic dominance. |
| **Top-Heavy Leagues** | La Liga, Süper Lig | Ecosystems structurally dominated by 2, and occasionally 3, major historical powerhouses. |
| **Balanced Leagues** | Premier League, Serie A | Ecosystems exhibiting high internal parity with multiple viable title contenders. |

---

## Data Sources & Collection Plan
The engineering architecture of this project relies on integrating primary financial datasets with granular fan loyalty metrics.

### 1. Primary Financial & Performance Metrics
* **Sources:** Historical ledgers from **Transfermarkt** and **FBref**.
* **Data Points:** Seasonal squad market values, annual transfer expenditures, final league table point distributions, and geometric championship margins.
* **Collection Method:** Extracted via automated Python scraping scripts and targeted CSV compilation to guarantee absolute historical and mathematical tracking.

### 2. Fan Engagement Tracking (Enrichment Layer)
* **Digital Footprint:** Capturing global search volume trends and media curiosity using the Google Trends API (`pytrends`) to establish a baseline for digital interest.
* **Physical Footprint:** Compiling publicly disclosed matchday stadium attendance reports and aggregate seasonal stadium capacities to measure physical, real-world loyalty.

---

## Data Characteristics
* **Temporal Scope:** A longitudinal analysis spanning 10 complete consecutive competitive seasons (2015–2025).
* **Sample Density:** Accounting for an average density of 20 teams per league across 6 independent nations, the finalized master database contains approximately **1,200 unique team-level records**, aggregated into 60 comprehensive "Year-League" master macro-samples.
* **Structure:** Constructed as a structured time-series matrix, enabling the analysis of temporal fluctuations in fan retention relative to financial and competitive polarization.

---

## Analysis & Methodology Plan
1. **Data Preprocessing:** Standardizing data scales, handling cross-currency values, and executing precise outer joins to merge Transfermarkt records with Google Trends metrics into a central master database using Pandas.
2. **Exploratory Data Analysis (EDA):** Engineering visual frameworks to map the "Spending Gap" against digital interest shifts across different cultures.
3. **Correlation Diagnostics:** Executing rigorous statistical tests (Pearson & Spearman coefficients) to evaluate the exact linear and monotonic bonds between parity indicators and engagement.
4. **Hypothesis Testing:** Deploying advanced statistical frameworks (ANOVA models and Supplementary Multi-Variable Correlations) to determine if macro-structures explicitly govern audience stability.
5. **Predictive Modeling:** Developing non-linear Machine Learning pipelines to forecast real-world fan behaviors based on preceding economic indicators.

---

## Expected Findings (Initial Assumptions)
* A sharp, highly predictable negative linear correlation between expanding championship point margins and global digital interest.
* Empirical proof that severe financial dominance by an elite duopoly or monopoly triggers a severe drop in engagement from neutral audiences.
* Statistical validation that "Balanced Leagues" showcase far higher resilience against fan interest drops compared to rigid, single-team dominated systems.

---

## Phase 1: Advanced Statistical Analysis & Hypothesis Testing

Rather than relying on flat visualizations, this phase implemented rigorous statistical verification across 4 distinct hypothesis frameworks to analyze the ecosystem from global, structural, physical, and temporal angles.

### 1. Global Structural Group Comparison (One-Way ANOVA)
* **Objective:** Test if the defined league frameworks (Balanced, Dominant, Top-Heavy) yield statistically distinct baselines of global digital interest.
* **Hypotheses:** * $H_0$: There is no significant difference in mean digital interest across the three structural archetypes.
  * $H_1$: At least one league structure exhibits a statistically different mean interest level.
* **Results:** $F\text{-Statistic} = 5.4772$, **$P\text{-value} = 0.0066$** ($\alpha = 0.05$).
* **Conclusion:** **Reject $H_0$.** This mathematically establishes that the macro-competitive design of a league directly governs its digital footprint on a global stage.

### 2. Internal Financial Gap vs. Average Stadium Attendance (Pearson Correlation)
* **Objective:** Test if expanding domestic inequality physically drives local match-going fans away from stadiums.
* **Hypotheses:**
  * $H_0$: There is no linear relationship between a league's maximum financial gap and its physical stadium crowds.
  * $H_1$: A significant linear correlation exists between the financial gap and attendance.
* **Results:** Correlation Coefficient ($r$) = **$0.6941$**, **$P\text{-value} = 0.0000$** (rounded from $< 0.0001$).
* **Conclusion:** **Strongly Reject $H_0$.** This exposes a fascinating socio-economic paradox: wider financial divides strongly link to *higher* physical stadium attendance. The extreme concentration of capital allows elite clubs to secure world-class superstars, transforming matches into global premium spectacles that draw massive crowds, completely outweighing the negative sentiment surrounding reduced domestic parity.

### 3. Total League Value vs. Internal Inequality (Trickle-Down Economic Analysis)
* **Objective:** Test if capital growth within a league "trickles down" to lower-tier teams, stabilizing parity, or if it accelerates internal divide.
* **Hypotheses:**
  * $H_0$: Total league market value has no correlation with internal financial standard deviation.
  * $H_1$: Total value and internal standard deviation share a significant correlation.
* **Results:** Correlation Coefficient ($r$) = **$0.8434$**, **$P\text{-value} = 2.74 \times 10^{-17}$** ($< 0.0001$).
* **Conclusion:** **Strongly Reject $H_0$.** This definitive finding completely debunks the trickle-down economic theory in sports analytics. As a league successfully injects more capital and grows its total valuation, the financial standard deviation scales up proportionally. New revenue streams are heavily captured by the top elite, directly amplifying polarization.

### 4. Temporal Shift Analysis (The Financial Divide Over Time)
* **Objective:** Test whether the financial gap is static or systematically compounding over the last decade.
* **Hypotheses:**
  * $H_0$: The passage of time (Years) has no linear relationship with expanding internal financial gaps.
  * $H_1$: The financial gap scales linearly as time progresses.
* **Results:** Correlation Coefficient ($r$) = **$0.3384$**, **$P\text{-value} = 0.0082$**.
* **Conclusion:** **Reject $H_0$.** This verifies that the socio-economic polarization of football is actively worsening year-over-year. The gap between the richest and poorest clubs continues to widen, emphasizing a structural failure in global sport regulations (such as Financial Fair Play) to halt wealth hyper-concentration.

---

## Phase 2: Machine Learning & Predictive Modeling

To evaluate if financial metrics possess genuine predictive capabilities regarding fan engagement, a comprehensive machine learning architecture was developed.

### 1. Initial Attempt & Paradigm Pivot: Predicting Digital Interest
The initial regression framework utilized internal financial gaps to directly predict global digital interest scores. This attempt yielded universally negative $R^2$ scores across all default configurations, empirically proving that digital media curiosity is highly volatile and driven by external social variables rather than structural wealth metrics alone.

Based on this diagnostic feedback, the target objective was successfully pivoted to predict **Average Stadium Attendance** using two primary features: `Total_Market_Value` and `League_Google_Interest`.

### 2. Model Selection and Split Diagnostics
Three separate algorithms were deployed to model the underlying patterns of the ecosystem:
* **Linear Regression:** Severely underfitted the data, confirming that crowd dynamics do not operate on a simple flat straight-line function.
* **K-Nearest Neighbors (KNN):** Successfully grouped similar localized economic structures.
* **Decision Tree Regressor:** Perfectly captured threshold-based jumps in stadium attendance, achieving an outstanding baseline **$R^2$ Score of 0.8143** on a standard 80/20 evaluation split.

### 3. Rigorous Validation: Shuffled 5-Fold Cross-Validation
To eliminate data selection bias and confirm model stability on our compact macro-dataset (60 consolidated records), a **Shuffled K-Fold Cross-Validation ($k=5$)** was executed. Scrambling the rows ensures that time-series sequencing does not isolate unseen leagues during training.
* **Mean Cross-Validated $R^2$ Score:** **$0.6326$ ($63.26\%$)**
* **Cross-Validation Standard Deviation ($\sigma$):** **$0.1401$**
* **Interpretation:** Achieving a cross-validated predictive baseline of ~63.3% across randomized splits mathematically confirms that our Decision Tree model possesses genuine generalized predictive capacity rather than overfitting to a single train-test partition.

### 4. Interpretability Model: Feature Importance Analysis
Gini importance distributions were extracted from the finalized Decision Tree to isolate the exact decision-making weight of the features when forecasting crowd behaviors:
* **Total Market Value Importance:** **$0.8893$ ($88.93\%$)**
* **Google Search Interest Importance:** **$0.1107$ ($11.07\%$)**

**Discussion:** The feature diagnostics provide a clear socio-economic conclusion: **Total League Wealth is the absolute dominant anchor of physical fan presence.** While online search interest (Google Trends) indicates global curiosity, digital media surfing, and casual entertainment, the commitment of physically buying a matchday ticket and occupying a stadium seat is strictly tied to the financial caliber of the league. High market values yield world-class talent and premium infrastructure, acting as the ultimate engine for stadium crowds.

---

## Final Conclusion & Future Outlook

This project successfully establishes a rigorous data-driven architecture bridging football economics with multi-layered fan sentiment. While my initial childhood intuition suggested that massive financial gaps simply ruin the sport by extinguishing competition, the empirical reality extracted from the data is far more nuanced and complex.

The project mathematically proves that modern football economics are fundamentally polarized: total capital growth actively increases inequality ($r = 0.8434$) and the gap is systematically compounding over time ($r = 0.3384$). However, the core revelation is the **financial polarization paradox**: this concentration of wealth does not drive fans away; instead, it acts as the primary vehicle for physical stadium attendance ($r = 0.6941$) by grouping global superstars into elite flagship clubs. Furthermore, our machine learning pipeline demonstrated that while simple linear approximations fail, non-linear frameworks like **Decision Trees** can leverage these financial and digital footprints to forecast real-world physical attendance metrics with solid accuracy (Cross-Validated $R^2 = 0.6326$, Baseline Split $R^2 = 0.8143$).

### Future Work
Future extensions of this project will look to incorporate real-time sentiment analysis via the X (Twitter) API and live broadcasting viewership revenue data. This will allow us to dissect whether local television audiences and domestic neutral viewers react differently to the death of competitive balance compared to the physical match-going fans who continue to fill hyper-capitalized stadiums.
