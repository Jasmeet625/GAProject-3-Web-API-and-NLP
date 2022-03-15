Problem Statement:

To create a text classifier to determine whether a reddit post would be classified into the Subreddit group "Blogging" or "Writing". This classifying objective would allow a blogger or a writer to post his/her posts in the right category so as to receive the most amount of views.

Can we use Natural Language Processing to build this classifier to determine the most amount of views for posts by bloggers and writers?


Dataset:

Data of 2 subreddit: Blogging and Writing were scrapped using Pushift API.

After getting our url in json, request is sent to Reddit using a non-deafault value for the key 'User-agent' to prevent Reddit from shutting our script from accessing its API.

A status code of 510 writing posts and 686 blogging posts were received.

The scraped data is saved in a Pandas Dataframe and exort as csv file.


Executive Summary:

EDA:

From our analysis, the Blogging subreddit group have a huge emphasis on their blog optimisation (common phrases that appear: SEO, traffic flow, keyword search etc.) and less on technical writing elements. However, the Writing subreddit group appears to be the opposite. Posts appear to be focused on writing techniques, with many users posting questions and seeking help for their stories (common phrases that appear: 'writing advice, don know, dont want, help writing, start writing').

In terms of overall tonality of the words/phrases that commonly appear in both subreddit groups, we can conclude Blogging subreddit group appears to be more formal and professional, whilst Writing subreddit group appears to be more casual and community-based. This could be due to the fact that Bloggers are more marketing/promotion oriented, whilst writers are more focues on the art of writing.

Modelling (Classification Model):

As seen from the models, both models have performed similarly in predicting whether posts fall under the Writing or Blogging subreddit groups, with an accuracy of approximately 93%. From our Logistic regression, we were able to understand how our Logistic regression classify our posts based on the words appeared.

Interestingly, words that are of greater importance in classfiying posts into the Blogging subreddit are: Posts, Content, Website, Niche, Article, Google, SEO, link etc (web-analytics oriented) Whereas words that are of greater importance in classfiying posts into the Writing subreddit are: story, character book, novel, read, writer, plot, feel, chapter etc. (traditional writing-oriented)


Conclusion:

In conclusion, we are rather indifferent about both the Naive Bayes model or the Logistic Regression model in classifying our subreddit posts.

Both models have achieved a similar accuracy scores, despite having differences in other metrics that we have identified. ROC curve also shown that Naive-Bayes and Logistic Regression is largely similar in performance.
