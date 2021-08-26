# Project Name:- Covid Vaccine Data California 

### Overview:- As California begins opening up it becomes important to learn about how many people have been vaccinated in different counties in California. This dataset contains the report of vaccination status by different counties.
We will extract and analyze this information in our project. 

### Extract:- Below are all the things that will be extracted from this data in our project. 
Total doses given at specific date \
Number of pfizer doses given \
Number of moderna doses given \
Number of JJ does given \
Number of people fully vaccinated \
Number of people partially vaccinated \
At least one dose \
Chart showing vaccination and cases correlation 

### Process:-
First, we will import the latest csv file into jupyter notebook and start the data cleaning process.
There are certain columns that we will not need like California flag status so we will drop that. Also, certain rows include the data from non CA counties as well, 
so we will get rid of that as well. We also merge any relevant data from both data sets into one data frame. We are thinking of displaying the above 
results by finding mean and standard deviation and then represent them visually. We can work with the data more once we start the process. 

### Data Cleaning:-
1.) We have renamed all the rows in order to properly differentiate the names. For example, changing counties to California Counties, pfizer_doses to PFIZER, moderna_doses to MODERNA and jj_doses to JANSSEN and etc.

2.) In our data set there were rows that contained data for counties that were not part of California. Those rows includes "Outside California", "Unknown" and "All CA and non-CA Counties. 

3.) There was a column named "california_flag" to show that which county belongs to the California. We did not need that since we already removed all the non-California counties from our dataset. This means went from 15314 rows to 14573 rows in total. And then we printed them to display the final dataset. 

4.) Later on in the notebook we created a subset of the data that only looks at the month of August 2021 which has the most recent vaccine data. We did some webscrapping to add a population column to the data set so we can make more comparisons. The data that we scrapped needed some cleaning so we could make it useable with our existing dataframe. 

### Data Visualization:-

1.) First, we are graphing a time series analysis for certain dates of three vaccines Pfizer, Moderna and Janssen doses taken. It starts from 2020-12-15 spanning to 2021-05-30. 
Blue graph shows the Pfizer doses. We see the pick during the the 2020 and it slows down and there is a slight pick between february 2021 to April 2021. Orange graph shows the 
Moderna doses and green graph shows the Janssen doses. Grpah for this two vaccines are little similar to Pfizer and Moderna as well. 

2.) Second, we have done pie chart comparasion with Riverside County and Los Angeleous county to see how many people are fully vaccinated in both counties regardless of which 
vaccine people have taken. We see that in Los Angeles county there are more people who are fully vaccinated compare to Riverside County. This graph does not account the population
of both counties though. 

3.) Third, we are plotting a bar graph where we are finding the mean of Pfizer, Moderna and Janssen does and then comparing which vaccine people are prefering to take in Rierside, 
Los Angeleous, Orange and San Diego counties. From the graph we see that in all counties Pfizer vaccine dominates the other vaccine. Moderna comes second and Janssen stays third choice for the people. 

4.) Fourth, we are visualizing total number of Pfizer, Moderna and Janssen does people have taken on each day. This is basically more detailed version of what we did in the first step. Here we see that in December 2020 very less doses were taken and as the day passed people started getting vaccinated in 2021. Similar to last step Pfizer leads other vaccine in terms of total doses taken. Then, we are also graphing how many people became fully vaccinated and partially vaccinated on each day. It can be seen that during the december 2020, most of the people received the first dose of the vaccine. This is why we do not see the graph of fully vaccinated. But as the day passes we see the fully vaccinated graphs showing up. 

5.) Fifth, we limited our dataset to only with the August 2021 to see which county has the higest number of people vaccinated. We see the high bar in Los Angeles County and on the second graph we see more counties getting fully vaccinated. Then, we do the same by checking how many people are partially vaccinated. 
