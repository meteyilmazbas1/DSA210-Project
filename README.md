
# DSA210-Project  

## Overview  
Climate change has been increasingly linked to volatility in agricultural commodity prices. Coffee, as a climate-sensitive crop, offers a clear case to examine this relationship.  
This project investigates how **temperature and precipitation variations in major coffee-producing countries** (Brazil, Colombia, Ethiopia, Vietnam) influence the **global Arabica coffee price**.  
By integrating climate reanalysis data with economic time-series, the analysis aims to identify whether climate anomalies can partially explain or predict changes in coffee prices. Understanding these links may help producers and policymakers adapt to climate risks in global trade.

---

## Project Goal  
The main goal of this project is to explore how **climate indicators** (temperature, rainfall, anomalies) correlate with **coffee price movements** and whether short-term or lagged effects exist.  
By studying this connection, I aim to uncover evidence of climate-driven economic fluctuations and evaluate if machine learning models can capture meaningful predictive patterns.  

These questions will be addressed through monthly data spanning multiple decades (1990–2025) from trusted open sources (FRED, Berkeley Earth, World Bank).

---

## Research Questions  
1. How do temperature and precipitation changes in coffee-producing countries affect Arabica coffee prices?  
2. Are there delayed (lagged) effects of climate conditions on subsequent coffee price movements?  
3. Which climate variables (temperature, rainfall, anomalies) have the strongest statistical relationship with price levels?  
4. Do correlations differ among producer countries (Brazil vs. Ethiopia vs. Vietnam)?  
5. Can simple regression or tree-based models explain or forecast coffee price changes based on climate data?  
6. Are there seasonal or cyclical patterns connecting production climate and commodity market behavior?  

---

## Dataset  

### Primary Data Sources  
- **Arabica Coffee Prices (FRED):**  
  Monthly Arabica coffee price index (`PCOFFOTMUSDM`), in U.S. cents per pound, from 1990 to 2025.  
- **Climate Data (Berkeley Earth / World Bank):**  
  Monthly mean temperature and total precipitation data for key producer countries.  
  - Berkeley Earth provides long-term country-level climate summaries.  
  - World Bank CKP API offers observed monthly temperature and rainfall averages.

### Data Enrichment  
Economic and environmental datasets will be merged by **year-month** identifiers.  
For each country, the merged table will include both **current** and **lagged** climate variables (1-, 3-, and 6-month delays) to explore short-term effects.  

### Temporal Scope  
- Time period: **January 1990 – December 2025**  
- Frequency: **Monthly** observations  

---

## Data Structure  
The unified dataset will contain the following variables:


date: Month and year of observation
year_month: Year–month identifier for merging 
arabica_price: Arabica coffee price (UScents per pound)
country: Producer country (Brazil, Colombia, Ethiopia, Vietnam)
tavg_c: Monthly average temperature (°C)
pr_mm: Total monthly precipitation (mm)
temp_anomaly: Temperature anomaly vs. long-term average
tavg_c_lag1 / tavg_c_lag3 / tavg_c_lag6 Temperature lags (1, 3, 6 months)
pr_mm_lag1 / pr_mm_lag3 / pr_mm_lag6 | Precipitation lags (1, 3, 6 months)
season: Meteorological season (DJF, MAM, JJA, SON)
country_group: Producer region classification (Latin America / Africa / Asia)

---

## Expected Insights  
- Visualization of long-term co-movement between global coffee prices and regional climate variables.  
- Statistical evidence of lagged effects between climate anomalies and price shifts.  
- Country-specific differences showing which producers are more climate-sensitive.  
- Regression and feature-importance results highlighting which factors explain price volatility.  
- Practical interpretation for sustainability and supply-chain risk assessment.  
