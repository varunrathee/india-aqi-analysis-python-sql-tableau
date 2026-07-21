# Indian Air Quality (AQI) Analysis — Python + SQL + Tableau

Analysis of air quality trends across 26 Indian cities (2015–2020) using
real CPCB government data — covering city rankings, seasonal pollution
patterns, and pollutant breakdowns.

## Live Dashboard
[View on Tableau Public](https://public.tableau.com/views/AQIDashboard_17846599713060/AQIDashboard?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))

## Data Source
Kaggle: Air Quality Data in India (2015–2020) — CPCB city-level daily records

## Process
- Cleaned data in Python (pandas) — handled missing pollutant values with
  city-level median imputation, dropped rows with missing AQI, engineered
  Year/Month columns
- Loaded cleaned data into SQLite and queried city-level average AQI rankings
- Built an 8-sheet interactive Tableau dashboard for the full analysis,
  including seasonal trends, a geographic map, and pollutant breakdowns

## Dashboard Features
- KPI cards: Overall avg AQI, worst city, best city
- India map color-coded by average AQI severity
- Seasonal trend line comparing Delhi vs Bengaluru across all 12 months
- City × Month heatmap showing pollution patterns across top cities
- AQI severity bucket distribution (Good → Severe)
- Pollutant breakdown (PM10, PM2.5, NO2, CO, SO2, O3)

## Key Insights
- Overall average AQI across all cities: 166.5
- Ahmedabad was the most polluted city (avg AQI: 452.1); Aizawl the cleanest (34.77)
- Delhi's AQI spikes sharply in winter months (Nov–Jan), while Bengaluru
  stays comparatively flat year-round
- PM10 and PM2.5 are the dominant pollutants by a wide margin over CO, SO2, and O3

## Files
- `aqi_cleaning_and_analysis.ipynb` — Python cleaning and city-level SQL
  ranking query. (Seasonal and pollutant-correlation analysis was done
  directly in Tableau using the same cleaned dataset.)

## Tools
Python (pandas), SQL (SQLite), Tableau
