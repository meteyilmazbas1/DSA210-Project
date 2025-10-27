# DSA210-Project  
## Climate and Coffee Prices: A Data-Enriched Global Study  

## Overview  
Climate change increasingly affects global agricultural commodities, especially coffee.  
This project examines how temperature and precipitation changes in major coffee-producing countries (Brazil, Colombia, Ethiopia, Vietnam) relate to Arabica coffee price fluctuations.  
The study integrates coffee prices with climate data to reveal possible environmental influences on market volatility.

## Research Questions  
1. How do temperature and rainfall changes influence Arabica coffee prices?  
2. Are there delayed effects between climate conditions and price changes?  
3. Which producer countries are most sensitive to climate variables?  
4. Can simple models predict coffee prices using climate indicators?

## Dataset  
- FRED: Monthly Arabica coffee prices (`PCOFFOTMUSDM`, 1990–2025).  
- Berkeley Earth / World Bank CKP: Monthly temperature and precipitation for each producer country.  
- Datasets were merged by `year-month` and lag features were created to study delayed impacts.

## Data Analysis  
1. Data Cleaning: Standardized time format, removed missing data, created lags.  
2. Exploratory Analysis: Plots and correlations of prices vs. climate variables.  
3. Modeling: Linear Regression, Ridge, and Random Forest to test predictability.  
4. Visualization: Time-series plots, scatter charts, and feature importance graphs.

## Findings  
- Clear long-term correlations between climate anomalies and Arabica prices.  
- 3–6 month lag effects observed in temperature and precipitation trends.  
- Brazil and Vietnam show higher sensitivity than Ethiopia or Colombia.  
- Tree-based models highlight temperature and rainfall as top predictors.

## Limitations & Future Work  
- Uses global price index — local market differences not captured.  
- Country-level averages may mask local climate variability.  
- Future work: add ENSO, export data, and deep learning models.
