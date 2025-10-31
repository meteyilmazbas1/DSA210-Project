# DSA210 Project  
## Climate and Coffee Prices: A Data-Enriched Global Study

### Problem Definition  
Global coffee prices fluctuate not only due to economic factors but also because of climate variability.  
Since coffee is a climate-sensitive crop, changes in temperature and precipitation directly influence supply, yield, and thus market prices.  
This project aims to analyze how climate indicators (temperature, rainfall, anomalies) in major coffee-producing countries (Brazil, Colombia, Ethiopia, Vietnam) relate to Arabica coffee price changes.  
The goal is to identify whether climate conditions can partially explain or predict price volatility.

### Hypothesis  
H₀ (Null Hypothesis): Climate variables (temperature and precipitation) have no significant relationship with Arabica coffee prices.  
H₁ (Alternative Hypothesis): Climate variables, especially temperature and precipitation anomalies, significantly influence Arabica coffee prices—either immediately or with time lags.  

The project will test whether short-term (1–3 months) and medium-term (up to 6 months) lag effects of climate data can help explain price changes.

### Data to Be Used and Rationale
Two types of data will be integrated to connect environmental and economic dimensions:  

1. Economic Data – Coffee Prices  
   Source: [FRED – Federal Reserve Economic Data](https://fred.stlouisfed.org/series/PCOFFOTMUSDM)  
   Variable: Monthly Arabica coffee prices (`PCOFFOTMUSDM`) in U.S. cents per pound (1990–2025).  
   Reason: Represents a reliable global indicator of market price trends.

2. Climate Data – Temperature and Precipitation
   Sources:
   Berkeley Earth](https://berkeleyearth.org/data/) – long-term country-level monthly temperatures and anomalies.  
   World Bank Climate Knowledge Portal (CKP)](https://climateknowledgeportal.worldbank.org/api/v1/country) – observed monthly averages for temperature and rainfall.  
   Reason: Allows comparison between weather conditions and price dynamics for each producer country.  

By merging these datasets by year–month, the project can explore both immediate and lagged effects (1, 3, and 6 months) of climate variables on coffee prices.

### Data Collection Method  
The coffee price dataset will be directly downloaded from FRED as a CSV file.  
The climate data will be accessed in two ways:  
Download country-level temperature files from Berkeley Earth.  
Use World Bank CKP API to programmatically collect observed monthly climate indicators (temperature, precipitation).  
Both datasets will be cleaned and combined using Python (`pandas`).  

### Expected Outcome  
Identification of statistically significant links between climate anomalies and coffee prices.  
Evidence of lagged effects where previous climate conditions influence later market prices.  
Country-level comparison showing which producers are most affected by environmental changes.  
Foundational insight for sustainable agriculture and climate risk management.
