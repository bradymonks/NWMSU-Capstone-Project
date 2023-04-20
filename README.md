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

To start, I loaded the csv and 

# This repo will maintain the code and CSV file that I will be using alongside any extra files to be used. 