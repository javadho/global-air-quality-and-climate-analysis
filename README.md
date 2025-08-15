# Global Air Quality and Climate Analysis

## Project Overview
This project investigates the relationship between global air quality, measured by PM2.5 concentration, and climate variables including temperature, precipitation, and humidity. By integrating datasets from the World Bank, the analysis explores temporal and spatial trends, identifies correlations, and uncovers insights into how climate patterns may influence air quality globally.

## Dataset Description
The final dataset used in this analysis contains:
- **PM2.5 Concentration** (µg/m³) – Annual mean concentration of fine particulate matter with a diameter of 2.5 micrometers or less by country from 1990 to 2020.
- **Air Temperature** (°C) – Country-level average temperature per month from 1990 to 2020.
- **Precipitation** (mm) – Total monthly precipitation per country from 1990 to 2020.
- **Relative Humidity** (%) – Monthly average humidity per country from 1990 to 2020.
- **Year** – Time dimension (spanning multiple decades).

The dataset covers a wide range of countries and years, allowing for both time-series and cross-sectional analysis.

## Data Collection
Two primary data sources were used:
1. **Air Quality Data (PM2.5)** – Sourced from the [World Bank](https://data.worldbank.org/indicator/EN.ATM.PM25.MC.M3), providing annual PM2.5 concentration levels by country.
2. **Climate Data** – Sourced from the [World Bank Climate Knowledge Portal](https://climateknowledgeportal.worldbank.org/download-data), including temperature, precipitation, and humidity statistics.

Data from both sources were downloaded as CSV files and prepared for integration.

## Data Cleaning
The cleaning process involved:
- Converting datasets from **wide format** to **long format** for consistent year-based alignment.
- Converting year columns to integer data types for proper time-series handling.
- Removing missing values for PM2.5 to ensure valid comparisons.
- Standardized climate data by sorting, formatting dates, extracting years, and calculating annual averages per country.
- Merging climate variables with PM2.5 data using country and year as keys to produce a unified dataset.

## Exploratory Data Analysis (EDA)
EDA was performed to identify trends, distributions, and potential relationships:
- **Distribution Analysis** – Histograms and density plots were created for PM2.5, temperature, precipitation, and humidity.

![](https://github.com/javadho/global-air-quality-and-climate-analysis/blob/main/Visualizations/Distribution.png)

- **Central Tendency Measures** – Mean, median, and mode of each variable were calculated to understand typical values.

|        | PM2.5 | Temperature | Humidity | Precipitation |
|--------|-------|-------------|----------|---------------|
| Mean   | 26.78 | 19.34       | 69.46    | 101.03        |
| Median | 27.10 | 19.33       | 69.48    | 101.11        |
| Mode   | 23.53 | 18.75       | 68.67    | 94.48         |

  
- **Time-Series Trends** – Line plots of mean annual PM2.5 and climate variables over decades highlighted temporal shifts.

- **Bivariate Analysis** – Scatter plots examined PM2.5 in relation to each climate variable to identify correlation patterns.

## Visualizations
Key visualizations included:
- **Global Trend Lines** – Showing changes in average PM2.5, temperature, and precipitation over time.
- **Scatter Plots** – PM2.5 vs. temperature, PM2.5 vs. precipitation, PM2.5 vs. humidity, colored by continent.
- **Country-Level Comparisons** – Highlighting nations with extreme PM2.5 values and their corresponding climate conditions.
- **Interactive Bokeh Plots** – Allowing dynamic exploration of relationships across years and countries.

## Insights
1. **Global Decline in PM2.5 in Some Regions** – Developed countries showed gradual improvement in air quality, while some developing nations experienced rising PM2.5 levels.
2. **Temperature Relationship** – Higher temperatures were modestly associated with elevated PM2.5 in certain regions, potentially due to stagnant air conditions.
3. **Precipitation Impact** – Higher rainfall correlated with lower PM2.5 levels, likely due to particulate washout effects.
4. **Humidity Effect** – In humid climates, PM2.5 levels showed mixed trends, suggesting regional factors and pollution sources play a significant role.
5. **Regional Disparities** – Air quality challenges varied greatly between continents, with South and East Asia showing the highest PM2.5 concentrations.

