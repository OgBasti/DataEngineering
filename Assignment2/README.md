# Assignment 1 – COVID-19 Data Analysis with Pandas

This repository presents data analysis of real-world COVID-19 daily report data using Python and Pandas, with a focus on answering structured analytical questions from a provided dataset.

## Overview

- **Goal:** Explore, clean, process, and analyze COVID-19 data to extract insights and answer 13 data analysis questions.
- **Assignment Context:** Structured questions drive analysis, covering data exploration, descriptive statistics, feature engineering, and calculated metrics.

## Main Data Features

| Feature              | Description                                                         |
|----------------------|---------------------------------------------------------------------|
| FIPS                 | US-only, Federal county code                                        |
| Admin2               | US county name                                                      |
| Province_State       | Province, state, or dependency name                                 |
| Country_Region       | Country, region, or sovereignty name                                |
| Last_Update          | Timestamp of the report (UTC)                                       |
| Lat, Long            | Geographic coordinates                                              |
| Confirmed            | Total confirmed COVID-19 cases                                      |
| Deaths               | Total deaths due to COVID-19                                        |
| Recovered            | Reported recovered cases                                            |
| Active               | Active case estimate                                                |
| Incident_Rate        | Cases per 100,000 persons                                           |
| Case_Fatality_Ratio  | 100 × Deaths / Confirmed Cases (%)                                 |
| Combined_Key         | Combination of geographic fields for unique location identification |

*(For full descriptions, see notebook and CSSE COVID-19 Data Repository.)*

## Workflow

- Load and inspect the dataset.
- Perform exploratory data analysis (EDA).
- Calculate descriptive statistics.
- Engineer and validate features (e.g., fatality rates).
- Address 13 assignment questions with analytical code and results documented in Jupyter.

## Data Source

Data adapted from the [CSSEGISandData/COVID-19] project by Johns Hopkins University (JHU).

- Dong E, Du H, Gardner L. (2020). An interactive web-based dashboard to track COVID-19 in real time. *Lancet Inf Dis*, 20(5):533-534. doi: 10.1016/S1473-3099(20)30120-1

## Results

- The notebook provides code, narrative, and results for each question, using tables, calculations, and basic visualizations where relevant.

---

_See the notebook for all code, results, and detailed explanations._



