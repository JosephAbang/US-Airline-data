# Data Expo 2009: Airline on time data
## by Joseph Abang


## Dataset
Every commercial flight within the United States between October 1987 and April 2008 is represented by arrival and departure data.I used a sample of 200,000 records from each year between 1987 and 2008 of the dataset already on Kaggle that can be found here (https://www.kaggle.com/datasets/wenxingdi/data-expo-2009-airline-on-time-data), this is the dataset used in the first notebook (exploratory-analysis). <br>
I also uploaded the wrangled dataset, this is the dataset uploaded in the second notebook (explanatory-analysis). I removed unused columns, deleted duplicates, and dropped null values during the wrangling process. Additionally, I added new columns (dummy variables) to facilitate exploration and performed transformations (merging, changing data types) on a few columns. The clean and dataset spans the years 1995 to 2008 and includes 11 columns and 2,730,250 values.
### Variables 
* Origin (object)
* Destination (object)
* Unique Carrier (object)
* Distance (float, Miles) 
* Date (datetime)
* AirTime (float, minutes)
* Late_Arr (int, dummy)
* Late_Dep (int, dummy)
* ElapsedTime_percnt_error (float, percentage)
* Is_Weekend (int, dummy)
* flight_length (object)



## Summary of Findings

#### Carrier Information

- Popular carriers according to frequency: 
* Least popular: 9 Air (AQ)
* Most popular: Southwest Airlines (WN)

- 3 most popular destinations and origins are;
    * Orchard Field Airport (ORD)
    * Atlanta Airport (ATL)
    * Dallas/Fort Worth airport (DFW)
> A pattern exists where most of the popular destinations are the same as origins which suggests that most flights are return flights. 

- The **most popular carriers** according to flight lengths are:
    * Short haul flights - Southwest airlines (WN)
    * Medium haul flights - American airlines (AA)
    * Long haul flights - American airlines (AA)

#### Flight information
- **Annual flights** counts spiked in 2002 and created a modal peak between 1995 - 2008. The year with the least number of flights is 2001. This is the same year that the 9/11 attacks happened. **Weekly flights** show a steady number of flights during weekdays (Monday-Friday) and a slight decrease in the number of flights on weekends.
**Daily flights** reveal that flight demand decreases significantly in the last few days of the month.

- The greatest amount of flights are short haul flights (1,653,329 counts) followed by medium haul flights ( 1,073,085 counts) and then Long haul flights (3,836 counts). The carriers mostly go on short and medium haul flights.

- Most medium haul flights are between 800 miles to 1200 miles and 3700 miles to 4200 miles for long haul flights.

#### Percentages
* Arrivals
    * Late - 21.3%
    * Ontime - 78.7%

* Departures
    * Late - 17.7%
    * Ontime - 82.3%

* Weekend flights (%): 26.8%
* Weekday flights (%): 73.2%

#### Weekday(s) with highest amount of arrivals/departures;
* On-Time - Mondays, Tuesdays and Wednesdays
* Late - Thursdays and Fridays

#### Day(s) with highest percentage of arrivals/departures;
*  Late - 14th - 23rd, 26th, 27th and 28th

> In comparison to on-time arrivals, late arrivals have a marginally higher airtime value. There are many potential causes for this, including the weather or technical difficulties. Airtime should therefore be taken into account when there are delays in arrival.

> There was a significant correlation between distance and airtime. The longer the carrier is in the air, the further the destination is; **airtime increases as distance increases.**



## Key Insights for Presentation

##### Flight information
**Weekly flights** show a steady number of flights during weekdays (Monday-Friday) and a slight decrease in the number of flights on weekends.
**Daily flights** reveal that flight demand decreases significantly in the last few days of the month.

#### Percentages
* Arrivals
    * Late - 21.3%
    * Ontime - 78.7%

##### What day of the week is best to fly and arrive on-time?
* On-Time - Mondays, Tuesdays and Wednesdays

#### Carrier Information
Popular carriers according to frequency: 
* Least popular: 9 Air (AQ)
* Most popular: Southwest Airlines (WN)

##### Which airport is most known for short, medium and long flights?
* Short haul flights - Southwest airlines (WN)
* Medium haul flights - American airlines (AA)
* Long haul flights - American airlines (AA)

> There was a significant correlation between distance and airtime. The longer the carrier is in the air, the further the destination is; **airtime increases as distance increases.**

> In comparison to on-time arrivals, late arrivals have a marginally higher airtime value. There are many potential causes for this, including the weather or technical difficulties. Airtime should therefore be taken into account when there are delays in arrival.

#### Code modifications
* I increased the figure sizes for better presentation hence also increasing the titles and labels.
* I used 'symlog' instead of 'log' for better visualization.
* I seperated a subplot into individual plots as sub-slides for a slide.
* I included a function that adds scale labels, titles and font sizes to plots.