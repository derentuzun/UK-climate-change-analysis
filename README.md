# UK Climate Change Analysis

Statistical investigation of climate change evidence across 37 UK Met Office
weather stations using regression modelling, bootstrap inference, and hypothesis testing.

## Overview

This project analyses long-term weather patterns in the UK to answer:
- Is the maximum temperature increasing over time, and at what rate?
- Has the number of frost days changed significantly across decades?
- Do these patterns vary by region?

## Methods

- **Sinusoidal linear regression** to model seasonal temperature cycles and extract long-term warming trends
- **Residual bootstrap** (1,000–2,000 iterations) to compute confidence intervals for trend coefficients (β₁) across all 37 stations
- **Bootstrap prediction intervals** for August 2075 maximum temperatures
- **Chi-squared independence tests** (decade-level and year-level) to assess changes in frost day patterns

## Key Results

- All 37 stations show positive warming trend coefficients (β₁ > 0)
- Frost day frequency has significantly declined at most stations (p < 0.001)
- Coastal stations (e.g. Camborne) show weaker frost trends compared to inland stations (e.g. Durham, Oxford)

## Data

Data sourced from the [UK Met Office Historic Station Data](https://www.metoffice.gov.uk/research/climate/maps-and-data/historic-station-data).
CSV files are not included in this repository — download each station file directly
from the Met Office and rename to match filenames in the code (e.g. `durhamdata.csv`).

## Tech Stack

Python · NumPy · Pandas · Matplotlib · Scikit-learn · SciPy · Jupyter
