# [Power BI] Airbnb Listings Analysis - 5 Asian Famous Tourism Cities

## I. Introduction

### 1. Context

Airbnb Inc. is an American company operating an online marketplace for short- and long-term homestays and experiences. Started in 2007 with an air mattress in an extra room, Airbnb today has a market capitalization of over $90 billion with 7M+ listings, 4M+ hosts covering 100K cities and towns in 220+ countries and regions worldwide. 

Airbnb enables people to rent out their homes or spare rooms to tourists, however, has been accused of inflating house prices, pushing out locals, straining resources and fuelling overtourism. Around the world, countries have started to place restrictions on Airbnb and especially short-term rentals in order to counteract this.

For example, in **Japan**, short-term rentals are limited to 180 days per year and must either have an owner living onsite or a dedicated person in charge of admin. Hosts must also collect guest data for government reporting. In certain districts, rentals are only permitted at specified times of the year. In **Singapore**, there are currently no licensing requirements for Airbnb properties, however, property rentals must be at least 3 months long (for private properties) or 6 months long (for public properties - HDB). HDB flats also cannot be rented out to tourists.

This project aims to provide a broad audience with the answers to several questions related to some famous tourist-attracted cities in Asia including **Bangkok, Tokyo, Taipei, Hongkong** and **Singapore**: *How many listings and hosts are there is these cities? How many listings does each host have? Which listings type is more popular? Single-listings or multi-listings? Short-term or Long-term? What types of room are listed? How do the prices differ? etc.*

### 2. Dataset

The dataset was provided by [Inside Airbnb](http://insideairbnb.com/get-the-data) with [Data Policies](http://insideairbnb.com/data-policies/) and [Disclaimers](http://insideairbnb.com/data-assumptions/).

The data utilizes public information compiled from the Airbnb web-site. Data is verified, cleansed, analyzed and aggregated.
No "private" information is being used. 

This project will use 5 CSV files (city-listings.csv) of 5 Asian cities downloaded from Inside Airbnb website (dated June 2023), with the same structure and format. 

Data Dictionary as follows:

| Field                          | Type     | Description                                                                                                                                                                                           |
|--------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| id                             | integer  | Airbnb's unique identifier for the listing                                                                                                                                                            |
| name                           | string   |                                                                                                                                                                                                       |
| host_id                        | integer  |                                                                                                                                                                                                       |
| host_name                      | string   |                                                                                                                                                                                                       |
| neighbourhood_group            | text     | The neighbourhood group as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles.                                                           |
| neighbourhood                  | text     | The neighbourhood as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles.                                                                 |
| latitude                       | numeric  | Uses the World Geodetic System (WGS84) projection for latitude and longitude.                                                                                                                         |
| longitude                      |          | Uses the World Geodetic System (WGS84) projection for latitude and longitude.                                                                                                                         |
| room_type                      | string   |                                                                                                                                                                                                       |
| price                          | currency | daily price in local currency. Note, $ sign may be used despite locale                                                                                                                                |
| minimum_nights                 | integer  | minimum number of night stay for the listing (calendar rules may be different)                                                                                                                        |
| number_of_reviews              | integer  | The number of reviews the listing has                                                                                                                                                                 |
| last_review                    | date     | The date of the last/newest review                                                                                                                                                                    |
| calculated_host_listings_count | integer  | The number of listings the host has in the current scrape, in the city/region geography.                                                                                                              |
| availability_365               | integer  | avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may be not available because it has been booked by a guest or blocked by the host. |
| number_of_reviews_ltm          | integer  | The number of reviews the listing has (in the last 12 months)                                                                                                                                         |
| license                        | string   |                                                                                                                                                                                                       |

### 3. Project Goal

The goal of the **Airbnb Listings Analysis of 5 Asian Cities** project is to conduct a comprehensive analysis of lodging properties listed on Airbnb in Bangkok, Tokyo, Taipei, Hongkong and Singapore to derive meaningful insights into listings in these markets.

The primary tool used for the analysis is Microsoft Power BI, which enables the connection to the dataset, data transformations and the creation of a meaningful and insightful report.


### 4. Project Roadmap

1. **Data Acquisition:** The initial step involved downloading the listings dataset from Inside Airbnb website.
2. **Data Connection**: Import 5 csv files into MS Power BI Desktop, append all queries as a new query, display source table name column as the city name.
3. **Exploratory Data Analysis**: Use Query Editor to gain insights into the data quality, structure and distributions.
4. **Data Cleaning:** Due to the high quality of the dataset, no significant data cleaning was necessary.
5. **Data Modeling**: There is only one large table appended from 5 csv files (of 5 different cities) with the same format and structure. There are some new tables created for easier and clearer calculation of measures. New relationships are established respondingly.
6. **Comprehensive Analysis**: Utilized calculated columns and measures to generate new data insights and enhance analysis capabilities.
7. **Detailed Report:** One-page report featuring valuable insights and practical information about Airbnb Listings in 5 Asian Famous Tourism Cities: Bangkok, Tokyo, Taipei, Hongkong and Singapore.


## II. Final Report

[MS PowerBI Link](https://app.powerbi.com/reportEmbed?reportId=7314c2cf-27de-4286-91c5-e5706b673c60&autoAuth=true&ctid=bc30914a-fec6-4dd0-adc0-5845114e6713)

## III. Key findings

- **Listings Count**: Among 5 cities, Bangkok has by far the most number of listings. Singapore has the least listings but the highest percentage of recently active listings (>80%). On the contrary, nearly 80% of listings in Tokyo have no reviews in the last 6 months.
- **Listings per Host**: Almost 2/3 hosts in Bangkok have only one listing. In all cities, nearly a half of all hosts own 10+ listings. More than 1/3 hosts own 10-99 listings. In Hongkong, nearly 1/3 of hosts have 100+ listings, while in Taipei and Tokyo, no hosts have more than 100 listings. Top 10 Hosts own total 2.9K listings, equivalent to 6.7% of all listings, mainly distributed in Hongkong.
- **Room type**: Entire home/apartment is the most popular room type in almost all cities, except for Hongkong, where Private room is predominant. Hotel room and Shared room are less common in all cities, account for only 5-10% of all listings. 
- **Terms**: Nearly 70% of listings in Singapore and more than 50% of listings in Hongkong require long-term rentals, while almost all listings in Tokyo accept short-term rentals.
- **Prices**: Airbnb is not always cheaper than a hotel! Entire home/apartment is 35-45% more expensive than hotel room in Singapore and Hongkong. Singapore is most expensive with prices of 3.3 -2.5 times higher than the figures of Bangkok and Hongkong respectively. Prices in Singapore also fluctuate within the widest range, followed by Taipei. In all cities, mean prices are much higher than median, which means the majority of prices are lower, but have unusually high values.