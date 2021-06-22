# mta_eda
MTA Ridership [exploratory data analysis]

### Project Proposal Template

#### Question/need:

- As New York City slowly resumes normal life and people return to work, the Metropolitan Transit Agency is tasked with [keeping riders safe](https://www.wsj.com/articles/how-does-new-york-keep-transit-riders-safe-from-covid-19-trial-and-error-11609678802). Overcrowding on subways will continue to present a health risk to riders unless addressed creatively. The MTA wants to understand where ridership is highest and growing the fastest in order to keep the public safe. 

  This information can inform plans to deploy more buses in hot spots and invest in alternate transit options, such as creating [more busways](https://www.nytimes.com/2020/07/06/nyregion/mta-buses-nyc-coronavirus.html) and bike lanes, to relieve overcrowding. In order for mass transit to persist, riders must view it as safe; this analysis represents a preliminary step toward reaching that goal.

#### Data Description:

- I'm looking at the MTA's weekly [turnstile CSVs](http://web.mta.info/developers/turnstile.html). Each row contains a count of the number of the people who swiped through, or exited, a given turnstile within a four hour interval. So, it's possible to observe the flow of passengers throughout the day. 
- I am also using MTA's [Stations data](http://web.mta.info/developers/developer-data-terms.html#data) which maps stations to their latitude/longitudes for geospatial visualization.
- Using the data, I'll construct two main metrics: passenger counts and relative percentage change of passengers by station.

#### Tools:

- I am using SQL to query in data, pandas for data analysis and manipiulation, matplotlib for visualizations, and geopandas for geospatial analysis.

#### MVP Goal:

- A minimum viable product would be tabular data on the most crowded stations, as well as those experiencing most rapid growth -- accompanied by visualizations.

<details class="details-reset details-overlay details-overlay-dark" id="jumpto-line-details-dialog" style="box-sizing: border-box; display: block;"><summary data-hotkey="l" aria-label="Jump to line" role="button" style="box-sizing: border-box; display: list-item; cursor: pointer; list-style: none;"></summary></details>