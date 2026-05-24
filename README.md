This README file describes the subset of the COVID-19 dataset that focuses on the United States. The dataset is provided by Our World in Data and includes both original and derived features. The dataset has been curated by Bryan Tuck for in-depth analysis of the pandemic's impact within the United States.

This README is intended to provide a comprehensive understanding of the subset and its variables for anyone using it for analysis, modeling, or educational purposes.

## Dataset Overview:
This subset of the COVID-19 dataset reflects the situation in the United States, providing detailed data on cases, deaths, hospitalizations, and other metrics relevant to the pandemic. Our World in Data has compiled this information, drawing from official sources and making it accessible for public analysis. The dataset is part of a larger collection that tracks the global impact of the COVID-19 pandemic, with daily updates throughout its duration.

## Original Variables:
+ date: The date when the data was recorded.
+ total_cases: Total confirmed cases of COVID-19.
+ new_cases: New confirmed cases of COVID-19 on the given date.
+ total_deaths: Total deaths attributed to COVID-19.
+ new_deaths: New deaths attributed to COVID-19 on the given date.
+ total_cases_per_million: Total confirmed cases of COVID-19 per 1,000,000 people.
+ total_deaths_per_million: Total deaths attributed to COVID-19 per 1,000,000 people.
+ icu_patients: Number of COVID-19 patients in intensive care units (ICUs) on the given date.
+ hosp_patients: Number of COVID-19 patients in the hospital on the given date.
+ weekly_hosp_admissions: Number of COVID-19 patients newly admitted to hospitals in the given week.
### Derived Features:
+ daily_case_change_rate: The percentage change in new cases compared to the total cases on the previous day.
+ daily_death_change_rate: The percentage change in new deaths compared to the total deaths on the previous day.
+ hospitalization_rate: The percentage of total COVID-19 cases that resulted in hospitalization on the given date.
+ icu_rate: The percentage of total COVID-19 cases that required intensive care on the given date.
+ case_fatality_rate: The percentage of total COVID-19 cases that resulted in death.
+ 7day_avg_new_cases: The 7-day rolling average of new COVID-19 cases.
+ 7day_avg_new_deaths: The 7-day rolling average of new COVID-19 deaths.
+ hospitalization_need: Categorical assessment of hospitalization rates as 'Low', 'Medium', or 'High' based on quantile distribution.
+ icu_requirement: Categorical assessment of ICU rates as 'Low', 'Medium', or 'High' based on quantile distribution.

The derived categorical assessments ('hospitalization_need' and 'icu_requirement') are relative to the dataset and are based on the distribution of the data within the United States. These labels are intended to facilitate the analysis and may not represent absolute thresholds for public health action.

The subset presented here includes only the most pertinent variables for a focused analysis on the United States, allowing for a clear understanding of the trends and patterns specific to the U.S. during the COVID-19 pandemic.

## Data Preprocessing:
+ The 'date' column has been converted to a datetime object to facilitate time series analysis.
+ Quantile-based discretization function (pd.cut) has been used to convert continuous variables into categorical variables for 'hospitalization_need' and 'icu_requirement'.
+ Rolling window functions have been used to calculate 7-day averages for new cases and deaths.
