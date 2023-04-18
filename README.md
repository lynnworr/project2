# Project 2

## Project Proposal

We are a new internet provider looking to expand to the global market. We will be examining different countries throughout the years to track the increase in internet use and where these increases thrive. We will compare this data to the global HDI (Human Development Index) as well to determine which country is the best fit for our new headquarters.


## Finding Data

In order to aquire our data, we used a few sources. This includes Kaggle, the Human Development Reports website, and World Bank website as well. Our sources comprise of excel files and csv files. 


## Project Report

*Extract*

We extracted our data using the Excel dataset from und.org and the csv dataset from kaggle.com. 

*Transform*

Once we read the data from the Human Development site, we were able to witness a steady increase in internet usage across the globe. We cleaned this data by selecting only the "Year" column equal to 2020 in order to narrow down our results and focus on a recent year of findings. We also dropped null or blank rows in the "Entity" column to minimize skewed results. After this was complete, we dropped the "Unamed:0" and "Year" columns to continue narrowing down our findings. So that data could be more easily interpreted, we renamed the "Entity" column to "Country".  

Next, we merged this data with the excel data found on Kaggle, and we cleaned it up by reordering the columns, and checking for any duplicates. We converted our dataframe to a list of dictionaries, and it was ready for the next step.

*Load*

Once our data was collected and transformed, we were able to load it into the non-relational database, MongoDB. We named our instance of MongoClient "mongo" and inserted our data (hdiTest) into a collection using .insert_many. We queried the collection with "results" equal to list(hdiTest.find()), and were able to successfully confirm that the data was loaded when seaching "for x in results".

### Sources:
* https://hdr.undp.org/data-center/human-development-index#/indicies/HDI
* https://www.kaggle.com/datasets/ashishraut64/internet-users




