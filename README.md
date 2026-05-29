# Socioeconomic Determinants of Adolescent Pregnancy in Ecuador: A Cantonal-Level Econometric Analysis Using 2022 Census Microdata

## Project Overview
This repository contains an empirical analysis of the structural drivers of adolescent pregnancy across the 221 cantons of Ecuador. Utilizing aggregated cantonal indicators constructed from individual-level microdata from the **2022 Census (INEC)**, this study evaluates the marginal effects of geographic rurality, educational attainment, structural poverty (NBI), ethnic composition, and demographic pressure on youth populations. 

The objective is to provide a reproducible, statistically rigorous pipeline that translates raw national census microdata into actionable policy insights regarding reproductive health and regional socioeconomic disparities in Ecuador.

## Methodology & Model Specification
To estimate the relationship between socioeconomic indicators and adolescent fertility, we implement a multivariate Ordinary Least Squares (OLS) framework with **Heteroskedasticity-Robust Standard Errors (HC3)** to account for spatial variances and population-size differentials across cantons.

The baseline cross-sectional econometric specification is defined as follows:

$$\text{AdolescentPregnancy}_c = \beta_0 + \beta_1 \text{Rurality}_c + \beta_2 \text{Education}_c + \beta_3 \text{YouthDensity}_c + \beta_4 \text{PovertyNBI}_c + \beta_5 \text{Indigenous}_c + \varepsilon_c$$

Where for each canton $c$:
* `AdolescentPregnancy`: The percentage of women aged 12–19 who have had at least one child.
* `Rurality`: The proportion of the cantonal population residing in designated rural sectors.
* `Education`: The average years of formal schooling completed by the population aged 15 and older.
* `YouthDensity`: The ratio of the population aged 15–29 relative to the canton's total geographic area.
* `PovertyNBI`: The percentage of the population living with Unmet Basic Needs (Necesidades Básicas Insatisfechas).
* `Indigenous`: The percentage of the population self-identifying as Indigenous.
* `Error Term (ε)`: The stochastic error term.

## Repository Structure

```text
├── data/              # Cleaned cantonal-level CSV data files
├── notebooks/         # Documented Colab notebooks for ETL and estimation
└── README.md          # Project documentation and research overview
```

## Setup and Reproducibility
To replicate the environment and rerun the econometric models:

1. Clone this repository:
```bash
git clone [https://github.com/ignaciogaytan2030/ecuador-adolescent-pregnancy-econometrics.git](https://github.com/ignaciogaytan2030/ecuador-adolescent-pregnancy-econometrics.git)
```

2. Run the notebooks inside the `notebooks/` directory sequentially using Google Colab or a local Jupyter environment.
