# tableau-challenge
Week 20 Homework

## Citibike Analysis








## Repository Structure
### FOLDER: RawData
- Contains all the csv files from Jan 2019 to April 2021

### FILE: citibikes.ipynb
- Contains the jupyter notebook which performs ETL; extracts the data from the RawData folder, concatenates the data using the pandas library, performs transformation on the data (adding a day column) and loads the dataframe into a csv file.

### citibikes.twb
- Contains the tableau file which extracts the 1 csv file (as produced from the citibikes.ipynb file), and displays the multiple sheets, dashboards and story.
