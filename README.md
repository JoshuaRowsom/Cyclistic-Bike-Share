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
___________________________________________________________________________________________________________________________________________________________________________________

## Cleaning

I imported the files, ran ```colname``` to ensure that the names stayed the same over the years, and then ran ```str``` to check for incongruencies, and converted 2020- 09, 10, and 11 ride_id and rideable_type to ```as.character``` to match the rest of the months. Next, I removed any bikes in service and rows missing data.  Then, I created new columns for the date and times, including month, day, year, weekday, month/year, ride length, start and end times. Finally, I arranged the weekdays for your viewing pleasure.
________________________________________________________________________________________________________________________________________________________________________________

## Analysis
###  Who is using the bikes?

Cyclistic Bike Share has members and casuals who have accrued 4.8 million rides over the past 13 months.

![Total rides](https://user-images.githubusercontent.com/91980090/140583500-3678d841-77db-4a87-a9be-3b2791044205.jpeg)
![Weekday Rides](https://user-images.githubusercontent.com/91980090/140583515-c22e7b23-1e85-4ee1-bf1c-4f6847d9e927.jpeg)
![Monthly Rides](https://user-images.githubusercontent.com/91980090/140583525-669a62ab-49e0-4423-b611-f2fc8443daa2.jpeg)

This data shows that members use the bike more than casuals during weekdays, and casuals overtake members on weekends. Also, there was a 26.8% increase in casual users and a 13.2% increase in members in September year over year.

## What types of bikes are they using?
Cyclistic Bike share has three types of bikes, classic, docked, and electric.  

![Bike Type](https://user-images.githubusercontent.com/91980090/140583547-fbf7ed96-aee6-4dbc-a59c-244f7580b08e.jpeg)

After November, classic bikes became the most used bikes. After January members stopped using docked bikes

## When are they using the bikes?
Before I could run the numbers for duration I had to check if there were any outliers. Fur the duration calculation I removed the top and bottom 5% so the ouliers would not effect the averages. 
![Duration](https://user-images.githubusercontent.com/91980090/140583648-100b1fdc-a54d-45a4-87f8-33d9cdd1ec48.jpeg)

On Average, casuals ride 28% more time than members. 

![Start hour](https://user-images.githubusercontent.com/91980090/140583764-2f8e7f20-d2ad-48a7-938f-1dd612f56949.jpeg)

These charts show that more members use the bikes in the morning and evening when compared to casuals.

## Where are they picking up and dropping of the bikes.
![start loc](https://user-images.githubusercontent.com/91980090/140584522-4b8b299f-ec05-4a71-909b-43e31ac74d77.jpeg)
![end loc](https://user-images.githubusercontent.com/91980090/140584526-24c11e24-7061-4c65-bbb0-a0da6fdbbefd.jpeg)


# Conclusion
Casual riders use the bikes for a longer duration. Casuals average 18-minute rides, and members average 13-minutes. That's a 27% difference in time spent with the bike.

Members ride more from 5 am to 10 am, suggesting more members use the bikes to travel to work. From 10 am to 5 pm, members and casuals just about even out. Then, from 5 pm to 9 pm, members overtake casuals again. 

A glance at the maps, and four things pop out:
1. The density of casual riders starting and ending their rides in park and waterside locations. 
2. The similarities between the density between members and casuals north of latitude 41.92. 
3. The increase in density in members south of latitude 41.88 and west of longitude -87.650, a university area.
4. There is very little change in the density maps between start and end locations. 

The duration and density location differences between members and casuals suggest that casuals primarily use bikes for leisure and short exploration. In contrast, members primarily use bikes for work and school. 
One thing to note is that both members and casuals use classic bikes vastly more than other bikes, suggesting that users also use the bikes to be healthier, or there are not enough of the other bikes.
