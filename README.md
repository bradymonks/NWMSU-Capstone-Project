# NWMSU-Capstone-Project

Walk through the AthleteDatabase.csv file with me as I perform analysis on it and look for distinct patterns.

## Overview

Using python analysis, I wanted to find where athletes are being produced among the three major sporting leagues in the United States - Major League Baseball, National Basketball Association, and National Football League. Performing EDA on the data and introducing a new metric, I was able to get quality results over an abundance of data.

## Exploratory Data Analysis

I started with the EDA.ipynb script as wanted to get a general idea of the data I was using. I was able to put together some insightful visuals that allowed an idea of the data set to be formed. My analysis included code from pandas, matplotlib, plotly, seaborn, and scipy. 

### Bar Charts

I started by looking at the league breakdown among Conference and Birth State. Using pyplot from matplotlib, I created some stacked bar charts. 

![Conference X League Breakdown](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/ConferenceLeague.png)

![State X League Breakdown](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/StateLeague.png)

### Contigency Tables

To transform these graphs to see the actual data, I created some contingency tables. I sorted them by actual athlete production so that the top producers are first. To create these, I used the crosstab function from pandas. 

![Conference X League Breakdown](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/ContTableConf.png)

![State X League Breakdown](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/ContTableState.png)

### Interactive Charts

Using plotly, I was able to create a neat interactive map of the U.S. that feels like I'm taking a deeper dive into the data. 

![Heat Map](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/HeatMap.png)

United States Heat Map

## Summary Statistics

I also used pandas to help me along with some summary statistics. I used the .describe() function to help me see the top frequencies for each sport among the "College" and "BirthPlace" features. 

![Summary Statistics](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/SummaryStatistics2.png)

## Chi-Squared

I also ran a Chi-Squared test on these three features - BirthPlace, College, Conference - with League to see what the association was like. All three features had indications that there was strong assiciation between each feature and League.

For BirthPlace, the statistic was 20,646 with a P-value of  5.77328e-169 and 15,284 Degrees of Freedom. 

Conference had a statistic of 1,122 and a P-value of  6.309067e-205 to go with 46 Degrees of Freedom.

To go with a statistic of 19,392 College had a P-value of 0 and 2,922 Degrees of Freedom. 

# New Score

In my NewScore.ipynb script, I wanted to introduce a new metric that would allow me to score/rank cities, colleges and combinations of both to help deduct the best options for each professional league. I only scored the features "College" and "BirthPlace". 

To start, I loaded the csv and wrote some code that grouped by League and College, giving me the total counts for each college in each league. I then added another column that took the total amount of athletes for each college in a specific league and divided it by the total amount of athletes in that league, giving me the percentage that that college made up of that league. From there I sorted the dataframe by League and Percentage and ranked by three the dataframe, giving me top rank for each league and going down. 

![Ranks & Percents](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/ranks_percents.png)

Then I filtered that dataframe to just give me all the schools that appeared in the top 10 of any league to be included for a graph. 

I have experience using ggplot in R to help put together faceted graphs and I know that can be imported into python so I used many imports from the plotnine package to help me achieve this. 

![Top 10 College](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/Top10College.png)

Red bars indicate that school is in the top 10 for that League, while gray bars indicate that school is in the top 10 for another sport, just not the one with the bar. 

## Final College Rankings

In order to achieve a final ranking for all the colleges, I needed get a pivot table that include a row for each college and had their ranking for each League. From there, I added another column that summed up the totals rankings to give me a score. Using principles from golf (lowest score wins), I then sorted the new summed column and ranked the schools from there. These new scores indicate which schools were near the top for everything, or possibly near the top for one or two and lacked in the other(s). 

![Final College Ranks](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/CollegeFinalRanks.png)

I performed the same transformation using the BirthPlace feature and got the following results. 

![Ranks & Percents - BirthPlace](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/ranks_percents_birthplace.png)


![Top 10 - BirthPlace](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/Top10BirthPlace.png)


![Final College Ranks](https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/Images/BirthPlaceFinalRanks.png)



# This repo will maintain the code and CSV file that I will be using alongside any extra files to be used. 