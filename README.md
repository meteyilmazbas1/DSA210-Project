# DSA210 Project  
## Climate Effects on Global Coffee Prices  

### Motivation  
One of the most traded agricultural products and a vital export for many tropical economies is coffee. I chose this subject to research how environmental factors affect the volatility of the coffee market in the coffee-producing countries.  
 
My aim is to determine whether coffee prices in producing countries are related to temperature and rainfall change. I also use Starbucks store counts to see if countries with larger coffee markets react differently to climate-driven price changes.

### Research Questions  
1. How do temperature and rainfall changes in producer countries affect coffee production?   
2. Can we predict coffee price volatility using combined climate, production, and transportation variables?
3. Does the size of a country’s coffee retail market (Starbucks store counts) influence the relationship between climate variables and price change?
### Hypothesis  
H₀: There is no correlation between the number of Starbucks store counts and how climate factors affect coffee prices. 

H₁: Higher store counts show stronger links between price variation and climate variables.

### Data and Sources  

Cecafe Brazilian-Coffee Exporters Council (https://www.cecafe.com.br/en/market-indicators/cepea-esalq-prices/#:~:text=Data%20Ar%C3%A1bica%20R%24%20Ar%C3%A1bica%20US%24,733)

Federacion Nacional de Cafeteros de Colombia (https://federaciondecafeteros.org/wp/coffee-statistics/?lang=en#:~:text=,more%20information%20about%20the%20price)

Indonesia Wholesale Price Index: Agriculture: Annual Crops: Coffee Bean - https://www.ceicdata.com/en/indonesia/wholesale-price-index-by-sector-agricultural/wholesale-price-index-agriculture-annual-crops-coffee-bean#:~:text=Indonesia%20Wholesale%20Price%20Index%3A%20Agriculture%3A,is%20categorized%20under%20Indonesia%20Premium

Berkeley Earth (https://berkeleyearth.org/data/) World Bank CKP(https://climateknowledgeportal.worldbank.org/) Copernicus (ERA5) (https://cds.climate.copernicus.eu/) WorldClim (https://www.worldclim.org/data/monthlywth.html)

FAOSTAT Food and Agriculture Organization (https://www.fao.org/faostat/en/#data/QC)

Statista - https://www.statista.com/statistics/218366/starbucks-stores-worldwide/ Kaggle - https://www.kaggle.com/code/gpreda/starbucks-location-worldwide-data-exploration
### Methodology  
Data Collection
- Collect data from FRED, FAOSTAT, Berkeley Earth, and shipping indicators.  
- Align all series on a monthly basis.  

Data Integration 
- Link production to climate metrics by country.  

Data Analysis
- Perform correlation and time-lag analysis to explore relationships.   
- Merge Starbucks store data with climate–price panel by country, forward-filling values to match time frequency.
- Run regression models with interaction terms to test whether market size moderates the climate–price relationship.
