# Client Project - Measuring the Economic Impact of a Natural Disaster

### David Bertsch, Mekdes Kebede, Chris Langan, Noah Monastersky

### April 29, 2019

## Problem Statement

How can we measure the economic impact of a disaster in terms of wages and unemployment?

## Plan

In order to approach this problem, we will look at an isolated natural disaster and investigate the economic impact that may have resulted in localities that were affected by the disaster. In this project, we will use Hurricane Sandy as a case study.

We will first select some relevant localities for analysis. Since we are investigating Hurricane Sandy, we will select Mid-Atlantic and Northeast coastal cities in the United States. This part of the United States was the most directly in the path of the storm.

The following localities will be analyzed:

- Atlantic City, NJ
- Baltimore, MD
- Boston, MA
- Bridgeport, CT
- New Haven, CT
- New London, CT
- Newport, RI
- Ocean City, MD
- Portland, ME
- Providence, RI

We will analyze the wages and unemployment in these localitites. The wage data is broken down by industry, and we will investigate how wages in each of these industries may have been impacted by Sandy.

In order to compare the relative impact of the storm in each of the localities of analysis, we will also investigate weather data that is related to the intensity of the storm conditions. We will be interested to see to what extent the relative economic impact in each locality is reflected by the relative intensity of the storm in each locality.

## Hypotheses

The following hypotheses will frame the focus of our analysis:

1. The occurrence of a natural disaster will lead to a pronounced loss of wages and increase in unemployment.

In general, we think that the occurrence of a distaster will have an economic impact on localities in the path of the disaster. The economic metrics that we are analyzing are wages and unemployment, so we think that we will see a drop in wages and an uptick in unemployment in the localities of analysis at the time immediately following Hurricane Sandy.

2. The occurrence of a natural disaster will negatively affect wages in tourism industries.

We think that tourism industries will experience the largest impact from a disaster, because those industries are based on people visiting, and people spending money in these localities. During a disaster event like a hurricane, we would expect that, for a somewhat extended period of time surrounding the disaster, there would be a a major dip in any tourism-related spending, and that this may ultimately be reflected in wages.

3. The occurrence of a natural disaster will not significantly affect wages in professional industries. 

Conversely, we do not think that wages in professional industries will be impacted significantly by the occurrence of a disaster. While these industries may lose some productivity related to having to close offices for a brief time, we feel that this will not be nearly enough to result in a significant drop in wages.

4. The relative intensity of a disaster in a given locality will be correlated to any negative impact on wages and unemployment.

We think that any localized economic impact resulting from a disaster will be proportional to the relative intensity of the disaster in that locality.

## Data

#### Wages

We gathered data on wages broken down by localities from the Bureau of Labor Statistics (BLS) through their API. (Information on how to use the BLS API can be found here: https://www.bls.gov/developers/home.htm) Specifically, we pulled data related to wages in our localities of analysis broken down into industries. This data was taken from the Quarterly Census of Labor and Wages reports.

The data for wages is broken down into the following categories:

- natural resources and mining
- construction
- manufacturing
- service-providing
- trade, transportation, and utilities
- information
- financial activities
- professional and business services
- education and health services
- leisure and hospitality
- other services
- unclassified

Wage data relateed shortcomings:

When collecting the economic data we collected wage and unemployment data but were only able to find monthly data for these two statistics which limited how much we were able to see the affects of natural distasters which often impact communities immediately. Additionally our wage datasets had many missing values which meant that some industries we could not affectively model and make conclusions about. When using BLS's API to get our wage data we were only able to bring in private industry data and were having difficulties bringing in government and non-profit industry data. This limited the amount of wage data we were able to gather on industries and it might be that government and non-profits are impacted differently from natural disasters compated to private industries. It is also worth noting that wages are not the best at measuring the economic impact of the sudden changes that natural disasters cause but are better measurements of how in demand different fields are. One possible alternative tht we could use in the future to measure the economic impact of sudden changes would be sales per day in a given locality.

#### Unemployment



#### Weather

In order to obtain historical weather data related to storm conditions, we gathered data from National Oceanic and Atmospheric Administration (NOAA). 

We collected data for the following weather metrics:

- barometric pressure
- precipitation
- maximum sustained 2 minute wind speed
- maximum sustained 5 second wind speed
- tide levels

We acquired precipitation and wind data through the use of NOAA's Climate Data Online Search (https://www.ncdc.noaa.gov/cdo-web/search). Historical data on barometric pressure and tide levels was readily available in downloadable csv files. Ultimately, we did not use the tide level data as a metric to measure storm intensity.


Weather data related shortcomings:

When I collected tide levels for each of the localities there were were not consistent patterns on how many readings were taken per day so some days would have more readings than other days. Even though there were not consistent readings per day tide readings were conistent in that they had readings every single day. When I collected barometric pressure statistics there were instances where there would be multiple months worth of data missing, which according to a employee at NOAA was most likely due to problems with the machines taking the readings.

## Methodology

Because natural disasters occur suddenly, we are trying to assess the sudden fluctuations in the economic data that may have occurred in the months following Hurricane Sandy, which occurred in October 2012. That means that, in the context of ARIMA modeling, we are interested in extracting the moving average component of this data (which handles sudden fluctuations), and ignoring the auto-regressive component of this data (which handles long-term trends). Because we have obvious seasonality in this data, we will take one order of seasonal differencing (12 months) before fitting the models.

We will perform this analysis on both the wages data and the unemployment data. We will perform a qualitative analysis of these time series in order to investigate if there is any noticeable change in wages or unemployment due to Hurricane Sandy. 


## Results



## Conclusions