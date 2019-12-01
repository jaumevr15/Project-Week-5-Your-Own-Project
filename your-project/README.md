<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# The impact of the reopening of Sant Antoni Market in Barcelona
*[Jaume Vicens Rivas]*

*[Data full-time Ironhack Barcelona & 30/11/2019]*

## Content
- [Project Description](#project-description)
- [Questions & Hypotheses](#questions-hypotheses)
- [Dataset](#dataset)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
This project analyzes the impact of the reopening of Sant Antoni Market in May 2018 using three main variables: rental prices, unemployment and number of Airbnb listings in Sant Antoni area. These variables are analyzed before, during and after the reopening.

## Questions & Hypotheses
As a neighbour of Sant Antoni area, I could personally feel some effects which I related to the reopening: my landlord insisted on increasing the rent, I saw a trend of businesses being opened and felt the increase of tourists in the area. For this reason, this projects wants to answer the following questions using real data:
* Has the Sant Antoni market made an effect in the area since it was reopened?
* Has the reopening affected the rental prices in the area and its surroundings?
* Has the reopening affected the unemployment rate of the area and surrounding neighbourhoods?
* Has the number of Airbnb listings increased since the reopening of the market?

## Dataset
The project used several different sources to find relevant data:
- Barcelona Open Data: [https://opendata-ajuntament.barcelona.cat/es/] for rental prices per neighbourhood and unemployment rate, which has been cleaned and adapted having the following as outputs found in the folder [datasets]:
 * 00_barr_rent_increment.csv [The increase of rent per neighbourhood from 2013 to 2019 in percentage]
 * 01_barr_rent_13_18.csv [Rental prices per neighbourhood from 2013 to 2019, in absolute numbers per apartment, per month]
 * 02_barr_rent_19_trim.csv [Rental prices per neighbourhood in 2019, per quarter, in absolute numners per apartment, per month]
 
 * 20_unemployment_2019.csv [Unemployment rate per month, per neighbourhood in 2019]
 * 21_unemployment_2018.csv [Unemployment rate per month, per neighbourhood in 2018]
 * 22_unemployment_2017.csv [Unemployment rate per month, per neighbourhood in 2017]
 
- Eixos (through Open Data Barcelona): [http://eixos.cat/] for listings of businesses in Barcelona. This data will finally not used as part of the analysis as the time period of this data does not match with the analysis. 
* 10_cens_locals_2014.csv [Business listings in Barcelona in 2014]
* 11_cens_locals_2016.csv [Business listings in Barcelona in 2016]
 
 - InsideAirbnb: [http://insideairbnb.com/get-the-data.html] for the number of listings of Airbnb apartments in Barcelona. 
* 30_listings_airbnb_0415.csv [Airbnb listings in Barcelona by April 2015]
* 31_listings_airbnb_1116.csv [Airbnb listings in Barcelona by November 2016]
* 32_listings_airbnb_0417.csv [Airbnb listings in Barcelona by April 2017]
* 33_listings_airbnb_0418.csv [Airbnb listings in Barcelona by April 2018]
* 34_listings_airbnb_0419.csv [Airbnb listings in Barcelona by April 2019]

-  [https://github.com/martgnz/bcn-geodata] for geojson files with the limits of each neighbourhood in Barcelona:
* 70_barris.geojson

There is as well a few short databases gathering particular information needed for the project:
* 40_neighbourhood_stats.csv [Population and area in sqm*10000 of the analyzed neighbourhoods]
* 50_density_df.csv [Density of Airbnb listings per areaa]
* 60_density_df_for_geojson.csv [Density of Airbnb lisings in 2019, adapted for geojson file to use in Tableau]


## Workflow
The main challenge was when defining the question to understand which variables should be used when defining impact and finding the right data to try to answer the question. In the case of the business listings database from Eixos, although finding it as one of the most representative databases to analyse, the analysis had to drop this variable due to lacking most recent information. 

Once question and data is defined, the use of many different files and datasets made the cleaning process slower than expected. And when trying to find very particular information from the data. Some manual manipulation was required to have the data in the required format.

#### 3 minutes presentation
ONe of the main goals of this project was to be able to summarize the analysis in a three minutes presentation addressed to non-technical audience. This meant studying very carefully the use of visualisations and simplifying them in a wway that could be understood easily. Tools like Tableau and Pyplot were used and optimised to get the desired output.


## Organization
The project was firstly organized and visualised in a white board to understand the to-do's and main objectives, and later summarized in a Trello board that you can find here: [https://trello.com/b/IsUO05K1/sant-antoni-market]

The repository is divided into four different parts/folders:
 * code_cleaning: Jupyter notebook files to make the data cleaning and plots creation possible.
 * databases: All needed databases mentioned above.
 * final_plots: The different plots obtained.
 * presentation_pics: All the pictures used in the presentation.

## Links
[Repository](https://github.com/jaumevr15/Sant-Antoni-Market-Impact)  
[Slides](https://slides.com/jaumevicensrivas/sant_antoni_market)  
[Trello](https://trello.com/b/IsUO05K1/sant-antoni-market)  
