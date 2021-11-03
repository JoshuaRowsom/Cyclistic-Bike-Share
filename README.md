![Cyclistic](https://user-images.githubusercontent.com/91980090/140099515-c5a4ecb6-3a34-4c3a-808c-d176e57293cf.JPG)

# Cyclistic-Bike-Share 
#### Google Data Analytics Capstone

I am new to data analytics, and this is my first git repository, data analysis, coding, using R, and sharing my code. The project was to figure out how members and casual riders use Cyclistic bike shares bikes.

I asked the following questions:
1. Who is using the bikes?
2. What are they doing with the bikes, and what types of bikes are they using?
3. When are they using the bikes?
4. Where do there trip take them?
_________________________________________________________________________________________________________________________________________________________________________________

## Prerequisites
Data provided by [Divvy](https://divvy-tripdata.s3.amazonaws.com/index.html), 09/2020 to 09/2021.

The following packages:
```
library(lubridate)
library(tidyverse)
library(ggmap)
library(dplyr)
library(scales)
library(ggplot2)
```
If you are new to R, you need to ```install.packages(name of package)``` before you can load the with ```librabry(name of package)```
___________________________________________________________________________________________________________________________________________________________________________________

## Cleaning

I imported the files, ran ```colname``` to ensure that the names stayed the same over the years, and then ran ```str``` to check for incongruencies, and converted 2020- 09, 10, and 11 ride_id and rideable_type to ```as.character``` to match the rest of the months. Next, I removed any bikes in service and rows missing data.  Then, I created new columns for the date and times, including month, day, year, weekday, month/year, ride length, start and end times. Finally, I arranged the weekdays for your viewing pleasure.
________________________________________________________________________________________________________________________________________________________________________________

## Analysis
###  Who is using the bikes?

Cyclistic Bike Share has 4.8 million rides that are broken into two group, members and casuals. 

![a67aa27f-4f3c-4124-b3d8-da1593e0528a](https://user-images.githubusercontent.com/91980090/140192252-6761bf3e-7115-4dfe-8912-b76138b2581c.png)
![6ef66150-f127-47fe-827c-d6e8245c5d19](https://user-images.githubusercontent.com/91980090/140192272-85064368-a668-4eaf-bb7e-2571a15a5539.png)
![13345334-363e-4358-a054-b1456c4d32d3](https://user-images.githubusercontent.com/91980090/140192263-c6429ae1-30b1-4d60-814e-9fa2ebfbd581.png)



This data shows us that members use the bike more than casuals during weekdays and casuals overtaske members on weekends. There was a 23% increase in casual users and a 24% increase in members year over year in the month of September.

## What types of bikes are they using?
Cyclistic Bike share has three types of bikes, classic, docked, and electric.  

![0bf67a40-a691-4b6e-b017-84feab520f7f](https://user-images.githubusercontent.com/91980090/140181863-d40b6141-151f-462f-bafa-c83cc05497ad.png)

After November classic bikes became the most used bikes. After January members stopped using docked bikes

## When are they using the bikes?
Before I could run the numbers for duration I had to check if there were any outliers. Fur the duration calculation I removed the top and bottom 5% so the ouliers would not effect the averages. 

![c0d98883-61fd-4357-b003-c2e9e5a41925](https://user-images.githubusercontent.com/91980090/140185092-a6f4ffdc-4cb7-4c44-a8c2-e719103b7a8c.png)

Casuals on average, ride 28% more time than members. 

![af319efd-edbb-473b-b069-fe4e695ec346](https://user-images.githubusercontent.com/91980090/140192520-d7b4e0e4-0300-48ce-b3eb-87b610ded0cd.png)
![730032fb-1718-4882-b018-f2d1e8d1536c](https://user-images.githubusercontent.com/91980090/140192878-b006b186-3f39-4b70-87e7-495c22818078.png)

These charts show thatmore mebers use the bikes in the morning and evening when compared to casuals.

## Where are they picking up and dropping of the bikes.

