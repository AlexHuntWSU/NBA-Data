# NBA-Data

Big Question: With this project, I wanted to find out if a home court advantage in basketball actually exists and if so, what stats such as FT and 3P percentages are most effected. In my analysis, I also looked over offensive and defensive ratings to find out which is better for winning.

Data Process: My data for this project comes from the NBA website and was collect by manual data entry into Excel as there was no option to save the data as a csv file. The [NBA Stats](https://www.nba.com/stats/) database is very comprehensive but I only needed the win percentage (win%), free throw percentage (FT%), field goal percentage (FG%), 3 point percentage (3P%), and offensive and defensive ratings for both home and away games. With only 30 teams and one season, manual input was manageable. However, if I wanted to extend my analysis over multiple seasons and additional statistics, I would need to incorporate data mining or find another data source.

Upon importing the dataset into R, I realized that it needed to be in a different format to create the boxplots. I started off by melting the data in long format so every row is a single observation using the library package "reshape2". After this, I created a new column called "Location" to add either "Away" or "Home". I started by making all the values "Away" then using a loop to change the rows with a home value such as "HomeFT" or "Home3P" to "Home". Now that I had the location column created, I needed the variables to lose their location identifier. Because the loop did not work in changing these values, I had to export it into excel and manually change the names. After that, the dataset was imported into R and a boxplot was created using ggplot2 and the facet wrap feature. 

Data Sources:

[Home Traditional Stats](https://www.nba.com/stats/teams/traditional/?sort=W_PCT&dir=-1&Season=2021-22&SeasonType=Regular%20Season&Location=Home)

[Away Traditional Stats](https://www.nba.com/stats/teams/traditional/?sort=W_PCT&dir=-1&Season=2021-22&SeasonType=Regular%20Season&Location=Road)

[Home Ratings](https://www.nba.com/stats/teams/advanced/?sort=W&dir=-1&Season=2021-22&SeasonType=Regular%20Season&Location=Home)

[Away Ratings](https://www.nba.com/stats/teams/advanced/?sort=W&dir=-1&Season=2021-22&SeasonType=Regular%20Season&Location=Road)

![Boxplot](Boxplots.png)


