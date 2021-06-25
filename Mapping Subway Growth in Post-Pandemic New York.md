# Mapping Subway Growth in Post-Pandemic New York 

Elizabeth Naameh

## Abstract

The goal of this project is to understand subway ridership trends in New York as the city resumes normal life in a ‘post-pandemic’ world to help the NYC Department of Transportation [keep riders healthy](https://www.wsj.com/articles/how-does-new-york-keep-transit-riders-safe-from-covid-19-trial-and-error-11609678802). I worked with data provided by the Metropolitan Transit Agency and the City of New York, leveraging numerical, temporal and geographic feature engineering along with linear regression to extract ridership trends for the first six months of 2021. After plotting popularity and growth per station and by borough, I compared ridership against pre-pandemic levels using 2019 data. I built interactive visualizations and communicate my results using Plotly.

## Design

The NYC DOT is tasked with keeping riders as the economy re-opens. This includes monitoring subway stations for overcrowding, which remains a health risk as vaccination efforts continue, and ensuring mass public transit remains safe to use. The Agency has solicited the support of UrbanFootprint, a software company that helps public- andn private-sector organizations derive actionable insights from environmental, urban, and socio-economic data. The results from this analysis will be used to inform plans to deploy more buses in hot spots and invest in alternate transit options, such as creating [more busways](https://www.nytimes.com/2020/07/06/nyregion/mta-buses-nyc-coronavirus.html), [bike lanes](https://www.nytimes.com/2021/01/28/nyregion/bike-brooklyn-bridge-de-blasio.html), and [bike parking](https://www.nytimes.com/2021/01/26/nyregion/bike-parking-nyc.html), to relieve overcrowding. 

## Data

I'm looking at the MTA's weekly [turnstile CSVs](http://web.mta.info/developers/turnstile.html). Each row contains a count of the number of the people who swiped through, or exited, a given turnstile within a four hour interval. So, it's possible to observe the flow of passengers throughout the day. The data pulled covers the time periods from January through June of 2021 and, for pre-pandemic comparison purposes, March through June of 2019. I am also using [MTA's Stations location data](https://data.cityofnewyork.us/Transportation/Subway-Stations/arq3-7z49) which maps stations to their latitude/longitudes for geospatial visualization, and [NYC borough maps](https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm) data to map my findings. Although the datasets include information for 439 subway stations throughout New York, I limited my analysis to the busiest 100 as determined by overall foot traffic.

## Algorithms

*Data Cleaning* 

1. Identifying faulty turnstile data by comparing cumulative entries and exits over time, and adjusting for reverse counters and counter resets
2. Regularized passenger counts (i.e. removing weekends and federal holidays) to better identify growth trends

*Feature Engineering*

1. Mapping latitude and longitude to boroughs so analysis could identify geographic trends
2. Combining numerical columns to produce new numeric features to highlight illogical values for passenger counts identified during EDA and capture trends

*Models*

Linear regression was used to identify boroughs and stations with the fastest absolute growth, as well as the fastest return to pre-pandemic ridership levels. 

## Tools

- Numpy and Pandas for data manipulation
- Scikit-learn for modeling
- Matplotlib and Seaborn for plotting
- Plotly for interactive visualizations
- Geopandas for geospatial analysis

## Communication

In addition to the slides and visuals presented, the MTA Analysis will be embedded on my personal website and blog.

<img src="https://github.com/lizzynaameh/mta_eda/raw/46df9804bebbd516b5c471e73433f6efb68f3bb2/Images/MTA%20Ridership%20in%202021%20-%20borough%20map.png" width="300" height="450">
<img src="https://github.com/lizzynaameh/mta_eda/blob/main/Images/Subway%20Traffic%20Growth%20by%20Borough%2C%202021.png" width="750" height="390">

![MTA Ridership in 2021 - borough map](https://github.com/lizzynaameh/mta_eda/raw/46df9804bebbd516b5c471e73433f6efb68f3bb2/Images/MTA%20Ridership%20in%202021%20-%20borough%20map.png)
![Subway Traffic Growth by Borough, 2021](https://github.com/lizzynaameh/mta_eda/blob/main/Images/Subway%20Traffic%20Growth%20by%20Borough%2C%202021.png)
