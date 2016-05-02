# Section-02--Project-Group-5-DATA-MINING

##Providing API's to Explore Trending Topics, Discovering What People Are Talking About and More
===================================================================================================

### `OVERVIEW`

We are planning to use twitter data to retrieve the data from twitter using O'Auth authentication. And provide API's for users to explore the trending topics, discover what people are talking about etc. As part of this we are planning to do the following tasks.

      →API to find intersection between trends.
      →Collections of test results extracting text screen names and hashtags from tweets.
      →API for creating frequency distribution of words in tweets.
      →Collecting lexical diversity of tweets and API for it.
      →Generating histograms of words, screen names, and hashtags.
      →Generating a histogram of retweet counts and API for it.

We tried to look at trending topics in twitter and take up one topic and capture the pulse of the users. We planed to analyze the tweets of a trend and produce some information which is not apparent and can be extracted through data mining techniques.


### `DATA`

Using twitter data to retrieve the data from twitter using O'Auth authentication.

1. API for retrieving trends.
2. API to find intersection between trends 
3. Collections of test results.
4. Extracting text screen names and hashtags from tweets.
5. API for creating frequency distribution of words in tweets.
6. Collecting lexical diversity of tweets and API for it.
7. Generating histograms of words, screen names, and hashtags.
8. Generating a histogram of retweet counts AND API for it.

We used tweepy library to collect tweets. We used trends place API to pull the latest trends. We collected worldwide trending topics and topics trending in US. This data is stored in files worldTrends.json, usTrends.json.Then we found the intersection of the two. Out of the trends we selected the trending topic #NotGreatTVShows to do further analysis. (This topic might not be trending when we run the code again some time later).Then we collected tweets for hash tag #NotGreatTVShows using search API of tweepy.This data is stored in not-great-tv-shows-full.csv. We collected names of all TV shows from below link.
Wikipedia - https://en.wikipedia.org/wiki/List_of_American_television_series 


### `RESEARCH QUESTIONS`

To Explore Trending Topics, Discovering What People Are Talking About and More.
How social media impacts on people.

Tasks
       1. Creating a script to access twitter data from OAuth and providing an API for it.
       2. Retrieving data required for the above mentioned tasks.
       3. Creating API's where ever required so that users can use it.

### `MODELS AND ANALYSIS`

We are planning our models and preliminary analysis will be performed in a Jupyter Notebook and development in python.
We tried the shows which were repeated the most in tweets with hashtag #NotGreatTVShows.For this we had to have a counter (used counter in collections) for the TV show name. Then we used ngrams to find and found the most repeated ngrams in the tweets. From around 13k tweets we found the most repeated 50 ngrams we selected ngrams size of 4.We have tried with 1, 2, 3, & 5 and found 4 gives better results. But after we extracted the ngrams it did not correspond to actual TV show name. For example as we used ngrams size of 4 'So You Think You Dance' TV show was mentioned as 'So You Think You' in most of the tweets they mentioned the shows with funny names. For example "It's Always Sunny in Philadelphia" is mentioned as Always Raining in Philadelphia. So we had to map these ngrams with correct TV show names. For that we collected as many TV show names as possible from below link.
Wikipedia - https://en.wikipedia.org/wiki/List_of_American_television_series
we stored this data in tvshows.csv .Then we used Sequence Matcher of diff lib to find the most similar tv show for a particular ngram.We used the similarity ratio of .65 . We experimented with multiple values for similarity ratio from .5 to 0.9 and arrived at this number for better results. Finally we displayed the most tweeted shows in the hashtag #NotGreatTVShows

 
### `CODE AND APPLICATION`

Will post the code in our GitHub repository and instructions on installation are in the README.md file at the root level.

### `PROJECT MANAGEMENT`

We are team of five, SaiRaj Nagula, Bharadwaj Mateti, Surya Kiran Yelagam, Arunkumar Bonthala, Kamal Nayan Raju Kanchanapalli.we will be sharing our work among ourselves. SaiRaj will be taking care of development, data analysis. Arunkumar and surya are taking back end work consisted of an API that was created to provide data to the front end. And Writing O Auth script to pull linked in Connections and Bharadwaj and kamal would work on data set, data analysis and UI development and together we are collaborating to check the progress of the project testing and documentation. 


## `PROJECT TEAM, DELIVERABLES AND CHECKPOINTS`
===============================================================================

####`TEAM`

| Team member | Roles and skills | Contributions |
|-------------|-------------------------|---------------------------------------------|
| SaiRaj(0603) | Data analysis, Testing |data analysis, Testing, Build scripts |
| SuryaKiran(0650) | Web API, Data analysis, Python |  Data analysis, Python |
| ArunKumar(0843) | Web API, Data analysis, Python |  Data analysis, Python |
| Bharadwaj(0614)| Testing, Data analysis | Data analysis, Test harness; |
| Kamal Nayan(0266)| Testing, Data analysis | Data analysis, Test harness; |

### `DELIVERABLES AND CHECKPOINTS`
====================================================================================

| Checkpoint date | Expected Deliverable                                                          | Responsible team member(s) | Checkpoint results                                                                                                                  |
|---------------|-------------------------------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 2/15/16 | Collected data and analysed it.| All Team Members.| Check Point 1 Completed.|
| 3/08/16 | creating a streaming script which collects data from twitter because twitter has a limit on number of requests people make per day.We are Writing a script to collect the trends in twitter data and aslo Writing a script to pull in all the tweets of each trend. | sairaj,surya,arun | developed an algorithm for performing analysis on tweets to see how many of them are psitive,negtive and neutral. |
| 4/15/16 |  Managed to pull the data from the tweets through the twitter API and also pulled the data from tweets on deadpool movie through the twitter API.|sairaj,surya kiran,arunkumar | projected our prelimenary results of trending topics on twitter . |
| 4/18/16 | completed data segregation and using python libraries json for parsing the data and pandas for manipulation of data.| sairaj,bharadwaj,kamal |projected our prelimenary results of trending topics on twitter .|
|4/25/2016| we have completed implementing matplotlib for creating charts showing twitter trends and we are in a process of testing our final results.| sairaj, Surya Kiran, arun kumar| Created charts showing twitter trends.|
| 5/01/16 | added code and data files and submitted the documentation copy | sairaj,bharadwaj | We could find the Tv shows which were mentioned most using hashtag #NotGreatTVShows and also displayed the number of tweets that the show has recieved.|

### `REFERENCES`

→ https://en.wikipedia.org/wiki/List_of_American_television_series 
