# Hypothesis Testing in Healthcare: Drug Safety

## Project Overview
This project analyzes the safety of a new drug by conducting statistical hypothesis tests on a clinical trial dataset. The dataset contains demographic information, treatment groups, and adverse effects.

## Dataset
The dataset `drug_safety.csv` was sourced from [Hbiostat](https://hbiostat.org/data/) and modified to include:
- `trx`: Treatment group (Drug or Placebo)
- `adverse_effects`: Presence of at least one adverse effect (Yes/No)
- `num_effects`: Number of adverse effects per individual
- `age`, `sex`, `wbc`, `rbc`: Additional clinical attributes

## Hypotheses Tested
1. **Proportion of adverse effects**: Is there a significant difference between the Drug and Placebo groups? (Z-test)
2. **Number of adverse effects**: Is it independent of treatment type? (Chi-square test)
3. **Age distribution**: Does it differ significantly between the groups? (Mann-Whitney U test)

## Results
- **Adverse Effects Proportion (Z-test)**: p-value = `two_sample_p_value`
- **Adverse Effects Independence (Chi-Square test)**: p-value = `num_effects_p_value`
- **Age Group Comparison (Mann-Whitney U test)**: p-value = `age_group_effects_p_value`

## How to Run
```bash
pip install numpy pandas statsmodels scipy seaborn pingouin matplotlib
python hypothesis_testing.py
