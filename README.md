# Data602_Final_Project
# Introduction
This is a NLP project with a objective to understand the sentiment behind the cell phone review on amazon.

# What is NLP ?
Natural language processing (NLP) is a method to translate between computer and human languages. It is a method of getting a computer to understandably read a line of text without the computer being fed some sort of clue or calculation. In other words, NLP automates the translation process between computers and humans. source

# Overview
This project is sentiment analysis project. As the name suggests, sentiment analysis is used to identify the sentiments among several cell phone 
reviews on amazon. It is also used to identify the sentiment where the emotions are not expressed explicitly. Companies are using sentiment analysis, 
an application of natural language processing (NLP) to identify the opinion and sentiment of their customers online. 
It will help companies to understand what their customers think about the products and services.
Companies can judge their overall reputation from customer posts with the help of sentiment analysis. 
In this way, we can say that beyond determining simple polarity, sentiment analysis understands sentiments in context to help us better understand 
what is behind the expressed opinion.

I have performed Sentiment Analysis on an amazon reviews dataset that is available to
download here. There are 1128437 rows and 12 columns in the dataset. Below is the table
which provides some information about the columns in the dataset.
# Column Non-Null Count Dtype
--- ------ -------------- -----
![image](https://user-images.githubusercontent.com/89949881/167934168-ae9b0f06-c9fc-4fda-a670-989dfe760f68.png)


 
# Data Preprocessing:

1. Created a new column called “Sentiment” using the overall column.
a. 0 - negative (overall < 3)
b. 1 - neutral (overall = 3)
c. 2 - positive (overall > 3)
2. Dropped the duplicate rows from the dataset.
3. Dropped the missing values from the dataset.
4. Dropped the columns 'vote', 'image', 'style', 'reviewerName' as they are not required for
our analysis.
5. There were 1124555 rows and 9 columns in the resulting dataset

# Exploratory Data Analysis:
Then I performed Exploratory Data Analysis on the data and got the following plots and
conclusion about the data.
Then I have done the word cloud for different groups of reviews i.e positive,
negative and neutral.

# Training and Testing:
In total I have trained 5 models. They are:
1. Classification using Random Forest Model: When I used a random forest model I got
about 79% accuracy but it predicted everything as positive. So the performance of the
random forest model is bad.
2. Classification using Logistic Regression: When I used a logistic regression I got about
90% accuracy on the test data.
3. Classification using LSTM: When I used an LSTM model with 5 epochs I got an accuracy
of 90.82% test data.
4. Regression using LSTM: When I used an LSTM model for regression with 5 epochs I got
a Mean Squared Error of 0.3597.
5. Classification using Random Forest Model: I have then joined the predicted rating from
the above Regression using LSTM model to the original dataframe, then preprocessed
the data and then used a Random Forest Classifier to predict the sentiment.
I got an accuracy of 91.21% on the test data using the above model and it is the best
accuracy I have achieved.

# Classification Report of the best model:
 ![redme02](https://user-images.githubusercontent.com/89949881/167934513-44311e94-9f3a-4617-b932-647abebfba43.png)

