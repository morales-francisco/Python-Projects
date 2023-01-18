# Data Cleaning + EDA - Airbnb Buenos Aires #


## Introduction ##
Airbnb is an american company operating an online marketplace for short-term homestays and experiences. The company acts as a broker and charges a commission from each booking.

## Source ##
The data source is [Inside Airbnb](http://insideairbnb.com/get-the-data/).

Note: All the prices are expressed in Argentinian Pesos.

## Objective ##
I'll focus on three key topics in this project and analyze them:

- The hosts: their current number, growth, location, number of listings they have, and whether they are super hosts. 

- The listings: the typical nightly rate, the amenities that are most frequently offered, and the listing categories. 

- The neighborhoods with the most listings, the highest prices, and thus the best price-rating ratio.

## Conclusions ##

- From 2010 to 2022, the number of hosts increased linearly and consistently. 10127 hosts had listings at the time the dataset was created. 
- There is only one host with 2365 listings. This person  resides in the United Kingdom. 
- Argentina is where 93% of the hosts are located, with Buenos Aires accounting for 83% of them. Barcelona, Madrid, Miami, and New York have the highest concentrations of the remaining 7% who reside abroad. 
- Super-hosts make up 74% of the hosts.

- There is no evidence that the prices charged by super hosts and standard hosts differ significantly. 
- Super hosts typically receive higher overall review ratings than regular hosts. 
- 79 percent of hosts only have one listing. 
- The majority (87%) of listing types relate to the entire house/apartment, followed by a private room (11%). 
- Palermo, Recoleta, and San Nicolás are the areas with the most listings. 
- Palermo, Recoleta, Nuez, and Retiro all have higher prices than the other ten neighborhoods with the most listings, despite having a wider price range (greater interquartile range). I find numerous outliers in every situation.
- A single night costs, on average, $11308. The most expensive areas are Puerto Madero, Dock 1, Dock 4, and Dock 3. I kept the values below the 99th percentile for this analysis. 
- The areas with the best price-rating ratios are Boedo, Versalles, Parque Patricios, Villa General Mitre, and Parque Avellaneda.
