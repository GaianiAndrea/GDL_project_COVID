# Will COVID survive this summer?

This project explore an approach to covid cases forecasting based on Graph Neural Networks and mobility data.

## Description

Since the very beginning of coronavirus pandemic, cases of new infection have been recorded at multiple geographical locations at regular intervals ([OWID](https://github.com/owid/covid-19-data), [NYT](https://github.com/nytimes/covid-19-data), [JHU](https://github.com/CSSEGISandData/COVID-19)). Can we train a Spatiotemporal GNN to predict evolution of coronavirus’ spread?
Also, the graph costruction problem is challenging in this setting.

## Contributions
- Andrea Gaiani
- Rocco Felici

## Tools
[![tsl](https://torch-spatiotemporal.readthedocs.io/en/latest/_static/tsl_logo.svg)](https://torch-spatiotemporal.readthedocs.io/en/latest/#)[^1]

[^1]: TorchSpatiotemporal library that can be found on [github](https://github.com/TorchSpatiotemporal).


## Main references
A. Kapoor et al., “[Examining covid-19 forecasting using spatio-temporal graph neural networks](https://arxiv.org/abs/2007.03113)”, 2020. 

<!-- ## Related works -->


## Dataset
- adjacency_matrix: it contains the matrix which represents the adjacency of the counties. In this file columns and rows represent the counties and the value in the cell is 0 if the two counties are not adjacent, or 1 if they are. We consider adjacent every neighbouring county, every county with a maximum distance of 50 miles and each county with at least XX flight per year. To make this matrix we used: air_mobility, county_adjacency2010, sf12010countydistance50mile. 

- air_mobility:

- county_adjacency2010 is a dataset taken from:  https://www.nber.org/research/data/county-adjacency. In this dataset there are all the neighbouring counties.

- final_df_202X are a datasets created using population, us-counties-202X and vaccination_per_county_202X. In these datasets we have: number of cases, number of deaths, percentage of the population vaccinated and population, divided per FIPS and per day.

- population is a dataset where given a FIPS we have the population (census of 2019). To create this dataset we used COVID-19_Vaccinations_in_the_United_States_County

- sf12010countydistance50mile is a dataset taken from: https://www.nber.org/research/data/county-distance-database. This dataset shows the adjacent counties with a maximum distance of 50 miles.

- us-counties-202X is a dataset taken from: https://github.com/nytimes/covid-19-data. In these datasets we have the number of cases and deaths per each day and per each counties.

- vaccination_per_county_202X are dataset created from COVID-19_Vaccinations_in_the_United_States_County. These datsets show the percentage of the population vaccinated per each day and per each FIPS.

- COVID-19_Vaccinations_in_the_United_States_County is a dataset taken from: https://healthdata.gov/dataset/COVID-19-Vaccinations-in-the-United-States-County/ipdn-uaih/data. In this dataset there is all the relative data to the COVID-19, as percentage of the population vaccinated per each county per each day, but also a more detailed data as how many first doses are given in a given county for each date or also how many booster were distributed.
