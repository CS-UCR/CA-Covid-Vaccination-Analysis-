# Project Name:- Covid Vaccine Data California Counties

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
#### BEFORE RENAME:
![Before Rename](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Before.PNG?raw=true "Before Rename")
#### AFTER RENAME:
![After Rename](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/After.PNG?raw=true)

2.) In our data set there were rows that contained data for counties that were not part of California. Those rows includes "Outside California", "Unknown" and "All CA and non-CA Counties. 

3.) There was a column named "california_flag" to show that which county belongs to the California. We did not need that since we already removed all the non-California counties from our dataset. This means went from 15314 rows to 14573 rows in total. And then we printed them to display the final dataset. 
#### AFTER DROPPING COLUMNS:
![AFTER DROPPING COLUMNS](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/After%20dropping.PNG?raw=true)

4.) Later on in the notebook we created a subset of the data that only looks at the month of August 2021 which has the most recent vaccine data. We did some webscrapping to add a population column to the data set so we can make more comparisons. The data that we scrapped needed some cleaning so we could make it useable with our existing dataframe. 

### Data Visualization:-

1.) First, we are graphing a time series analysis for certain dates of three vaccines Pfizer, Moderna and Janssen doses taken. It starts from 2020-12-15 spanning to 2021-05-30. 
Blue graph shows the Pfizer doses. We see the pick during the the 2020 and it slows down and there is a slight pick between february 2021 to April 2021. Orange graph shows the 
Moderna doses and green graph shows the Janssen doses. Graph for this two vaccines are little similar to Pfizer and Moderna as well. 
#### Summary of doses taken by dates 3 vaccines ( More details later..)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Doses%20on%20Date.PNG?raw=true)

2.) Second, we have done pie chart comparasion with Riverside County and Los Angeleous county to see how many people are fully vaccinated in both counties regardless of which 
vaccine people have taken. We see that in Los Angeles county there are more people who are fully vaccinated compare to Riverside County. This graph does not account the population
of both counties though. 
### Riverside + Los Angeles Comparasion Of Vaccination
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Riverside-LA.PNG?raw=true)

3.) Third, we are plotting a bar graph where we are finding the mean of Pfizer, Moderna and Janssen does and then comparing which vaccine people are prefering to take in Rierside, 
Los Angeleous, Orange and San Diego counties. From the graph we see that in all counties Pfizer vaccine dominates the other vaccine. Moderna comes second and Janssen stays third choice for the people. 
### Comparing Prefered Vaccine Of Four Counties
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Prefered%20Vaccine.PNG?raw=true)

4.) Fourth, we are visualizing total number of Pfizer, Moderna and Janssen does people have taken on each day. This is basically more detailed version of what we did in the first step. Here we see that in December 2020 very less doses were taken and as the day passed people started getting vaccinated in 2021. Similar to last step Pfizer leads other vaccine in terms of total doses taken. Then, we are also graphing how many people became fully vaccinated and partially vaccinated on each day. It can be seen that during the december 2020, most of the people received the first dose of the vaccine. This is why we do not see the graph of fully vaccinated. But as the day passes we see the fully vaccinated graphs showing up. 
### Number of PFIZER, MODERNA, JANSSEN doses (December 2020 - August 2021)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%201.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%202.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%203.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%204.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%205.PNG?raw=true)
### Fully Vaccinated vs Partially Vaccinated (December 2020 - August 2021)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%206.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%207.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Date%20Analysis%208.PNG?raw=true)

5.) Fifth, we limited our dataset to only with the August 2021 to see which county has the higest number of people vaccinated. We see the high bar in Los Angeles County and on the second graph we see more counties getting fully vaccinated. Then, we do the same by checking how many people are partially vaccinated. Then we have done similar with the data from December 2020. This was very early stage in vaccination so as we can see we do not have any graph to visualize as very few people were fully vaccinated.
### Data for August 2021 only
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Number%20of%20fully%20vaccinated.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Number%20of%20fully%20vaccinated%202.PNG?raw=true)
### Data for December 2020 only
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/December%20Fully.PNG?raw=true)

6.) This part also goes along with data cleaning, where we scrapped the data in order to add the population column in our dataset. In the graph we see the list of counties by population and number of people are fully vaccinated. We do the same to see how many people are partially vaccinated.
### Adding Population Column
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Population%20Column.PNG?raw=true)
### Population vs Number of people fully vaccinated + Partially Vaccinated
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Population%20Fully%20Vaccination.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Population%20Fully%20Vaccination%202.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Population%20Partially%20Vaccination.PNG?raw=true)
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Population%20Partially%20Vaccination-2.PNG?raw=true)

7.) Lastly, we are zooming in the above graphs. For example, first we took the four counties with higest population ( Los Angeles, Riverside, Orange, San Diego ) to see how they compare with fully vaccinated as well as total partially vaccinated. And we are doing the same with the counties that are least populated. 
### Checking Vaccination Status (Fully Vaccinated) in counties with higest population
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Higest%20Population%20Fully%20Vaccinated.PNG?raw=true)
### Checking Vaccination Status (Partially Vaccinated) in counties with higest population
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Higest%20Population%20Partially%20Vaccinated.PNG?raw=true)
### Checking Vaccination Status (Fully Vaccinated) in counties with least population
![](https://github.com/CS-UCR/final-project-covidvaccineca/blob/main/Project%20Screenshots/Less%20Population%20Fully.PNG?raw=true)
