# Do Women's FIFA World Cup Matches Have More Goals Than Men's?

## Project Overview
This project investigates whether more goals are scored in **women's** FIFA World Cup matches compared to **men's**. Using official match results since 2002, we perform statistical hypothesis testing to validate or refute this claim.

## Dataset
Two datasets were scraped from a reliable online source:
- **`women_results.csv`**: Results of all international women's matches.
- **`men_results.csv`**: Results of all international men's matches.

For this study, we **only** consider matches from the **FIFA World Cup (excluding qualifiers)** since **January 1, 2002**.

### Key Variables:
- `date`: Match date.
- `tournament`: Type of competition.
- `home_score`, `away_score`: Goals scored by each team.
- `goals_scored`: Total goals per match (`home_score + away_score`).

## Hypothesis Testing
We assume a **10% significance level (α = 0.10)** and define:

- **Null Hypothesis (H₀)**: The mean number of goals in women's and men's FIFA World Cup matches is the same.
- **Alternative Hypothesis (H₁)**: The mean number of goals in women's FIFA World Cup matches is higher than in men's.

### Statistical Tests:
1. **Normality Tests**:  
   - Shapiro-Wilk Test  
   - Anderson-Darling Test  
   - KDE plots & Q-Q plots  
2. **Wilcoxon-Mann-Whitney Test** (non-parametric test for comparing two independent groups).  

## Results
- **P-value from Wilcoxon-Mann-Whitney test**: `wmw_test['p-val']`
- A significant p-value **rejects H₀** in favor of **H₁**, suggesting more goals in women's FIFA World Cup matches.

## How to Run
```bash
pip install pandas numpy pingouin seaborn matplotlib scipy statsmodels
python soccer_goals_analysis.py
