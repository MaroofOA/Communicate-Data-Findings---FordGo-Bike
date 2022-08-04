# Ford GoBike System Data
## by Morufdeen Olatunbosun Atilola


## Dataset

This dataset includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. The data contains 183,412 rides with 16 variables which includes: Ride duration (Secs), Start and end time, start and end station id and Name, start and end station Latitutude and Longitude, Bike Id, User type, member birth year, Member gender, Bike share for all trip (Yes or No)

For the analysis, I selected duration as the main focus of exploration. From the peruse of the dataset, I believe that the distance between two points considering the start and end station latitude and longitude of each trip would have a significant impact on the duration. I also believe that user_type, birth_year (to determine member's age), and gender may also affect the duration of the trip.

Before I start the data exploration, I carried out some transformation on some of the features. These includes:

1. I created a new column for the distance covered on each trip using the latitude and longitude of the start and end date by applying haversine formula
2. I created a new column for the age of each member using the member birth year column
3. I created a new column for day of the week, hour of the day, and month of the year for both start and end time.

After the Preliminary data wrangling, the shape of the dataset was now 174952 rides with 24 features

## Summary of Findings

From the analysis, below are some of the findings as related to the main features (Duration):

1. The duration dataset is not normally distributed as it is skewed to the right with quite a number of trips were completed within a short period of time.
2. Majority of the trips started in the morning around 8am and evening around 5pm and most of the trips are done on weekdays (Monday to Friday)
3. There is a weak correlation between the duration, distance, and age. this boils to the fact that these three numerical variables are not normally distributed. We may also assumed that farther trips will take longer duration provided that variables like speed are constant, but more than 90% of the distance covered is between 0 to 20000m which was all completed within 0 to 75000secs.
4. Younger riders of ages between 20 to 40 years old spent longer duration to complete their trips, this may be due to the longer distance covered by the younger riders or the number of trips that the young riders embarked on.
5. Majority of the riders are within the age of 20-40 years and they completed their trips with an average distance covered between 1000 to 2000m that was completed within 500 to 2000 secs.
6. On an average, female riders are younger than male riders but the male riders completed their trips faster than the female riders.
7. Subscribers completed their trips within a very short period (less than 800 secs) on an average shorter than the customer users.



## Key Insights for Presentation

For the presentation, I focus on the influence of the age and distance on the duration of trips in seconds. Then, I consider the effect of some of the numerical variables particularly user_type and gender on the duration of the trip. I start by exploring the distribution of the main feature as well as the numerical features (distance and age). I explore the correlation between the numerical variables (duration and distance & duration and age).

Afterwards, I consider the relationship between the three numerical variables, then I use facetgrid to explore the duration and age with respect to the type of user and member gender. Lastly, I used a pointplot to explore the average duration across each day with respect to the user type.