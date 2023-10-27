# Call-Center-Analytics
Call center Analytics dashboard that reflects all relevant metrics and KPIs in the dataset
# Data Exploration:
-	The dataset consists of 1 table, 5000 rows, and 11 columns, each row represents a single inbound call, along with its details; Call ID, Agent, Date, Time, Topic, Answered(Y/N), Resolved(Y/N), Average talk duration in seconds, Average speed of answer in seconds, and Satisfaction rating.
-	The time range of the dataset is from 1st, Jan 2021 till 31st, Mar 2021. Operating daily from 9:00 a.m. to 6:00 p.m. 
-	There are 8 active agents and 5 different topics.
-	 Satisfaction rating is the received score from the customer which ranges from 1:5, where 1 is very dissatisfied, 5 is very satisfied, and 3 is neutral.
-	946 rows have missing values in Average talk duration, Speed of answer, and Satisfaction rating which are the abandoned calls.
-	There are no duplicated values in our dataset.
-	Speed of answer ranges from 10 seconds to 2 minutes and 5 seconds.
-	Average talk duration ranges from 30 seconds to 7 minutes.
# Data Preparation
-	To use the Average talk duration and the Speed of answer in hh: mm: ss format, first we will divide them by 24 hours, 60 minutes, and 60 seconds to result in a decimal number that represents the amount of time.
-	The next step is to import the data into Power BI, transforming the Average talk duration and the Speed of answer columns into duration Power Query, and 
-	In Power BI we will use Format function on the DAX measures that are used in the card visuals.
-	To extract the hour and the weekday of each call and to allow date hierarchical drilling in our visuals, we will create a dedicated date table using CALENDAR function.
-	We’ll use SWITCH function to create two new columns, the first column classifies
 the Satisfaction ratings into three categories: positive, neutral, and negative ratings, the second column transforms the Speed of answer into duration brackets (10 seconds each).
# Measures and KPIs: -
-	Total number of calls.
-	Total number of Answered calls - Total number of Abandoned calls.
-	Total number of Resolved calls - Total number of Unresolved calls.
-	Count of Positive Ratings - Count of Negative Ratings.
-	Call Abandonment Rate = Total number of Abandoned calls / Total number of calls.
-	Call Resolution = Total number of Resolved calls / Total number of Answered calls.
-	% of Positive Ratings = Count of Positive Ratings / Total number of Answered.
-	Average Call Duration.
-	Average Speed of answer.
-	Average calls per day.
-	Average Satisfaction score.
-	Service Limit: Calls answered in the first minute.
-	Longest Call Duration - Shortest Call Duration.
