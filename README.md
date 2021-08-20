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
1.) We have renamed all the rows in order to properly differentiate the names. For example, changing counties to California Counties, pfizer_doses to PFIZER and etc.\
2.) In our data set there were rows that contained data for counties that were not part of California. Those rows includes "Outside California", "Unknown" and "All CA and non-CA Counties. \
3.) Finally, there was a column named "california_flag" to show that which county belongs to the California. We did not need that since we already removed all the non-California countises from our dataset. This means went from 15314 rows to 14573 rows in total. And then we printed them to display the final dataset. 


