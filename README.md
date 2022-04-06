# Data-Visualization-of-Greenhouse-Gases-and-CO2-Emission-in-Countries-Continents
## Abstract
Greenhouse gases are primarily responsible for making Earth a habitable planet for all living organisms. However, due to various factors including deforestation, pollution etc. the balance of required greenhouse gases has blown out of proportion resulting in global warming, climatic changes, potential geographic, ecological, physical and health adversities. This is threatening the lives of human beings and hundreds of thousands of living species. Carbon dioxide constitutes a major part of greenhouse gases and has been prevalent in the atmospheric levels followed by gases like methane, nitrous oxide etc. Burning fossil fuels and utilization of non-renewable resources aid in this ever-increasing problem [2]. In this report we have tried visualizing the amount of annual and per capita CO2 emission and its consumption in different countries and continents. Also, the utilization of non-renewable sources of energy by continents is highlighted. Owing to the various issues due to increasing CO2 levels, it is important for countries and continents (as whole), to progress towards zero CO2 emission for the well-being of the entire planet. We have also visualized the progress of countries to achieve this and their target years. We can see very few countries like Bhutan, Guyana, Cambodia have already achieved this. Others are trying to achieve it in target years ranging from 2050 to 2070.

## Data Gathering:

The dataset is obtained from the public website Our World in Data (https://ourworldindata.org/) available in public GitHub Datasets (https://github.com/awesomedata/awesome-public-datasets ). The website has stored a hub of datasets for various phenomena (COVID-19, CO2 Emission etc.)  in GitHub https://github.com/owid/  . The original dataset had 1 Vs of Big Data namely Variety.  Using web scraping, the required features and attributes were downloaded from the GitHub repository. The original dataset had around 2M rows and 58 features.

This dataset was combined with data of Countries and Continents scraped from Statistics provided by the United Nations. It had 291 rows and 2 features. Additionally, the data of countries was gathered which are  having net-zero CO2 emission target Net Zero Scorecard. It had around 4000 records and 62 features. The datasets was segregatedaccording to countries and continents. Around 6k and 7k records were retained for countries and continents respectively with around 50 features for each. Also, for net zero CO2 emissions only 67 unique countries and 4 features were retained as they were sufficient for the visualization. The datatypes in each dataset were either float, int, double, date or string type.  

To summarize, around 4 datasets of huge volume were gathered. After processing and cleaning,there were 3 segregated datasets with fewer attributes but a good number of features. This helped in a clear visualization.

## Data Exploration, Processing, Cleaning and/or Integration

❖	 Python was used to clean the datasets and used Google Data Studio to explore the raw dataset. 
❖	Through this visual and additional filtering, it was noticed that in the original raw CO2 dataset, retrieved from the GitHub repo, countries and continents were grouped together in the ‘country’ column.  This prompted to segregate the datasets wrt countries and continents. 
❖	Using python,  first integrated the Continents (from Contries_Continents.csv) to the original dataset and removed all Unicode characters from the entire dataset.
❖	Next, mapped the countries to their respective continents.Dropped records of 3 countries which were noise components.
❖	Next, segregated the datasets into 2 separate datasets specifically for countries and continents respectively. This was done with the intention of a cleaner, flexible and more user-friendly dashboard visualization. 
❖	Next, checked the distinct count of countries in a year. Since, all the countries had continuous data from 1995 onwards, considered taking data of only the last 25 years (1995-2020). Hence, dropped the records prior to 1995.
❖	Other noisy and null values of less significant data points were dropped.
❖	Cleaned the dataset for net-zero CO2 emission and retained important features required for visualization.

## Visualization
Used PowerBI as the visualization tool. Referred https://chartio.com/learn/charts/line-chart-complete-guide/ and https://multimedia.journalism.berkeley.edu/tutorials/visualizing-data-a-guide-to-chart-types/ for design chart options for each graph. The visualization answers below queries:
1. ★	Does GDP (per capita) affect  CO2 emission (per capita) and consumption of CO2 (per capita) for a country?
2. ★	Is it high time that some countries and continents need to monitor utilization of fossil fuels?
3. ★	Asia as a continent is peaking high in emitting CO2 and Greenhouse Gases
4. ★	Are countries progressing towards Net-Zero CO2 Emission?

## References:
1.	Hannah Ritchie and Max Roser (2020) - "CO₂ and Greenhouse Gas Emissions". Published online at OurWorldInData.org. Retrieved from: https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions [Online Resource]
2.	Christina Nunez (May 13, 2019) – “Carbon dioxide levels are at a record high. Here’s what you need to know.”. Published online at https://www.nationalgeographic.com/environment/article/greenhouse-gases 
3.	United Nations Statistics Division (22 Oct 2019) – “List of Countries by Continent” - https://statisticstimes.com/geography/countries-by-continents.php 
4.	https://github.com/awesomedata/awesome-public-datasets 
5.	Net Zero Tracker. Energy and Climate Intelligence Unit, Data-Driven EnviroLab, NewClimate Institute, Oxford Net Zero. 2021. https://zerotracker.net/ 
6.	Millenium Development Goals Indicators, The official United Nations site for the MDG Indicators, https://millenniumindicators.un.org/unsd/mdg/Metadata.aspx?IndicatorId=0&SeriesId=776 


