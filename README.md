# Problem Statement
Major League Baseball has been declining in popularity from falling attendance, bad World Series ratings, and lack of nationally recognized stars. Now with a Covid-19 pandemic shutting down in game attendance, MLB is facing an existential threat to future revenue.<br><br>The commissioners offices has tasked me to try to grow the fan base with targeted ads with social media. We want to target the new potential fans using a Natural Language Processing model to classify teams they are interested in. We want to have the most accurate model possible with the goal to launch a model by next season. 

## Data
The data has been pulled from two subreddits before we pull more resources for data collection. The data has about 26k post from the Dodgers subreddit while there is 6k Yankee posts. Missing selftext from the body of the post are because of media like pictures or videos. The distributions of all lengths and word counts are skewed to the right. The titles lengths between one and 300 characters. A majority of the length of the titles are between 25 and 100. The word count for the titles are between one and 60 words. The length of selftext are between have 0 and 1000 with a word count between 0 to 1000. There was 44 just emoji post that have been removed from the data set. They would have not added any information for the model to us for classifying a Dodger or Yankee post. However, if someone only uses emojis in there post the model would not be able to incorporate them in the current model. The data has a lot of one word post that will not help the models accuracy for predicting the two subreddits. There is 275 that I will drop from the data set. I will don't want to drop any thing above this because of player names could be they only words in the post.

## Modeling

The Baseline model accuracy is about 77.97%. The most accurate model developed was a Random forest classifier with an accuracy of 85.89%. The misclassification rate of the model is 15.31%. The true positive rate of the model is 39.26%. The true negative rate of the model is 99.56%. The precision if the model is 96.17%

## Conclusion 

- The model can predict at 84% accuracy what post are from Dodger fans or Yankee fans
    - True positive rate is low at 39%
- Misclassified a lot Yankee fans as dodger fans
    - True negative rate is 99.56%
- Misclassified some Dodger fans as Yankee fans

## Next Steps

1. Expanded current model to all 25 teams
    - Not as accurate as but gets the next step to targeting users
2. Try Term Frequency-Inverse Document Frequency (TF-IDF) Vectorizer
    - TF-IDF is a score that tells us which words are important to one document, relative to all other documents.
    - words that occur often in one document but don't occur in many documents contain more predictive power.

## References 
How Popular Is Baseball, Really?,The New York Times, accessed 27 July 2020, <ttps://www.nytimes.com/interactive/2019/10/22/sports/baseball/baseball-popularity-world-series.html>