Data compiled from the HK Transport Department's monthly vehicle registration records, sourced via the community-maintained Webb-Database mirror (the open-source continuation of the legacy Webb-site database).


Hong Kong EV Adoption Analysis & Forecasting Dashboard

An end-to-end data analysis, forecasting, and visualization project tracking the trajectory of Electric Vehicle (EV) adoption in Hong Kong. This project cleans raw registration data, uses time-series forecasting in Python to predict future trends, and visualizes the insights in an interactive Google Sheets executive dashboard.

---
Dashboard Access & Previews

*   **Interactive Dashboard:** [Access Google Sheets Dashboard](https://docs.google.com/spreadsheets/d/12CoKswkyZ6Zl-4paeVbr6ws6ZkYlynNHEJ6Jtqm7Wdw/edit?usp=sharing) *(View Only)*
*   **Static Backup:** If you prefer offline access, the Excel version of the dashboard is available as a file in this repository.

> **Dashboard Preview:**
<img width="1298" height="705" alt="image" src="https://github.com/user-attachments/assets/a44e48c0-c814-490f-9c61-55ee737ec8e9" />

---

## Project Overview & Workflow

The goal of this project is to analyze historical trends of EV registrations in HK and forecast market penetration over the next few years. The workflow is divided into three major stages:

### 1. Data Sourcing & Cleaning
*   **Data Origin:** Raw monthly vehicle registration records compiled from the Hong Kong Transport Department.
*   **Data Source:** Sourced via the community-maintained [Webb-Database mirror](https://webb-database.com/) (the open-source continuation of the legacy Webb-site database).
*   **Python Processing:** Using `pandas`, the data was cleaned and registrations were aggregated chronologically to establish a clean time-series baseline.

### 2. Modeling & Forecasting (Python)
*   I developed a forecasting script in Python ('HK_EV_adoption.ipynb').
*   **Model Used:** Polynomial Regression (Degree 2) via scikit-learn. The model fits a quadratic curve to historical EV market share trends to capture the accelerating pace of adoption.
*   The script outputs a predictive DataFrame (`forecast_df`) projecting EV registration counts and adoption rates through 2030.

### 3. Google Sheets Dashboard Design
The clean historical data and the forecasted predictions were imported into Google Sheets to build a dashboard featuring:
*   **KPI Scorecards:** Total active EVs, current market share, and 5-year growth rate.
*   **Charts:** Historical growth curves mapped directly alongside future forecasted trends.
