
# DSA210-Project  
## Climate and Coffee Prices: A Data-Enriched Global Study  

---

## Motivation  
Coffee is one of the world’s most traded agricultural commodities and is highly sensitive to climate conditions.  
Global warming and irregular weather patterns increasingly affect coffee yields, influencing both price and supply.  
This project aims to understand **how temperature and rainfall variations in major coffee-producing countries** (Brazil, Colombia, Ethiopia, Vietnam) affect **Arabica coffee prices**.  
By studying the intersection of **climate science and economics**, I hope to uncover meaningful patterns that explain market volatility and provide insights for sustainability and economic resilience.

---

## Data Source  

### 1. **Arabica Coffee Prices (FRED)**
- **Source:** [Federal Reserve Economic Data (FRED)](https://fred.stlouisfed.org/series/PCOFFOTMUSDM)  
- **Description:** Monthly Arabica coffee prices (`PCOFFOTMUSDM`), measured in U.S. cents per pound.  
- **Period:** 1990–2025  

### 2. **Climate Data**
Two complementary datasets were used for environmental variables:  

- **Berkeley Earth:** Country-level monthly average temperatures (°C) and anomalies (1900–present).  
- **World Bank Climate Knowledge Portal (CKP) API:** Observed monthly averages for temperature and precipitation for each country.  

The datasets were **merged by `year-month` identifiers** to create a unified table combining economic and climate data.

---

## Data Analysis  

### Data Preparation  
- FRED Arabica price data downloaded via `requests`.  
- Climate data fetched via Berkeley Earth text files or World Bank CKP API.  
- Data cleaned, standardized, and merged using `pandas`.  
- Created lag features (`tavg_c_lag1`, `lag3`, `lag6`) to capture delayed climate effects.

### Exploratory Data Analysis (EDA)  
- Line plots showing co-movement of price and temperature/precipitation.  
- Correlation heatmaps to identify relationships between variables.  
- Country-level comparisons to evaluate regional sensitivity.  

### Modeling  
- Regression methods (Linear, Ridge, Random Forest) to test if climate factors explain price variability.  
- Time-split validation for predicting monthly price changes.  
- SHAP and permutation feature importance for model interpretability.  

### Visualization  
- Price trends vs temperature and precipitation (same-month and lagged).  
- Scatter plots and bar charts summarizing correlations.  
- Feature-importance plots explaining key drivers.

---

## Findings  

1. **Visible correlation** between long-term temperature anomalies and Arabica price trends.  
2. **Lagged relationships** indicate that past 3–6 month climate conditions may influence current price fluctuations.  
3. **Country variation:** Brazil and Vietnam show stronger climate-price sensitivity, while Ethiopia’s relationship is weaker (possibly due to other economic factors).  
4. **Model interpretability:** Temperature lags and rainfall variability appear as top predictors in tree-based models.  
5. **Economic relevance:** Confirms that environmental shocks contribute to price volatility in agricultural markets.

---

## Limitations and Future Work  

### Limitations  
- Coffee price data reflects global averages, not producer-country-specific prices.  
- Climate data granularity (country-level) may mask local microclimate differences.  
- Potential confounding factors (currency rates, labor costs, policy shifts) not included.  

### Future Work  
- Incorporate **ENSO (El Niño/La Niña)** indices for global climate effects.  
- Add **futures market data** to analyze speculative impacts.  
- Extend to **supply-chain and export volume** data for a holistic view.  
- Apply **advanced ML models** (e.g., LSTM for time series forecasting).  
