# DT-TM
In this project I has the opportunity to construct a Decision Tree to determine the best predictors for housing prices in a locality and the opportunity to conduct Text Mining.

The goals of this project were:
Split data into training and testing sets for use with a Decision Tree.
Create a Decision Tree, fit it with the data, make predictions with the tree and plot the decision tree model.
Conduct Text Mining operations on a Dataset.
Conduct sentiment analysis on a dataset and construct a word cloud with said data.
Provide a summary of the findings and make recommendations to Stakeholders based on the findings.

For this exercise I used the libraries:
rpart, rpart.plot, caret, tidyverse, tidymodels, tm, SnowballC, wordcloud, RColorBrewer, syuzhet 
I used the datasets:
"Boston Housing Data" from the UCI website and the "Yelp Labelled Dataset" from Kaggle.

For the Decision Tree I set out to find what the main predictor for the housing prices was. I started out by binning the Mediant House Values into three categories 0-15k, 15-30k and 30-50k. After, I created the test and training sets for the model, I fitted the model with the intent of testing the Median House Value against every other variable in the data. Then I tested the accuracy of the model through a confusion matrix. Lastly I extracted the predictions. 
From the results I could gather that most homes were valued in the 15-30k dollar range, and that number of rooms was the strongest predictor or home value.

For the Text Mining operations, I set out to conduct sentiment analysis on the dataset consisting of Yelp reviews. To start I created a Corpus object and performed many data cleaning steps to remove: whitespace, unwanted characters, numbers, stop words and punctuation. Then I stemmed the text and built a term-document matrix that I would then sort by descending frequency.
With preparations done I got the sentiments with a function, placed them in a data frame that I would then transform and plot.
Then I used two functions to both find correlations for terms and generate a word cloud.
From my observations on the associations, sentiments and the word cloud, I wrote out a few suggestions.

I did not run into major issues when creating the decision tree as the data was already clean and in order. I did not run into expected issues with the Yelp dataset and could carry out the needed cleaning, though due to limitations with stemming and the stop words I wanted to remove I had to remake a few times to get a cleaner result that more clearly conveyed sentiment.
