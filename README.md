# MTA Turnstile Data Analysis

To reproduce my results, run the following in order:
1. benson_scraper
2. benson_cleaner
3. merge_weather (this script requires requesting a CSV file from the NOAA - follow steps below to get this file)
4. benson_viz
5. scheduler_tool_demo

**Note**: Each Jupyter notebook spits out a csv that feeds the next notebook
**Note**: There must be a ```./csv``` folder in your path to store data from the scraper

### Steps to obtain MY Weather CSV file:

1. Go to [https://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND](https://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND)
2. For field "Select Weather Observation Type" choose "Daily Summaries"
3. For field "Search For" choose "Stations"
4. Enter the query "Central Park" in the search box
5. Find **NY CITY CENTRAL PARK, NY US** in the list on the left with the following Station ID, GHCND:USW00094728. Click "ADD TO CART" next to the search result
6. Your cart (upper right) should now have one item--click the cart to view items in your cart
7. The next screen, "Select Cart Options," should present you with 3 options. Choose "Custom GHCN-Daily CSV" and make sure the date range goes back 3 years and press "Continue"
8. Under "Select data types for custom output" check the box for "Precipitation" and click "Continue"
9. Enter your email address and SUBMIT ORDER
10. You will receive an email with the CSV file. Rename this file to **NY_weather_summer.csv** and copy it to the root project directory.


