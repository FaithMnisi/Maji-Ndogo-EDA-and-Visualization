# Maji Ndogo: Agricultural Data Exploration and Weather Data Validation

## Project Overview

This project explores agricultural and environmental data from the fictional country of Maji Ndogo to identify patterns that may influence crop production.

Using Python, SQL and exploratory data analysis (EDA), I investigated relationships between rainfall, temperature, soil characteristics, pollution levels and crop yields across five rural regions.

The project also examines data reliability by extracting measurements from unstructured weather-station messages and comparing them against farm-level weather measurements.

## Objectives

- Explore agricultural and environmental data across five regions.
- Investigate relationships between environmental conditions and crop yields.
- Examine regional differences in rainfall and crop distribution.
- Identify patterns and anomalies using statistical analysis and visualisation.
- Extract structured measurements from unstructured weather-station messages.
- Validate farm-level weather measurements against independent weather-station data.

## Tools and Technologies

| Tool / Technology | Application |
|---|---|
| Python | Data analysis, cleaning and transformation |
| Pandas | Data manipulation and statistical analysis |
| SQL / SQLite | Querying and joining relational datasets |
| Matplotlib | Data visualisation |
| Seaborn | Exploratory and statistical visualisation |
| Regular Expressions (RegEx) | Extracting measurements from unstructured text |

## Dataset Overview

The agricultural dataset consisted of four related tables:

- Geographic features
- Weather features
- Soil and crop features
- Farm management features

The tables were joined using `Field_ID`, producing an analytical dataset containing **5,654 records and 18 columns**.

The project also used **1,843 weather-station messages** collected from five stations. These messages contained temperature, rainfall and pollution measurements embedded in text.

## Methodology

### 1. Data Preparation and Cleaning

- Joined the four agricultural tables using SQL.
- Standardised inconsistent crop labels and removed trailing whitespace.
- Corrected negative elevation values.
- Inspected data types, descriptive statistics and missing values.
- Prepared the combined dataset for exploratory analysis.

### 2. Exploratory Data Analysis

Used Pandas, Matplotlib and Seaborn to investigate:

- Regional rainfall distributions and averages.
- Crop distribution across the five regions.
- Relationships between environmental variables and crop yields.
- Coffee yield relationships with rainfall, soil fertility and pollution.

### 3. Weather Data Extraction

Processed 1,843 weather-station messages using regular expressions to extract:

- Temperature
- Rainfall
- Pollution levels

The extracted measurements were converted into structured data and grouped by weather-station ID.

### 4. Weather Data Validation

Matched farm records to their nearest weather stations and compared average measurements from both datasets.

A **1.5% tolerance** was used to assess agreement between the corresponding measurements.

## Key Findings

### Regional Rainfall Differences

Average rainfall varied considerably across the five regions.

| Region | Average Rainfall (mm) |
|---|---:|
| Rural Sokoto | 1,705.08 |
| Rural Akatsi | 1,584.88 |
| Rural Hawassa | 1,325.94 |
| Rural Kilimani | 791.35 |
| Rural Amanzi | 723.63 |

The difference between the highest and lowest regional averages was approximately **981.45 mm**.

### Crop Distribution

Crop distribution differed across regions. In Rural Amanzi, the three most frequently represented crop types included:

| Crop | Number of Fields |
|---|---:|
| Potatoes | 98 |
| Wheat | 69 |
| Maize | 61 |

These findings highlighted differences in agricultural patterns across regions with varying rainfall conditions.

### Environmental Relationships and Coffee Yields

Correlation analysis identified:

- A negative correlation between pollution and standardised yield (**r = -0.286**).
- A negative correlation between soil pH and standardised yield (**r = -0.197**).
- Positive relationships between coffee yields, rainfall and soil fertility.
- A negative relationship between coffee yields and pollution.

These findings represent observed associations rather than evidence of causation.

### Weather Data Validation Results

A total of 15 comparisons were performed across five weather stations.

| Measurement | Within Tolerance | Outside Tolerance |
|---|---:|---:|
| Temperature | 5/5 | 0/5 |
| Rainfall | 1/5 | 4/5 |
| Pollution
