# Surfs_Up
SQLLite, Alchemy, Flask, Jupyter, Python

# Overview
This analysis reviews weather data from stations across Oahu, HI, between 2010 and 2017.  The analysis is being used to determine the viability of opening a storefront dedicated to surfing products and icecream.  The investors want to determine if the weather reported through the year is conducive to icecream sales without significant swings due to cold weather.  Using SQLITE, a database table representing the weather data from local weather stations will be queried and analyize using SQLAlchemy in a Jupyter notebook utilizing Python and Pandas. Data will be presented for both June and December.

# Results
Weather stations collected data throughout the year.  June data tabulated to 1700 records and December tabluated 1517 records over a seven year period. 
- June Data
  - Average Temperature : 74.9
  - Max Temperature : 85.0
  - Min Temperature : 64.0
  - Standard Deviation from the Average temperature : 3.26


![June Statistics](https://user-images.githubusercontent.com/79231355/117584513-16151300-b0d3-11eb-842f-b9eeb26d38f7.png)


  
- December Data
  - Average Temperature : 71.0
  - Max Temperature : 83.0
  - Min Temperature : 56.0
  - Standard Deviation from the Average temperature : 3.75

![December Statistics](https://user-images.githubusercontent.com/79231355/117584523-1d3c2100-b0d3-11eb-8e0e-7b93289aade0.png)







# Summary
At the time of collection for this database, the December records had not been observed, resulting in fewer entries for that month.  The temperature across the year is very stable.  June shows a mean observed temperature of 74.9 with December showing 71.0.  The standard deviation from the mean is 3.2 for June and 3.7 in December.  This statistic indicates the variance from the mean on any given day averages this value.  Put another way, the average range in observed temperature for June is 71.65 to 78.15.  For December, the average range is 67.29 to 74.79.  December has a larger swing in observed temperatures as indicated by the max and min shown in the statistical analysis.  This indicates that december may have fewer days where icecream and surfing products may be in demand.  
The analysis would be improved if the time of observation were shown in the database table.  There are days where no data was recorded on nearly all station locations.  Some have mutliple missed entries, idicating a standard operating procedure for entry of these observation was not in place.  The observed temperatures could be from anytime during the day.  Additionally, the elevation of the stations is not included in the table.  With the large volcanic mountains on the island, the higher the elevation, the cooler the ovserved temperature would be.  Adding a filter, such as filter(Measurement.station == 'USC00519281') to the session query in the code would allow filtering out weather stations not at or near sea level, if the information on location of the stations could be aquired. Reviewing the number of records from each station is helpful to determine which station may have poor data.  
![All stations](https://user-images.githubusercontent.com/79231355/117584868-f2eb6300-b0d4-11eb-9596-aac0c698c622.png)
Filtering out the 2 lowest may provide additional insight into observed values, and the averages. Using a filter such as the following, the result is a lowered average temperature for June, a higher min temperature observed.  The difference is small, but should be valuable for the analysis.


![station filter](https://user-images.githubusercontent.com/79231355/117584976-9ccaef80-b0d5-11eb-83b5-7defb7444bac.png)

New June Statistics


![Adjusted June Statistics](https://user-images.githubusercontent.com/79231355/117584996-b53b0a00-b0d5-11eb-8b60-ec50f6a5102d.png)






