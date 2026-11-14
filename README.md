# Boston Uber & Lyft Ride-Sharing: EDA & SQL Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/13VqfqDeOvkZGWZX81bj1MVWyB8-6rH_6?usp=sharing)

## Project Overview
This repository contains an end-to-end Exploratory Data Analysis (EDA) and relational database querying project analyzing ride-sharing metrics for Uber and Lyft in Boston. Using Python, Pandas, Seaborn, and SQLite, the project investigates ride pricing dynamics, service tier stratification, temporal demand patterns, and surge pricing behaviors.

## Dataset
* **Source:** Kaggle (Boston Cab Rides dataset)
* **Scale:** ~637k cleaned ride transactions after handling missing values and data hygiene.
* **Key Features:** Price, distance, surge multipliers, cab providers, specific vehicle service tiers, timestamps, and route source/destination pairs.

## Technical Stack & Tools
* **Language:** Python
* **Data Processing & Manipulation:** Pandas, NumPy
* **Data Visualization:** Seaborn, Matplotlib
* **Database & Querying:** SQLite (in-memory integration via Python)
* **Environment:** Google Colab

---

## Key Analysis & Workflow
1. **Data Cleaning & Preprocessing:** 
   * Handled missing value imputation and dropped null fare anomalies.
   * Converted Unix epoch timestamps into human-readable datetime objects, extracting hourly and day-of-week attributes.
2. **Univariate Distributions:** 
   * Examined right-skewed price distributions and short-distance urban commute frequencies.
3. **Bivariate & Multivariate Relationships:** 
   * Explored price vs. distance scaling across providers, uncovering that fares are heavily stratified by vehicle tier rather than mileage alone.
   * Analyzed price spread and outliers across standard economy vs. luxury tiers using boxplots.
4. **Temporal & Surge Trends:** 
   * Mapped hourly ride volume fluctuations to identify urban mobility and commuter patterns.
   * Analyzed surge multiplier frequencies across service classes.
5. **SQL-Based Insights:** 
   * Loaded the cleaned dataset into an in-memory SQLite database (`:memory:`) to execute relational aggregations, compute average pricing by tier, identify top high-cost routes, and calculate surge percentages.

---

## Key Business Insights
* **Vehicle Tier Stratification:** Fare pricing is primarily driven by vehicle tier (e.g., standard economy vs. luxury black cars) rather than raw trip distance. Short luxury rides command significantly higher baseline minimums than long economy trips.
* **Competitive Parity:** Both Uber and Lyft maintain highly aligned pricing envelopes and geographic distributions across the Boston metropolitan market.
* **Peak Demand Cycles:** Ride volumes shift dynamically by the hour of the day, reflecting traditional commuter rhythms and evening mobility habits.

## How to View and Run
You can inspect the full code, interactive visualizations, and SQL queries directly in your browser via Google Colab:
👉 [Open Notebook in Google Colab](https://colab.research.google.com/drive/13VqfqDeOvkZGWZX81bj1MVWyB8-6rH_6?usp=sharing)
[![View Dashboard](https://img.shields.io/badge/Tableau-Interactive%20Dashboard-orange)](https://public.tableau.com/views/BostonUberandLyftMarketIntelligenceDashboard/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
