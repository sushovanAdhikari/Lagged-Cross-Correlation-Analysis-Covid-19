# Lagged Cross-Correlation Analysis of Weekly COVID-19 Cases and Deaths in Louisiana

## Overview

This project explores the lagged relationship between weekly COVID-19 cases and deaths across the first three waves of the pandemic in Louisiana. Using time series cross-correlation and linear regression, we quantified how deaths lagged behind cases and analyzed the deaths-per-case ratio for each wave.

The analysis was conducted using publicly available data from the State of Louisiana and is accompanied by code notebooks and visualizations.

## Key Findings

### Lag Between Cases and Deaths:
- **Wave 1:** 7-week lag (deaths lag cases)  
- **Wave 2:** 15-week lag  
- **Wave 3:** 9-week lag  

### Deaths/Case Ratio (via linear regression slope):
- **Wave 1:** 0.038 (±0.004)  
- **Wave 2:** 0.0146 (±0.00048)  
- **Wave 3:** 0.0128 (±0.00055)  

These results suggest a decreasing mortality rate over time, potentially reflecting improved healthcare response and public health measures.

## Repository Contents

| File/Notebook               | Description                                        |
|----------------------------|--------------------------------------------------|
| `first_wave.csv`           | Weekly average cases and deaths during the first wave |
| `second_wave.csv`          | Weekly average data for the second wave           |
| `third_wave.csv`           | Weekly average data for the third wave            |
| `first_wave.ipynb`         | Cross-correlation and regression analysis for Wave 1 |
| `second_wave.ipynb`        | Analysis for Wave 2                                |
| `third_wave.ipynb`         | Analysis for Wave 3                                |
| `memorandum_covid_analysis.pdf` | Full report summarizing the methodology and findings |

## Methodology

### Cross-Correlation Analysis  
Used `scipy.signal.correlate` to measure the time lag between weekly cases and deaths. The peak lag was identified using `numpy.argmax`.

### Linear Regression  
Performed on lag-adjusted data to compute the slope representing the deaths-to-cases ratio using `scipy.stats.linregress`.

## Requirements

Install the required packages using:

```bash
pip install -r requirements.txt
```
## Visualizations

Each notebook contains:  
- Time-shifted plots of weekly cases and deaths  
- Regression plots showing the linear relationship after applying the lag  

## Author

**Sushovan Adhikari**  
Graduate Student at Southeastern Louisiana University  
Project Date: July 2023
