# Data Cleaning + EDA - Airbnb Buenos Aires #


## Introduction ##
Airbnb is an american company operating an online marketplace for short-term homestays and experiences. The company acts as a broker and charges a commission from each booking.

## Source ##
The data source is [Inside Airbnb](http://insideairbnb.com/get-the-data/).

[Link](https://docs.google.com/spreadsheets/d/1iWCNJcSutYqpULSQHlNyGInUvHg2BoUGoNRIGa6Szc4/edit#gid=1322284596) to the data dictionary.

Note: All the prices are expressed in Argentinian Pesos.

## Objective ##
In this project, I will analyze three main points:

- The hosts: how many there are currently, how they have grown, where they live, if they have one or more listings, if they are super hosts or not.

- The listings: how much a night costs on average, which are the most offered amenities, and the listings types.

- The neighborhoods: those with the most listings, the most expensive, and those with the best price-rating ratio.

## Conclusions ##

- The number of hosts grew linearly and steadily over the 2010-2022 period. By the time the dataset was created, there were 10127 hosts with listings.
- There is one host with 2365 listings. Lives in the UK.
- 93% of the hosts are located in Argentina and 83% of them are in Buenos Aires. Of the remaining 7% who live outside of Argentina, the cities with the highest participation are Barcelona, Madrid, Miami, and New York, among others.
- 74% of the hosts are super-hosts.
- There is no evidence of a significant difference between the prices offered by the super hosts that the standard ones.
- Super hosts receive, on average, a better overall review score than standard hosts.
- 79% of the hosts have only one listing.
- Of the listing types, 87% correspond to the entire home/apartment, followed by a private room with 11%.
- The neighborhoods with more listings are Palermo, Recoleta and San Nicolás.
- It can be seen that both Palermo, Recoleta, Nuñez, and Retiro have a higher price than the other 10 neighborhoods with the most listings, although with a greater dispersion (greater interquartile range). In all cases, I observe many outliers.
- The average price for one night is $11308. The most expensive neighborhoods are Dock 1, Dock 4, Dock 3 and Puerto Madero. For this analysis, I kept the values under the 99th percentile.
- The neighborhoods with the best price-rating ratio are Parque Avellaneda, Versalles, Parque Patricios, Villa General Mitre and Boedo.
