About:
- Sentiment analysis is one of the techniques that aims to classify textual data into positive, neutral, and negative labels. The study developed a predictive model that can be used in Natural Language Processing (NLP) to perform sentiment analysis predictions in various fields.  
- This project works on sentiment analysis on Covid **Twitter** tweets and **iPhone** Twitter tweets. 

Purpose: 
- Product review sentiment analysis, companies are able to understand the sentiment of the customers towards their products or services. Examine customer overall satisfication towards products and make improvements.
- Covid review can be used to determine a human's emotional state and stability during the pandemic so that the government can determine the mental health of the people and take precautions if needed. 

Dataset Description:
- Training dataset based on General Tweets that consists of both Twitter and iPhone tweets. The dataset consists of 27480 rows of training tweets with sentiment labels positive, neutral and negative. Neutral labelled consists of 11117 rows, positive labelled consists of 8582 rows, negative labelled consists of 7781 rows [https://www.kaggle.com/datasets/abhi8923shriv/sentiment-analysis-dataset?select=train.csv].
- Testing dataset (Using web scrapping technique from Twitter [https://apify.com/quacker/twitter-scraper]):
  1. Covid Tweets: The dataset consists of 290 rows of testing tweets with sentiment labels positive, neutral and negative. Neutral labelled consists of 102 rows, positive labelled consists of 88 rows, negative 
labelled consists of 100 rows.
  2. iPhone Tweets: The dataset consists of 310 rows of testing tweets with sentiment labels positive, neutral and negative. Neutral labelled consists of 77 rows, positive labelled consists of 107 rows, negative 
labelled consists of 126 rows.
![image](https://github.com/user-attachments/assets/cfae150f-e900-47ec-aeb7-f1b208235674)

Proposed Frameworks:
1. Machine Learning
   ![image](https://github.com/user-attachments/assets/26c1392e-21fe-49a7-811c-69563b80afed)

3. Deep Learning
   ![image](https://github.com/user-attachments/assets/a18d0df2-93c3-4483-9ce4-a80874a10244)


Eight classifiers were employed as base learners to evaluate sentiment analysis classification, namely Support Vector Classification (SVC), Logistic Regression, Multinomial Naive Bayes, K-Nearest Neighbor (KNN), Decision Tree, Random Forest, Gradient Boosting Classifiers, and Extremely Randomized Trees. Subsequently, ensemble classifiers such as Voting, Bagging, and Stacking were conducted in this experiment. Lastly, deep learning models were also carried out using CNN, RNN, LSTM, Bi-LSTM, and GRU. The hybrid ensemble and the deep learning model were also experimented with.

The deep learning model with the best performance is the Stacked RNN-LSTM-GRU with SVM, while the regular machine learning model that performed the best based on the COVID-19 Tweets test data is the Ensemble Bagging model of Random Forest.
