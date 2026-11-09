The Return to Schooling for Working Married Women, 1975

ECON 3916 · Applied Data Analytics · Midterm Project

Question

Among married white women in the U.S. who worked for pay in 1975, how much higher is the hourly wage associated with one more year of schooling, holding labor-market experience and mother's years of schooling constant?

The outcome is the log hourly wage, so the schooling coefficient reads as a percent difference in wages.

Data source
Dataset: mroz, from the wooldridge Python package (downloaded 2026-10-26).
Original source: Mroz, T. (1987), "The Sensitivity of an Empirical Model of Married Women's Hours of Work to Economic and Statistical Assumptions," Econometrica 55(4): 765–799. The data are drawn from the Panel Study of Income Dynamics (PSID), University of Michigan.
Sample: 753 married white women aged 30–60, observed for calendar year 1975. The regression uses the 428 women who worked for pay, because a wage exists only for women with a job.
Missing data: The wage is missing for the 325 women who did not work. I treat this as a sample-selection problem rather than imputing the missing wages (see Section 1 of the notebook).

The notebook saves a copy of the data to data/mroz.csv the first time it runs and reads that file on later runs.

Repository contents
File	What it is
Midterm Project/Econ_3916_Midterm.ipynb	The full analysis: data, figures, regressions, diagnostics, and the numbers quoted in the report
Midterm Project/ (PDF)	The written report
data/mroz.csv	The dataset as used, saved by the notebook
README.md	This file
How to run it

In Google Colab (recommended)

Open Midterm Project/Econ_3916_Midterm.ipynb from this repository in Colab (File › Open notebook › GitHub).
Choose Runtime › Run all.

The first cell installs the wooldridge package, so nothing else needs to be set up. The whole notebook runs in under a minute.

Locally

bash
pip install wooldridge numpy pandas matplotlib statsmodels scipy jupyter
jupyter notebook "Midterm Project/Econ_3916_Midterm.ipynb"

Then run all cells from top to bottom. Every number quoted in the report is printed by the final Numbers my report quotes cell.

Headline finding

Among married white women who worked in 1975, one more year of schooling is associated with about 12.5% higher hourly wages, holding mother's schooling and work experience constant (OLS with robust standard errors; the 95% confidence interval lies well above zero). Four extra years of schooling, roughly a college degree compared with a high-school diploma, is associated with about 60% higher wages.

The estimate barely changes when work experience is left out, when the number of young children is added, or when influential observations are dropped.

This is a conditional association, not a causal effect. Women with more schooling may also have more ability or motivation, which would push the estimate up. Because wages are observed only for women who chose to work, selection into employment could bias the estimate in either direction. The result describes working married women in 1975, not all married women.
