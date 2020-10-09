# Surfs_up

## Project Overview

We are given a task to analyze the weather and precipitation levels on a Hawaiian island, Oahu. Our client, W. Avy wants to know whether or not it's a good idea to invest money in a Surf and Ice Cream Shop there.

The data analyze is important to W. Avy as some precipitation is necessary to create a favorable flora and environment, but too much precipitation would make us miss out on business opportunities for the store.

## Resources

- Data Source: hawaii.sqlite
- Software: anaconda3, python 3.7.7, jupyter notebook, flask
- Library: matplotlib, pandas, numpy, datetime, sqlalchemy, and flask

## Project Analysis

Having created a bar chart based on the sqlite file provided by W. Avy, we can see that there are some trends, such as some months having more precipitation than others.
The bar chart shows precipitation amounts for every day between Aug - 2016 to Aug - 2017.


![](Images/precipitation.png)

We also calculated some statistics on the precipitation levels for same time period:

![](Images/precipitation_stat.png)

## Challenge Overview

What could be better for a business than being sustainable all year-round? W. Avy liked the above analysis, and he requested additional information about temperature trends before opening the surf shop. Specifically, he wanted temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Challenge Analysis

Analysis was done by extracting all of June temperature data and December temperature data. The statistics are displayed below.

#### June: 

![](Images/june_temps.png)


#### December:

![](Images/december_temps.png)


## Differences
- Average temperatures in June and December are 75 and 72 degs F, which indicates more people will surf in June than in December.
- Max temperatures in June and December are 85 and 83 degs F, which indicates there will be days in December, when icecream sales will be high.
- Min temperatures in June and December are 64 and 56 degs F, which indicates there will be days in June, when icecream sales will go down.

## Summary

Based on the information we can recommend that opening surf and icecream shops in Oahu is a sound investment. With temperatures @70+ deg F, Oahu is a good place to surf and have icecreams after surfing.

## Additional Queries

- To have a better idea about the weather, following queries would help out more:
  - a query to get the max, min, avg precipitations recorded by station for months of June and December.
    - select station, strftime('%m', date) date, max(prcp), min(prcp), avg(prcp) from measurement where strftime('%m', date) in ('07', '12') group by station, strftime('%m', date)
a query to get the max, min, avg temperatures recorded by station for months of June and December.
select station, strftime('%m', date) date, max(tobs), min(tobs), avg(tobs) from measurement where strftime('%m', date) in ('07', '12') group by station, strftime('%m', date)
