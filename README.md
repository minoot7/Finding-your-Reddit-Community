### Using Reddit's API for predicting Posts
>
> *Problem Statement:* Is it possible to create a classifier to predict which subreddit a given post came from?

In this project I have collected data uding Reddit's API and got the data for two subreddits "Running", and "Lose it".
The goal for this project is to using NLP and Machine Leaning models, build a binary predictor to determine which subreddit a given post is coming from.
>
> *Data Collection:* Reddit API
>
> *Data Cleaning and EDA* 

I first built API Function to pull posts as many as I need for the data collection. I chosen different subreddits , but since I needed more data entries, I used the subreddits with much more post enteries. Each subreddit has about 10000 enteries and after cleaning up and dropping the duplicates, I ended up having 19611 rows for the merged dataset. I located the text from each posts and created a new column to identify each post as whether coming from "Running" or "Lose it" subreddits.
>
> *Preprocessing* 
>
> 1- Removed non-letters, 
>
> 2- Converted to lower case and splitted the words,
>
> 3- Used stop words,
>
> 4- Used Stemming and Tokenizing.

Before starting the preprocessing NLP, I tried to plot the most common words in each data set and the plots represented a few nonsense vocabularies such as "19F", "made", "SW1", and I decided to implement stemming, tokanizing and using stopwords to get the related words for each subreddits.

> *Modeling*
>
> 1- Instantiated and fitted CountVectorizer and TF-IDF Vectorizer
>
> 2- Instantiated and fitted Pipeline and GridSearch
>
> 3- Used Logistic Regression, Naive Bayes Classifier and Random Forest Model

After the process of traning, testing and splitting, I used TFID Vectorizer and Count vectorizer tools to get the words frequencies. Then I created and compared different models such as Naive Bayes Clasifier, Logistic Regression and Random Forest Model and I got the highest score on the Count Vectorizer+ Logistic Regression Model for 99% on training dataset and %92 on testing dataset. 

### Conclusion

If you are an internet savvy person and follow different social news platform, you must have heard of Reddit ! Reddit allows its users to discuss and vote on content (such as links, text posts, and images) that other users have submitted. 
There are about 138,000 active subreddits among a total of 1.2 million subreddits. But, how is it possible to find your own community with the topics you have interest in?!

The challenge for this project is to help you identify the community which is right for you!

I know I know... You are thinking now “I like food and drinks”, “I love art and paintings” or maybe “I love Running and Losing weight” but don’t have the time to search in all these subreddits that Reddit offers and just want to find your community soon! You are already overwhelmed with life and prefer not googling to find the topics and community you like.

Well, that is why I am here! I try to help you out but how? My model here goes over all the subreddits that you have some interest in and BAM! It gives you the most key words of each subreddits and you can easily decide which community is for you! Why am I think my model is good? Another BIG BAM! Since my model has an accuracy of %99 to identify the certain posts and vocabularies from any subreddits. 
