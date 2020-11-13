# Performing Sentiment Analysis on Generating a Wordcloud Trump Campaign Speeches

Kaggle provides a number of great datasets. I found someone that posted 35 of Trump's campaign speeches in 2019 and 2020. Given how close the election was and how divisive Trump is considered by many, I thought it would be interesting to perform NLP and sentiment analysis on the speeches. 

Source: https://www.kaggle.com/christianlillelund/donald-trumps-rallies

## Steps Taken to Perform the Analysis
The Kaggle dataset provided 35 text documents with each text document containing one speech that Trump gave across various cities in the U.S.

I read in the the individual speeches, converting each speech into one large, concatenated string, and stored them into a DataFrame:

![alt text](images/original_df.png)

I then converted cleaned the text by removing punctuations:

![alt text](images/clean_df.png)

# Steps Taken to Perform the Sentiment Analysis

The analyis was performed using the NLKT (Natural Language Tool Kit), a popular Python library used to analyze human language data. Within the NLTK library there is a popular model called VADER (Valence Aware Dictionary And Sentiment Reasoner), which uses a lexical approach to analyze text. Words are labeled according to their semantic orientation as either positive or negative and the VADER provides an overall assessment of how positive or negative is the sentiment.

There are some pros and cons to using the VADER model which include:

Pros:
- Easy to understand approach and quick to implement

Cons:
- Misspellings and grammatical mistakes can cause the analysis to overlook words or usage

For more information here is a great article: https://www.codeproject.com/Articles/5269447/Pros-and-Cons-of-NLTK-Sentiment-Analysis-with-VADE

Lastly, I generated sentiment scores for each speech, appended them to empty lists, and then attached the sentiment scores to new DataFrame. This DataFrame was combined with the orignal DataFrame:

![alt text](Images/combined_df.png)

## Conclusion:

The speeches were largely rated as "neutral" 
