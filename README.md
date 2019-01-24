# data_bootcamp_project1

Team: Lee, Jordan, Diana

Project Description: Impact of natural disasters on housing prices.

Research Questions to Answer:
- What are the effects of the natural disasters on housing prices?
- Which natural disaster type has the most impact on housing prices?
- Which areas experence the those disaster types most frequently?
- How do those homes value compare to the rest of the US?
- Are there any factors that help or hinder recovery of housing prices?

Data Sets to be Used:
- FEMA Data Feeds (FEMA Web Disaster Summaries, Individual Assistance Housing Registrants Large Disasters, etc)
- Federal Reserve of St Louis
- Zillow API (multiple data sets available)
- Google or GeoFRED for mapping

Rough Break-down of Tasks:
- Import the data sets
- Cleanse
- Convert into format that allows for place and date
- Merge data sets
- Exploratory data analysis
- Create visualizations
- Consolidate findings
- Build Presentation


#PROCESS EXPLAINATION

Notebook Legend:

FEMA Data Clean
- This notebook takes data downloaded from FEMA
- It cleans the FEMA data by:
    - Deleting the irrelevant columns
    - Removes incomplete data sets
    - Renames columns to desired values
    - Sorts data so the begin date matches our Zillow data set.
    - Formats the county data so we can merge with Zillow.
    - Finds the top 6 disaster types, that have over 1,000 observations
	
Zillow Cleaner
- This notebook takes data downloaded from Zillow
- It cleans the Zillow data by:
    - Deleting the irrelevant columns
    - Setting the county data as the new index for the merge
    - Finds the Month over Month Change is Real Estate prices by Zip Code
- Saves the Data to CSV
- Finds the population average return for all zip codes
- Saves the Population data return to CSV

FEMA Zillow Merge
- This notebook takes all the cleaned data and merges it together
- Imports the FEMA and Zillow Data
- Merges the data together based on two contigentent vairables, "County Name" and "State"
- Verifies data integrity
- Saves the data to CSV

Normalized Data
- This Notebook converts all the raw data into useable information.
- It takes all the data and bins it to 1, 2, 3, 4, 5 and 6 months after the event for both the variable group, and the population group.
    - It takes the data and sorts it by event, county, then zip code.
    - Then it saves the new information into CSVs for charting later.
- Then it runs the statistical test on a desired data frame to determine if there is a statistical difference in medians.
- Finally, it converts these dataframes into index values and put into a list.
    -It saves the new indexed data frame into a CSV for charting later.

Charting
- This notebook takes all of the CSVs generated in the "Normalized Data" notebook
- It creates charts for each disaster type, and the indexed information.


