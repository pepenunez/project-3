# Data Visualizations with Tableau: Waves Report - Queensland

## File Structure

/data: contains the original files exported from data.gov.au/ organizad in folders by locations. It also contains 4 "clean files" (1 per each location) and "Queensland_waves_v2" with all the data aggregated. 
/Data-cleaning.ipynb: Jupyter notebook file where I import, manipulate and clean the data to be exported. 
/.gitignore: that contains Python's default configuration. 
/tableau_visualizations: link to tableau public

## Data
Source: https://data.gov.au/
Locations: Brisbane, Gold Coast & Townsville. 
Timeframe: 2017 - 2019

## Metadata

**Date/Time** - Date and time | Type = datetime
    Date and Time of data record, recorded in Australian Eastern Standard Time (AEST).

**Hs** - Significant Wave Height | Type = number
    Hs is the significant wave height or Hsig. It's the defined as the average of the highest one-third of wave heights in a wave record. This wave height closely approximates the value a person would see.

**Hmax** - Highest Single Wave | Type = number
    The height of the the highest single wave in a wave record.

**Tz** - Zero Up-Crossing Wave Period | Type = number
    The average of the zero up crossing wave periods in a wave record.

**Tp** - Wave Period | Type = number
    The wave period of those waves that are producing the most energy in a wave record.

**Dir_Tp** TRUE - Wave Direction | Type = number
    The direction that the peak waves are coming from, shown in degrees from true north.

**SST** - Sea Surface Temperature | Type = number
    The sea surface temperature at the wave monitoring buoy, in degrees Celsius.
    
## Process

### 0. Finding the data

Surfing is one of my favorite sports and hobbies. I like to practice it as much as I can and I wanted to analyse which where the best sports to go along the East Coast of Australia. Doing some research I found available information in https://data.gov.au/. I choosed 3 different location and downloaded information of 2017, 2018 and 2019. 

### 1. Data cleaning + preparation

- Created Dics with new columns info: location name, latitude and longitude. 
- Created unique dataframes per each location. 
- Concatenated them into one single DataFrame. 
- The source data contained NULL values as -99.0. I searched all the values and replaced them for NULL. 

### 2. Exporting tha data

While exporting the data I had some difficulties with the format of the dates. I found out that the original files had different formats for the date column. So, in order to solve it I unified the data type of the files that I imported in order to be able to concat them successfully.  

### 3. Tableau - Set up 

- Assure that the data types are correct and that the data doesn't have any incoherences. 

### 4. Tableau - Analysis

- I performed some basic visualizations with the purpose of data discovery. Those visualizations can be found in the "Basic" section in color "Teal". That was very useful to detect the main patterns and determine more complex analysis. 
- In the "Advance" section we can find some more in depth visualizations. 
- In the "Absolute" section we can find the graphs that I will use for the dashboard.
- *Dashboard*: the purpose of this dashboard is to enable the users to filter by location and dates and understand the basic conditions of the waves. 

## Main findings and conclusions

- Brisbane and Gold Coast seem better spots for surfing than Townsville. 
- We can find bigger waves in Brisbane than in the Gold Coast. 
- There is a positive correlation between the Period of the wave and the height of it. 


