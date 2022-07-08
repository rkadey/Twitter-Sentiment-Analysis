# Twitter-Sentiment-Analysis
## Introduction
Prior to winning the seat of goverment in 2016, the then Presidential Candidate in the person of Nana Akuffo-Addo for the New Patriotic Party (NPP) made a promise to build a Cathedral to honor God should he be voted by Ghanaians as their president. Fast forward to 2022, the goverment of Ghana under the leadership of His Excellency has generated a lot of debate online with the execution of the National Cathedral.

This project seeks to analyse the sentiments of twitter users on the building of the National Cathedral.

## Project Strategy
![image](https://github.com/rkadey/Twitter-Sentiment-Analysis/blob/main/Twitter%20Analysis%20Project%20Breakdown%20Infographics.png?raw=true)



### Data Mining
Our data for the project was mined from twitter with a sample size of 50,000 tweets. Python library snscrape.modules was imported to help with the mining. I queried tweets of Nationa Cathedral from 01 January 2018 to 07 July 2022. The data was loaded into my jupyter notebook and stored in a pandas dataframe named Data.

### Data Cleaning
The tweets in its raw state involved a lot of symbols, pictograghs, flags, emojis and links as well as transport and map symbols. This were removed by creating cleanText function and applying it to the Data. Retweets were also removed to avoid duplicate of data.

A check on the location column of our data reveals missing values. Those missing values were replcaed with 'NaN' and later changed to 'No location'. We define our custom Stop words ['ng', 'gh', 'GHC', 'million', 'RF', 'National', 'Cathedral', 'secretariat'] and added it to the default English Stop words [words that are unimportant like 'is, 'and' etc.] and alphabelts. This is to help our model concentrate on more important words for our analysis.
