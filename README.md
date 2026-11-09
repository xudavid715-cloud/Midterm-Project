# Midterm-Project
# ECON 3916 Midterm Project: Education and Wages

## Research Question
This project examines the relationship between education and hourly wages among married white women who worked in the United States in 1975.

Specifically, it investigates how one additional year of schooling is associated with hourly wages, controlling for work experience, children under six, and mother's education.

## Data Source
The dataset comes from the Panel Study of Income Dynamics (PSID), originally analyzed by Mroz (1987).

- Dataset: `mroz`
- Source: Wooldridge Python Package
- Original observations: 753
- Regression observations: 428

Source: https://pypi.org/project/wooldridge/

## Methodology
The analysis uses:
- Descriptive statistics and visualizations.
- OLS regression with HC1 robust standard errors.
- Residual analysis and Breusch–Pagan testing.
- VIF and Cook's distance diagnostics.

## Main Finding
One additional year of schooling is associated with approximately **12.6% higher hourly wages**, holding other factors constant.

This is a conditional association, not necessarily a causal effect, due to potential omitted variable bias and selection into employment.

## How to Run
1. Open `Econ_3916_Midterm.ipynb` in Google Colab or Jupyter Notebook.
2. Install the required packages using the notebook's setup cell.
3. Ensure `data/mroz.csv` is available, or allow the notebook to download it.
4. Run all cells from beginning to end.

## References
Mroz, T. A. (1987). *Econometrica*, 55(4), 765–799.

Wooldridge Python Package: https://pypi.org/project/wooldridge/
