# SIADS 593 Team Project: Exploring the Impact of Air Quality on Respiratory Health Outcomes

## Project Overview
This project investigates how air pollution—specifically levels of PM2.5 and Ozone—is associated with respiratory health outcomes across different regions in the United States. We aim to integrate environmental and public health data to explore spatial patterns and correlations.

## Data Sources

### 1. Behavioral Risk Factor Surveillance System (BRFSS) - 2023
- Source: [CDC BRFSS](https://www.cdc.gov/brfss/annual_data/annual_data.htm)
- Format: Fixed-width ASCII (.ASC), converted to CSV
- Key Features: Health responses including asthma prevalence, demographics, and location data
- Key Column: `_STATE` (mapped to full state name)

### 2. EPA Air Quality System (AQS) - 2023
- Files used:
  - `annual_conc_by_monitor_2023.csv` – Contains pollutant levels by monitoring station
  - `aqs_sites.csv` – Metadata for monitoring site locations
- Pollutants of Interest:
  - PM2.5 - Local Conditions
  - Ozone
- Key Columns: `State Code`, `County Code`, `Site Num`, `Parameter Name`, `Arithmetic Mean`

## 🔄 Data Integration

1. **Convert fixed-width BRFSS ASCII data** to CSV using column specifications from the CDC-provided layout and codebook.
2. **Decode categorical variables** using SAS `FORMAT23.sas` mappings.
3. **Join AQS pollutant data** with monitoring site metadata to extract `State Name` and `County Name`.
4. **Aggregate pollutant data** by state and county.
5. **Merge BRFSS and AQS data** on `State Name` to begin initial analysis (next step: improve precision using county-level identifiers).

## Next Steps
- Enhance BRFSS records with county-level location data if available.
- Conduct statistical analysis to explore correlations between air quality and asthma prevalence.
- Generate maps and visualizations to illustrate geographic disparities.

## Tools Used
- Python (Pandas, regex, Altair, PyPlot, Folium)
- EPA AirData and CDC BRFSS public data
- Jupyter Notebook environment 

## Team Members
- 