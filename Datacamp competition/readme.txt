# Predicting Industrial Machine Downtime: Level 2

## Executive Summary

This project explores patterns in machine downtime using operational data. The key objectives include:
1. Performing Exploratory Data Analysis (EDA) to understand the dataset.
2. Investigating correlations between different machine parameters.
3. Identifying trends in machine failures over time.
4. Providing final recommendations based on the findings.

---

## 💪 Competition Challenge

The competition requires a report that addresses the following:
- Identifying correlations between various operational data points.
- Examining machine downtime patterns over time.
- Determining which factors are visually associated with machine downtime.

---

## 🔍 Exploratory Data Analysis (EDA)

### Data Overview & Preprocessing
- Loaded and explored `machine_downtime.csv`.
- Checked data types and converted `Date` to datetime format.
- Handled missing values (dropped rows with <5% missing data).
- Examined failure machine distributions.

### Statistical Analysis & Visualization
- Summary statistics of numerical variables.
- Distribution plots for all numerical features.
- Boxplots to detect outliers before and after normalization.
- Pair plots to examine relationships between variables.
- Correlation heatmap to analyze feature dependencies.

**Findings:**
- No strong correlation among variables, indicating low multicollinearity.
- The highest correlations appear between **Cutting (KN), Torque (Nm), and Spindle Speed (RPM)**, but they remain weak.

---

## 📈 Patterns in Machine Downtime Over Time

- **Rolling averages of machine failures over time** suggest a rise from Feb 2022 to mid-March 2022, followed by a decline.
- No clear pattern detected in **failures by day, week, or month**.
- Potential external factors (e.g., increased number of machines or maintenance changes) might explain variations.

---

## 📊 Factors Connected to Machine Downtime

- **Feature Averages by Downtime Type**: Failure-prone machines exhibit higher **Spindle Speed (RPM)** and lower **Hydraulic Pressure**.
- **Machine Type & Failures**: No specific machine type shows a higher failure rate.
- **Correlation Matrix**: Weak correlations between features and downtime.
- **Boxplots & Histograms**: Certain feature ranges are associated with higher failure rates.

---

## ✅ Final Recommendations

To reduce machine failures, avoid operating within the following critical ranges:
- **Coolant Pressure (bar)**: 4-5 and above 7.
- **Coolant Temperature**: 11-19 and above 30.
- **Cutting (kN)**: 2.25-2.5 and above 3.5.
- **Hydraulic Pressure (bar)**: Below 90.
- **Spindle Speed (RPM)**: Above 25k.
- **Torque (Nm)**: 25-30 and below 18.

These insights can guide preventive maintenance strategies to minimize downtime and optimize machine performance.

---

## 🚀 Future Improvements

- Implement machine learning models to predict failures.
- Collect more granular operational data to enhance analysis.
- Explore external factors affecting machine failures (e.g., operator shifts, environmental conditions).

---

**📌 Author:** [Your Name]  
**📌 Repository:** [GitHub Link]  
**📌 Date:** March 2025

