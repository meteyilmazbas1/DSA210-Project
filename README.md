# DSA210 Project  
## Climate Effects on Global Coffee Prices  

### Motivation  
Coffee is one of the most widely traded agricultural commodities in the world and a crucial export product for many tropical economies. Climate conditions such as temperature variability directly influence coffee yields and production stability, which in turn may affect global and local coffee prices.

The motivation of this project is to investigate whether climate-related variables, together with production levels, have a measurable impact on coffee prices in major coffee-producing countries. Understanding these relationships is increasingly important under climate change conditions.

### Research Questions  
1. How do changes in average temperature affect coffee production in producer countries?

2. Is there a relationship between coffee production levels and coffee prices?

3. Can coffee price movements be explained using combined climate and production variables?

### Hypotheses  
H₀ (Null Hypothesis): Average temperature and coffee production do not have a statistically
significant effect on coffee prices in producer countries.

H₁ (Alternative Hypothesis): Changes in average temperature and coffee production significantly influence coffee prices in producer countries.

### Data and Sources  

Cecafe Brazilian-Coffee Exporters Council (https://www.cecafe.com.br/en/market-indicators/cepea-esalq-prices/#:~:text=Data%20Ar%C3%A1bica%20R%24%20Ar%C3%A1bica%20US%24,733)

Federacion Nacional de Cafeteros de Colombia (https://federaciondecafeteros.org/wp/coffee-statistics/?lang=en#:~:text=,more%20information%20about%20the%20price)

Indonesia Wholesale Price Index: Agriculture: Annual Crops: Coffee Bean - https://www.ceicdata.com/en/indonesia/wholesale-price-index-by-sector-agricultural/wholesale-price-index-agriculture-annual-crops-coffee-bean#:~:text=Indonesia%20Wholesale%20Price%20Index%3A%20Agriculture%3A,is%20categorized%20under%20Indonesia%20Premium

Berkeley Earth (https://berkeleyearth.org/data/) World Bank CKP(https://climateknowledgeportal.worldbank.org/) Copernicus (ERA5) (https://cds.climate.copernicus.eu/) WorldClim (https://www.worldclim.org/data/monthlywth.html)

FAOSTAT Food and Agriculture Organization (https://www.fao.org/faostat/en/#data/QC)

### Methodology  
Data Collection
-Coffee production data is obtained from FAOSTAT.
-Coffee price data is collected from country-specific official sources.
-Climate data consists of annual average temperature measurements.

Data Integration
-All datasets are aggregated to an annual frequency.
-A panel dataset is constructed by country and year.
-Only overlapping years across all datasets are retained.

Data Analysis
-Exploratory data analysis is conducted using descriptive statistics and visualizations.
-Correlation analysis is used to examine relationships between variables.
-Regression analysis is applied to evaluate the impact of climate and production on coffee prices.

## Machine Learning Analysis

We model coffee price prediction as a supervised learning regression problem.
The target variable is coffee price, and the input features include:

- Coffee production (tons)
- Average annual temperature (°C)

We use a linear regression model (OLS) to analyze the relationship between
production, climate, and coffee prices for Brazil, Colombia, and Indonesia
between 1996–2024.

### Model Summary
- Supervised learning (regression)
- Train/Test split: 75% / 25%
- Evaluation metrics: R², RMSE

### Key Findings
- Coffee production has a measurable effect on coffee prices.
- Average temperature captures climate-related supply-side influences.
- Results indicate that climate and production variables jointly contribute to coffee price dynamics in producer countries.

