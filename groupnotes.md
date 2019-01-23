#----------------------------------------
#Lee Notes
#----------------------------------------

I think we should break data manipulation into three steps.

1) We should find the dates and locations for each desired disaster location.
    - Then we group by disaster type and set up DF for each of those data type.
    - Create CSV files to reference into a later data frame.

2)We need to find a database with the most complete data, and also the data should be organized by zip code in each row, and date for each column. 
    - Once we find the appropraite data set we need to clean null values.
    - Once we have the clean data we need to loop through to find month over month change.
    - Clean the data to remove null values.
    - Once data is clean, we save a csv for merging later. 


3) We should use the CSV files to do a loc function to isolate a desired zip code for each disaster. Then use a loop to reference data for 12 months before the event and 12 months after the event. 
    - We then merge the two data sets to only include the desired zip codes. 
    - We can find the 12 months before and after by finding the desired index value through a loop function, then using another loop to find column -12 to column +12. from the event date.
    - Once we have the data complided we construct a DF with a Column index showing all the data for months -12 to +12. We can then do analysis on the data. 
 test



Looks great, Lee!! - Diana
