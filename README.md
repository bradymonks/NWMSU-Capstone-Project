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

Using plotly, I was able to create some neat interactive graphs that feel like I'm taking a deeper dive into the data. 

<iframe src="https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/athlete_bar_chart.html"></iframe>

Athlete Bar Chart

<iframe src="https://github.com/bradymonks/NWMSU-Capstone-Project/blob/main/athlete_map.html"></iframe>

United States Heat Map

# This repo will maintain the code and CSV file that I will be using alongside any extra files to be used. 