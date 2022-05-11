# Sentiment Analysis on Amazon Reviews of Cellphones and Accessories
# Introduction
This is an NLP experiment with the goal of understanding the emotion behind Amazon's cell phone reviews.

Dataset Link:
http://deepyeti.ucsd.edu/jianmo/amazon/categoryFilesSmall/Cell_Phones_and_Accessories_5.json.gz

# YouTube Link
https://youtu.be/k1d4t8knzLI

# What is NLP ?
Natural language processing (NLP) is a technique for translating computer and human languages. It is a technique for enabling a computer to sensibly comprehend a line of text without using any form of hint or computation. In other words, NLP automates computer-to-human translation. source

# Overview
This is a sentiment analysis project. Sentiment analysis, as the name implies, is used to determine attitudes within many cell phone ratings on Amazon. It is also utilized to discern sentiment when the feelings are not clearly conveyed. Companies are employing sentiment analysis, a natural language processing (NLP) technology, to determine their consumers' opinions and sentiments online. It will assist businesses in understanding what their consumers think about their products and services. With the use of sentiment analysis, businesses may assess their entire reputation based on consumer posts.
In this approach, we may argue that sentiment analysis goes beyond establishing mere polarity to assist us better comprehend what is underlying the expressed viewpoint..

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

