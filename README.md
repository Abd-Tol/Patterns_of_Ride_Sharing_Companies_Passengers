# Patterns of Ride Sharing Companies' Passengers

## Disclaimer: 
- This project is part of the Data Analyst training program from Practicum by Yandex. More info in link below:
https://practicum.yandex.com/profile/practicum100-da/ 
- The Data Sets are not open to the public therefore they are not included in this project


# Project Setup

You're working as an analyst for Zuber, a new ride-sharing company that's launching in Chicago. Your task is to find patterns in the available information. You want to understand passenger preferences and the impact of external factors on rides.
Working with a database, you'll analyze data from competitors and test a hypothesis about the impact of weather on ride frequency.


# Description of the data

A database with info on taxi rides in Chicago:

`neighborhoods table`: data on city neighborhoods
- `name` : name of the neighborhood
- `neighborhood_id` : neighborhood code

`cabs` table: data on taxis
- `cab_id` : vehicle code
- `vehicle_id` : the vehicle's technical ID
- `company_name` : the company that owns the vehicle

`trips` table: data on rides
- `trip_id` : ride code
- `cab_id` : code of the vehicle operating the ride
- `start_ts` : date and time of the beginning of the ride (time rounded to the hour)
- `end_ts` : date and time of the end of the ride (time rounded to the hour)
- `duration_seconds` : ride duration in seconds
- `distance_miles` : ride distance in miles
- `pickup_location_id` : pickup neighborhood code
- `dropoff_location_id` : dropoff neighborhood code

`weather_records` table: data on weather
- `record_id` : weather record code
- `ts` : record date and time (time rounded to the hour)
- `temperature` : temperature when the record was taken
- `description` : brief description of weather conditions, e.g. "light rain" or "scattered clouds"

### Preview:

From the previous Part in SQL we found the Trip duration for rides from the `Loop` neighborhood to the `O'Hare` International Airport on Saturdays with consideration to the weather condition and by calculationg the average duration based on condition we can find the following:
1. **GOOD:** 1999.67
2. **BAD:** 2427.20

Based on the average above we can say that the duration of rides from the the Loop to O'Hare International Airport changes on rainy Saturdays but this alone is not enough as it is based solely on the average without factoring if the difference is significant therefore we will continue our work in Python after exporting the data from the SQL Database and our work here will include the following: 

