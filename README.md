# Urban Traffic Crash Analysis: Patterns of Risk and Injury

**Project Level** Intermediate to Advanced 

# Overview

This project is an in-depth Exploratory Data Analysis (EDA) focused on identifying critical patterns and risk factors associated with urban traffic crashes. The analysis involves significant data cleaning, feature transformation, and temporal and categorical investigation using the powerful Pandas library in Python.

The primary goal is to transform raw crash data into clear, actionable insights, highlighting trends related to accident timing, weather, injury severity, and police response times.

## Data Origin and Scope

The dataset is provided by the City of Chicago and encompasses detailed reports on traffic accidents occurring within the city limits. The data is managed by the Chicago Police Department and is made publicly available through the City of Chicago's Data Portal. Understanding the specific geographic context of Chicago is crucial for interpreting the trends identified in the analysis.

## Project Breakdown

The analysis was executed within a structured Jupyter Notebook workflow, divided into the following key phases:

### 1. Data Cleaning and Preprocessing

The raw dataset required extensive preparation to standardize formats and handle missing values:
* **Standardization**: All column names were lowercased, and string-type row values were converted to lowercase for consistency.
* **Irrelevant Column Removal**: Columns like crash_record_id and crash_date_est_i were dropped as they were either redundant or uninformative for the analysis scope.
* **Categorical Mapping**: Values in columns like road_defect were consolidated (e.g., replacing 'unknown' with 'other'). Complex primary contributory causes were grouped for simplified analysis.
* **Data Type Conversion**: The crash_date and date_police_notified columns were converted to the datetime format to enable temporal calculations.
* **Duplication Handling**: Duplicate rows were identified and removed to ensure data integrity.

### 2. Exploratory Data Analysis (EDA)

The core analysis focused on revealing key accident trends:
* **Temporal Analysis**: Identified the most dangerous hours of the day for incidents (using crash_hour). Calculated incident frequency across the days of the week. Determined the number of cases where police notification was significantly delayed (over 3 days) from the crash date.
* **Injury and Environment Factors**: Aggregated the data to find the maximum number of injuries recorded under different weather_condition categories.
* **Causation and Damage Correlation**: Analyzed the most common damage value (e.g., $500 or less, over $1,500) associated with each prim_contributory_cause.
* **Missing Data Assessment**: Calculated the percentage of missing values across all columns to evaluate data completeness.

## Data Source

The project uses public traffic crash data sourced from the City of Chicago.

Dataset Name: Traffic_Crashes_-_Crashes.csv
Source URL: https://catalog.data.gov/dataset/traffic-crashes-crashes

## Key Findings

The EDA provided several critical insights into traffic safety and reporting in Chicago:
* **Peak Crash Times**: The highest volume of crashes occurs during the afternoon rush hour, specifically 3 PM (15), 4 PM (16), and 5 PM (17), indicating peak congestion as a major contributing factor.
* **Weekend High Volume**: Contrary to typical weekday commutes, Saturday and Sunday recorded the highest number of total incidents, suggesting elevated risk during leisure travel periods.
* **Injury in Clear Weather**: While severe conditions are dangerous, the highest overall injury counts (21 total injuries) were recorded during clear and rainy weather.
* **Damage Severity**: For nearly every major primary contributory cause, the most frequent reported outcome was the highest damage category, "over $1,500", underscoring the high cost associated with these incidents.
* **Delayed Reporting**: A substantial number of incidents (42,641) showed a delay of over 3 days between the crash and the police being notified, revealing a potential systemic issue in accident reporting compliance or data entry lag.
