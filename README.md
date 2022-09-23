# PyBer_Analysis
Analyze all the rideshare data from January to April of 2019 and create a compelling visualization.

## Overview of Project

### Purpose
The purpose of this project is to assist PyBer and V. Isualize create a summary DataFrame of the ride-sharing data by city type. In addition, the purpose of this project is to help Pyber improve their ride-sharing services and determine affordability for each city type.


## Analysis 
PyBer provided both city and ride data. The city data provided information on the city, city type and driver count, whereas the ride data provided information on the city, the date and time the ride accured, the cost of the ride (fare), and rider id. In order to run a comprehensive analysis, I needed to merge the two datasets into one DataFrame, so that I could analyze all items together. Since both datasets contained city, I just needed to include the columns from the city dataset to the left of the ride dataset. 

Image 1. 

![Merge Datasests](https://github.com/mrma2318/PyBer_Analysis/blob/6cc4ea7c39177fc49c0fb3b8666f1f87285eddb8/Resources/Image%201.png)

Before I could run any analysis, it's important to understand the data I am working with, so first I needed to get a summary of the dataset I was working with and put it into a seperate DataFrame. To get a summary DataFrame, I needed to get the total number of rides, drivers, and fares for each city type. To get the total number of rides per city type, I created a total rides variable that I set equal to the city type, and counted rides for each city type to get a total value. To get the total number of drivers and fares, I created variables that I set equal to the city type again, but this time had it set up to calculate the sum of drivers and fares based on city type. 

Image 2.

![Totals](https://github.com/mrma2318/PyBer_Analysis/blob/6cc4ea7c39177fc49c0fb3b8666f1f87285eddb8/Resources/Image%202.png)

In addition to the totals, it was also important to look at the average price per ride, as well as the average price per driver for each city type. To get these variables, I just needed to take the total fares and divide it by total rides and total drivers to get those values. While all this information was helpful, putting it into a summary dataframe will be beneficial to see all these items side by side to make comparisons and analyze the data. Therefore, I put all the variables I had just created and put them in summary dataframe. 

Table 1.

![Summary Dataframe](https://github.com/mrma2318/PyBer_Analysis/blob/6cc4ea7c39177fc49c0fb3b8666f1f87285eddb8/Resources/Image%203.png)

By looking at the table, you can gather information about the three city types. For example, urban cities have a lot higher number of total rides, drivers, and fares, but on average have a lower fare per ride and driver compared to rural and suburban cities. Whereas rural cities have a lot lower number of total rides, drivers, and fares, but have a higher average fare per ride and driver compared to suburban and urban cities. From this table, we can already gather that Rural cities might have less riders due to the high cost per ride per driver, whereas Urban areas have a lot more success with riders due to the afforable price per ride per driver. 

Now that I know this information, I can take a closer look at the data for PyBer and V. Isualize to create a multiple line graph showing the total weekly fares for each city. First, I needed to create another dataframe showing the sum of the fares for each day based on the city type and the date, and then reset the index so that I could create a new dataframe using the pivot table function. The pivot table allows me to see all the exact dates and times, as well as the total fare on those dates for each city type. In addition, I specified that I wanted to look at the dates between January 1, 2019 through April 29, 2019. After creating the pivot table for January through April, I needed to change the date index in the table to datetime so that I could resample by week. Once I changed the index, I was able to create a new dataframe using the resample function to get the sum of the fares by week. 

Table 2. 

![Weekly Fares Dataframe](https://github.com/mrma2318/PyBer_Analysis/blob/6cc4ea7c39177fc49c0fb3b8666f1f87285eddb8/Resources/Image%204.png)

## Results

Looking at the graph of the sum of the fares by week, it's difficult to read the table and generate a summary of the data. Therefore, creating a multiple line graph, we can take a look at each city type and the sum of the fares to visually see the difference between each city type and the sum of the fares. 

Daraframe Plot. 

![Resample Dataframe Plot](https://github.com/mrma2318/PyBer_Analysis/blob/6cc4ea7c39177fc49c0fb3b8666f1f87285eddb8/analysis/Pyber_fare_summary.png)

From the graph above you can see that Urban cities generated a higher amount of fares each month compared to suburban and rual cities. In addition, Rural cities generaded the lowest amount of fares each month compared to Urban and Suburban cities. The suburban cities are in the middle, they generate more fares than rural cities, but less than urban cities. This information supports our previous thoughts when viewing the summary dataframe we created earlier. Since urban cities have a lower ride fare average and lower price per diver, urban cities produce a greater overall fare total compared to the other cities because they get  significantly more riders compared to suburban and rural areas. In addition, rural areas have the highest average fare price per ride and a higher fare per driver. Therefore, they have a significatly lower amount of riders resulting in a lower total fare for rural areas. Lastly, suburban cities are in the middle. They have a higher fare price per ride and per driver compared to rural cities, but lower than urban cities. Therefore, they produce a higher total fare in suburban cities compared to rural cities, but less than urban cities. 

## Summary

### Business Recommendations

- One business recommendation from the results above is to take a look at the prices rides cost in rural cities. To increase the business in rural cities for rides, it might be beneficial to lower the price it cost per driver, to lower the average price per ride. If the price is lower per driver per ride, people might be more likely to use the PyBer ride-sharing app to get to places since it would be more afforable. 

- In addition, looking at the price per driver per ride in urban cities might be beneficial. Considering the high success urban cities have with riders, increasing the price per driver, increasing the average price per ride, could actually increase the total profit urban areas receive. The price per driver in urban cities is significantly lower than both rural and suburban cities. Therefore, increasing the price to where it wouldn't make a giantic difference could still keep the average number of riders while also increasing the total profit that urban cities are making. For example, in urban cities, the average price per driver is $0.67  . Just by increasing that that price slightly to $0.80  , would increase the average fare per ride for customers only slightly, while also increasing the total fare for urban cities. However, increasing the price too much in urban cities, could potentially impact the cities in a negative way. Suburban areas have an average price of $2.26 per driver. So if urban cities were to increase the price too much, they could potentially lose money overall. 

- Another recommendation is to gather data on the total number of people in each city type. Understanding why urban cities are doing significantly better than suburban and rural cities could be to other external factors. For example, if urban cities have a significantly higher number of people in their cities compared to suburban and rual cities, could be a factor in why urban cities do so well with the Pyber ride-sharing app. Another external factor to look at is the variety of public transportation each city type has. If a city type has multiple public transportation systems, it could be a reason for a decrease in the number of people who use the ride-sharing app. For example, if rural cities have buses for people to get from one place to another and it's cheaper to take the bus compared to utilizing the ride-sharing app, then PyBer might want to consider generating a more competitive price to get people more interested in using their app over taking the bus. 

- My final business recommendation would be to leave the price for the suburban cities and not make any changes to it at this time. Since the suburban cities do better than the rural cities, but less than the urban cities, the suburban area is a good constant to compare to. For example, if the urban cities were to increase their prices per driver per ride, close to the price of suburban cities, they are likely to decrease in their total fares. So they won't want to raise their prices constantly. Increasing their fares too often could eventually impact their number of riders, decreasing the total fares in urban cities. However, if the rural area were to decrease their prices per driver per ride closer to suburban city fares, they are likely to make additional fares. Decreasing their high fares could lead to an increase of riders, also increasing rural cities total fares. Any changes should be made gradually though, as drastic changes could result in a negative impact.