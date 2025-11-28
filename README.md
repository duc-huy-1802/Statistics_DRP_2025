# 📊 Statistics DRP 2025 — Unemployment Modeling & Economic Indicator Analysis

This project explores the relationship between U.S. unemployment, natural unemployment, and a series of macroeconomic and labor-market indicators.
It was developed as part of the University of Washington Statistics Directed Reading Program (Winter 2025).

The goal is to build statistical and machine-learning models that can:
* Analyze the relationship between unemployment and driving economic factors
* Predict when unemployment rises above its natural rate
* Compare model performance across Logistic Regression, SVMs, Random Forests, Ridge, and Lasso

## 📁 Project Structure

```
Statistics_DRP_2025/
├── stats_drp_project/
│   ├── Data/                  # Raw macroeconomic & labor datasets
│   ├── Visualizations/        # EDA and Model Visualizations
│   └── stats_drp_project.ipynb   # Main notebook for EDA & modeling
└── README.md                  # Project overview
```

## 📈 Variables Used in This Project

Below is a full list of the predictor variables and target variables used in the analysis, including descriptions and data sources.

| Name                              | Description                                              | Source                            | FRED Series      | Link                                               | Other Notes                                  |
|-----------------------------------|----------------------------------------------------------|-----------------------------------|------------------|----------------------------------------------------|----------------------------------------------|
| monthly_assault                   | Monthly national assault counts                          | Federal Bureau of Investigation   | —                | —                                                  | Retrieved from FBI explorer page             |
| monthly_bonds                     | 10-Year Treasury Constant Maturity Rate (monthly)        | U.S. Treasury / FRED              | DGS10            | https://fred.stlouisfed.org/series/DGS10           | Long-term interest rate                      |
| monthly_consumer_confidence       | Consumer Confidence Index (monthly)                      | The Conference Board / FRED       | CSCICP03USM665S  | https://fred.stlouisfed.org/series/CSCICP03USM665S | Not being used because of limited time frame |
| monthly_continuing_jobless_claims | Ongoing unemployment insurance claims (monthly)          | U.S. Department of Labor          | CCSA             | https://fred.stlouisfed.org/series/CCSA            | Converted from weekly to monthly             |
| monthly_cpi                       | Consumer Price Index (CPI)                               | Bureau of Labor Statistics (BLS)  | CPIAUCSL         | https://fred.stlouisfed.org/series/CPIAUCSL        | Used to compute inflation                    |
| monthly_federal_funds_rate        | Federal Funds Effective Rate (Fed Funds Rate)            | Federal Reserve                   | FEDFUNDS         | https://fred.stlouisfed.org/series/FEDFUNDS        | Monetary policy short-term rate              |
| monthly_inflation_rate            | Monthly inflation rate                                   | Derived from CPI data             | —                | —                                                  | Computed manually from monthly CPI           |
| monthly_job_postings              | Job openings / postings index (monthly)                  | BLS JOLTS or Indeed Hiring Lab    | JTSJOL (typical) | https://fred.stlouisfed.org/series/JTSJOL          | Based on available postings dataset          |
| monthly_job_quit                  | Monthly quits (voluntary separations)                    | BLS JOLTS                         | JTSQUL           | https://fred.stlouisfed.org/series/JTSQUL          | Indicator of labor market tightness          |
| monthly_jobless_claims            | Initial unemployment insurance claims (monthly)          | U.S. Department of Labor          | ICSA             | https://fred.stlouisfed.org/series/ICSA            | Aggregated from weekly data                  |
| monthly_labor                     | Total nonfarm U.S workers                                | Bureau of Labor Statistics (BLS)  | PAYEM            | https://fred.stlouisfed.org/series/CES0500000003   | Wage indicator                               |
| monthly_sp500                     | S&P 500 index level through the SPY ETF returns          | Yahoo Finance                     |                  | https://finance.yahoo.com/quote/SPY/               | Market sentiment indicator                   |
| monthly_unemployment_rate         | U.S. unemployment rate (monthly)                         | Bureau of Labor Statistics (BLS)  | UNRATE           | https://fred.stlouisfed.org/series/UNRATE          | Core unemployment metric                     |
| quarterly_gdp                     | U.S. Gross Domestic Product (quarterly)                  | Bureau of Economic Analysis (BEA) | GDP              | https://fred.stlouisfed.org/series/GDP             | Interpolated to monthly                      |
| quarterly_natural_unemp           | Natural unemployment rate (quarterly, CBO estimate NROU) | Congressional Budget Office (CBO) | NROU             | https://fred.stlouisfed.org/series/NROU            | Interpolated to monthly                      |


