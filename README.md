# tableau-challenge
Week 20 Homework
---------------------------
## Citibike Analysis
The Citibike analysis includes data from 2019, 2020 and up to April 2021. There are a total number of 1,596,518 total bike visitors throughout this period (whereby 1 bike visitor is equivalent to a tag on or tag off at a Citibike station.)

There are 3 dashboards created in the analysis:
- Busiest Stations: When and Where?
- Busiest Day and Time
- Citibike Popularity by Gender

On each dashboard, there are common filters for user interaction. These are the year and the months of the year. 
For example, the user may click on 2020 and June. The graphs and total bike visitors card value would update to reflect that specific month and year's data.

On the two dashboards; Busiest Day and Time and Citibike Popularity by Gender, users are able to also filter the data further by clicking on either Weekdays or Weekend to find trends of interest. Alternatively, the user is able to click on a particular day of the week to return only results of that day for visualisation results over the entire dashboard.

On the one dashboard Citibike Popularty by Gender, users are able to filter for the specific gender to view the number of female or male tagging on/off at stations, as well the popularity use of the bikes by time (year, month, weekdays, weekends, hourly).

### Busiest Stations: When and Where?
This dashboard incorporates a map visualisation whereby each bubble represents a Citibike station. The size of the bubble indicates the number of bike visitors such that the greater the number of visitors, the bigger the bubble. The colour intensity of the shaded bubbles indicate the average trip duration from the station.

The 3 most popular stations (using full dataset) are as per order:
- Grove St PATH (146, 434 visits)
- Hamilton Park (82,788 visits)
- Sip Ave (70,626 visits)

In 2019, the 3 most popular stations are as per order:
- Grove St PATH ( 93,324 visits)
- Hamilton Park (48212 visits)
- Sip Ave (38,170 visits)

In 2020, the 3 most popular stations are as per order: 
- Grove St PATH ( 45,860 visits)
- Newport Pkway (39,688 visits)
- Liberty Light Rail (33,866 visits)

Grove St PATH is easily always the most popular station without competition, with a significant gap of visitors before the 2nd most popular station, year after year (2019, 2020, 2021). 

#### Unexpected Findings: Phenomena is that there are fewer people on Citibikes but longer durations on them.
There are significantly less people between year 2019 and 2020 on Citibikes based on the tag on/tag off count at stations. 
- 2019: 809,894 station counts
- 2020: 673,604 station counts

Interestingly, the trip duration at Grove St PATH (whether it is the start point or end point of the trip) are generally short (~10 minutes if all data from 2019 to 2021 is taken into consideration). However, a stations such as Liberty Light Rail, located slightly further away from Colgate Center and also less visitor count, have a much higher average trip duration of 46 minutes. 

In terms of comparing trip durations, it appears that there is a significant difference between 2019 and 2020. 2021 (without the full year's data set) is showing similarities to 2020 in terms of trip duration.
Take Grove St PATH for example, which has an average trip duration of 7.7 minutes in 2019, 15.4 minutes in 2020 and 14.3 minutes in 2021. 
The trip duration has doubled from 2019 to 2020. (This trend is also common amongst other stations.)

### Busiest Day and Time
This dashboard clearly shows the days of the week vs number of bike visitors as well as the hours in a day vs number of bike visitors. 

#### Unexpected Findings: Phenomena is that there are evidently 'quiet Mondays' on the bikes, peak hour at 10pm in 2021, a shift towards 'popular Saturdays' on bikes in 2020 and 2021.
As a wild guess, before any analysis has taken place, I would assume that weekdays would yield the highest number of bike visitors across all stations compared to weekends. 

This trend is true for 2019 With weekdays varying from 118,986 to 129,714 visitors each day and weekends dropping from 84,374 to 99,590 visitors. 
However, in 2020, weekends were more popular; weekdays vary from 85,396 to 92573 visitors and weekends at 104,372 to 114,122 visitors. 

Furthermore, year after year, Mondays seem to always be the quietest weekday on bikes. In 2019, Tuesday was the busiest weekday at 129,714 visitors and Monday, the quietest weekday at 118,986 visitors. Tuesday and Wednesdays tend to always be the busiest weekdays for Citibike goers. 

In 2019 and 2020, the number of bike visitors have noticeable peaks at 8am and 6pm. However, in 2021, peak hour is 10pm at night, with a gradual trend increase from 5am in the morning. 

### Citibike Popularity by Gender
The dashboard illustrates the proportion of bike riders by gender. Additionally, the number of female and male riders on each day of the week as well as by the hour on a 24 hour cycle. 

#### Unexpected Finding: Phenomena is that significantly more males are using Citibikes than females.
There are about 3 times more males than female using Citibikes. Overall (all data taken into account), there are 994,058 males, 361,004 females and 241,456 unknowns. This trend is also evident across each individual years; 2019, 2020 and 2021. Unfortunately, more and more proportion of people over the years have chosen to be classified 'unknown' as opposed to revealing their true gender for the analysis. This could potentially skew the data and disprove the theory that more males than females are on the bikes (especially in 2021 where there were significantly more 'unknown' than each of the genders). 

The busiest hour for male and female are both at 5-6pm which is expected (end of a work day when people are commuting from offices). However, the 'unknown' category's peak hour is at 10pm. The proportion of unknowns is so much larger than the male and female category that it has placed the overall 2021 peak hour at 10pm (as also summarised in the previous dashboard). 

----------------------------
## Repository Structure
### FOLDER: RawData
- Contains all the csv files from Jan 2019 to April 2021

### FILE: citibikes.ipynb
- Contains the jupyter notebook which performs ETL; extracts the data from the RawData folder, concatenates the data using the pandas library, performs transformation on the data (adding a day column) and loads the dataframe into a csv file. (Note that this combined data csv file is not on this repo due to size restrictions on github. To attain the file, run citbikes.ipynb)

### FILE: citibikes.twb
- Contains the Tableau file which extracts the 1 csv file (as produced from the citibikes.ipynb file), and displays the multiple sheets, dashboards and story.
* Also available on Tableau online: https://prod-apsoutheast-a.online.tableau.com/#/site/newyorkcitibikeswithannabel/workbooks/45034?:origin=card_share_link
