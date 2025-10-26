##Overview

Climate change has been increasingly linked to volatility in agricultural commodity prices. Coffee, as a climate-sensitive crop, offers a clear case to examine this relationship.
This project investigates how temperature and precipitation variations in major coffee-producing countries (Brazil, Colombia, Ethiopia, Vietnam) influence the global Arabica coffee price.
By integrating climate reanalysis data with economic time-series, the analysis aims to identify whether climate anomalies can partially explain or predict changes in coffee prices. Understanding these links may help producers and policymakers adapt to climate risks in global trade.

##Project Goal

The main goal of this project is to explore how climate indicators (temperature, rainfall, anomalies) correlate with coffee price movements and whether short-term or lagged effects exist.
By studying this connection, I aim to uncover evidence of climate-driven economic fluctuations and evaluate if machine learning models can capture meaningful predictive patterns.

These questions will be addressed through monthly data spanning multiple decades (1990–2025) from trusted open sources (FRED, Berkeley Earth, World Bank).

##Research Questions

How do temperature and precipitation changes in coffee-producing countries affect Arabica coffee prices?

Are there delayed (lagged) effects of climate conditions on subsequent coffee price movements?

Which climate variables (temperature, rainfall, anomalies) have the strongest statistical relationship with price levels?

Do correlations differ among producer countries (Brazil vs. Ethiopia vs. Vietnam)?

Can simple regression or tree-based models explain or forecast coffee price changes based on climate data?

Are there seasonal or cyclical patterns connecting production climate and commodity market behavior?

##Dataset
Primary Data Sources

Arabica Coffee Prices (FRED):
Monthly Arabica coffee price index (PCOFFOTMUSDM), in U.S. cents per pound, from 1990 to 2025.

Climate Data (Berkeley Earth / World Bank):
Monthly mean temperature and total precipitation data for key producer countries.

Berkeley Earth provides long-term country-level climate summaries.

World Bank CKP API offers observed monthly temperature and rainfall averages.

##Data Enrichment

Economic and environmental datasets will be merged by year-month identifiers.
For each country, the merged table will include both current and lagged climate variables (1-, 3-, and 6-month delays) to explore short-term effects.

Temporal Scope

Time period: January 1990 – December 2025

Frequency: Monthly observations

Data Structure

The unified dataset will contain the following variables:


##Expected Insights

Visualization of long-term co-movement between global coffee prices and regional climate variables.

Statistical evidence of lagged effects between climate anomalies and price shifts.

Country-specific differences showing which producers are more climate-sensitive.

Regression and feature-importance results highlighting which factors explain price volatility.

Practical interpretation for sustainability and supply-chain risk assessment.
