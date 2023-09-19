# Using Voter File Data to Study Electoral Reform
This is a group capstone project completed for the MS in Data Science program at NYU. Group members are:
* Carolyn Kolaczyk
* Doma Ghale [@dg2491](https://github.com/dg2491)
* Jin Ishizuka [@jnshzk](https://github.com/jnshzk)
* Rodrigo Kreis de Paula [@rodrigokreis](https://github.com/rodrigokreis)

The goal of this project is to use voter file data consisting of nearly 190 million records to learn about how electoral reform affects participation in U.S. cities. This will involve wrangling and mining large datasets to uncover patterns in the demographic features associated with voter turnout across cities with and without ranked-choice-voting (RCV). We also develop predictive models to forecast the likely effects of RCV adoption on the turnout for different subgroups of voters.

## Data
Our voter-level data comes from the [L2 Political Academic Voter File](https://l2-data.com/datamapping/), which is a continuously updated database of registered voters in the US. It contains two types of files: Demographic and Vote History. The demographic file consists of 691 detailed socio-demographic variables for each voter. The vote history file contains information on which elections each voter has voted in since 1994.

We also use additional city-level [census data](https://simplemaps.com/data/us-cities). 

## Data Processing
We sample cities from eight states which have implemented ranked-choice-voting: 
* California
* Colorado
* Maine
* Maryland
* Minnesota
* New Mexico
* Utah
* Vermont

In order to obtain a sample of demographically similar RCV and non-RCV cities, we implemented a cosine similarity function. For each RCV city, we select the five non-RCV cities in the same state with the most similar demographics, using our cosine similarity function on census data at the city level. We modified our selection threshold to ensure that we have at least 30 non-RCV cities per state, if possible. If a state has data on less than 30 cities in total, we include all cities in that state. If a state has less than 6 RCV cities, we select a larger sample of the most similar non-RCV cities to get closer to our target of 30 non-RCV cities per state. This results in 30 RCV cities and 183 non-RCV cities for our analysis, whose geographic distribution is exhibited below:
 

## Visualizations

## Modelling

