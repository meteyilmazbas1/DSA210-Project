# DSA210 Project  
## Climate Effects on Global Coffee Prices  

### Motivation  
One of the most traded agricultural products and a vital export for many tropical economies is coffee. I chose this subject to research how environmental factors affect the volatility of the coffee market in the coffee-producing countries.  
 
My aim is to determine whether coffee prices in producing countries are related to temperature and rainfall change.

### Research Questions  
1. How do temperature and rainfall changes in producer countries affect coffee production?   
2. Can we predict coffee price volatility using combined climate and production variables?
### Hypothesis  
H₀: Average temperature and coffee production do not have a statistically
significant effect on coffee prices in producer countries.

H₁: Changes in average temperature and coffee production significantly
influence coffee prices in producer countries.

### Data and Sources  

Cecafe Brazilian-Coffee Exporters Council (https://www.cecafe.com.br/en/market-indicators/cepea-esalq-prices/#:~:text=Data%20Ar%C3%A1bica%20R%24%20Ar%C3%A1bica%20US%24,733)

Federacion Nacional de Cafeteros de Colombia (https://federaciondecafeteros.org/wp/coffee-statistics/?lang=en#:~:text=,more%20information%20about%20the%20price)

Indonesia Wholesale Price Index: Agriculture: Annual Crops: Coffee Bean - https://www.ceicdata.com/en/indonesia/wholesale-price-index-by-sector-agricultural/wholesale-price-index-agriculture-annual-crops-coffee-bean#:~:text=Indonesia%20Wholesale%20Price%20Index%3A%20Agriculture%3A,is%20categorized%20under%20Indonesia%20Premium

Berkeley Earth (https://berkeleyearth.org/data/) World Bank CKP(https://climateknowledgeportal.worldbank.org/) Copernicus (ERA5) (https://cds.climate.copernicus.eu/) WorldClim (https://www.worldclim.org/data/monthlywth.html)

FAOSTAT Food and Agriculture Organization (https://www.fao.org/faostat/en/#data/QC)

### Methodology  
Data Collection
- Collect data from FRED, FAOSTAT and Berkeley Earth.
- Align all series on a monthly basis.  

Data Integration 
- Link production to climate metrics by country.  

Data Analysis
- Perform correlation and time-lag analysis to explore relationships.   
- Merge climate and price panel by country, forward-filling values to match time frequency.
- Run regression models with interaction terms to test whether there is a climate–price relationship.
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
- Production has a measurable effect on coffee prices.
- Temperature captures climate-related supply-side effects.
- Results suggest climate and production jointly influence price dynamics.

