# Call-Center-Analytics
Welcome to our call center analysis dashboard for the first quarter of 2021. This comprehensive project aims to evaluate the performance of our agents during their operating hours and through time. By analyzing various metrics, we gain valuable insights into agent efficiency and customer satisfaction. The dashboard provides a detailed overview of key performance indicators such as call abandonment rate, call resolution, and service limit. With this information at hand, we can identify areas for improvement, optimize agent productivity, and enhance overall customer experience. Let's dive into the data and uncover opportunities to excel in our call center operations.
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
- To use the Average talk duration and the Speed of the answer in hh: mm: ss format, firstly, I divided them by 24 hours, 60 minutes, and 60 seconds to result in a decimal number representing the amount of time. The next step is transforming the Average talk duration and the Speed of answer columns into duration using Power Query, and then, using the Format function to the DAX measures that are used in the card visuals.
- I utilized the SWITCH function to create two new columns, the first column classifies the Satisfaction ratings into three categories: positive, neutral, and negative ratings, and the second column transforms the Speed of the answer into duration brackets (10 seconds each).
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
