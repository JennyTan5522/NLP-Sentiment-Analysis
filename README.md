About:
- Sentiment analysis is one of the techniques that aims to classify textual data into positive, neutral, and negative labels. The study developed a predictive model that can be used in Natural Language Processing (NLP) to perform sentiment analysis predictions in various fields.  
- This project works on sentiment analysis on Covid **Twitter** tweets and **iPhone** Twitter tweets by training on **General Tweets* from Twitter.
- Based on product review sentiment analysis, companies are able to understand the sentiment of the customers towards their products or services.
- Covid review can be used to determine a human's emotional state and stability during the pandemic so that the government can determine the mental health of the people and take precautions if needed.
- Purpose of using two datasets: To review how the models work in different data patterns and identify the most suitable sentiment classifier that can correctly classify the sentiment of a sentence in various fields.

------------------------------------------------------------------------------------------------------------------------------

Dataset Description:
- Training dataset based on General Tweets that consists of both Twitter and iPhone tweets. The dataset consists of 27480 rows of training tweets with sentiment labels positive, neutral and negative. Neutral labelled consists of 11117 rows, positive labelled consists of 8582 rows, negative labelled consists of 7781 rows [https://www.kaggle.com/datasets/abhi8923shriv/sentiment-analysis-dataset?select=train.csv]. Neutral labelled consists of 11117 rows, positive labelled consists of 8582 rows, negative labelled consists of 7781 rows.
  
- Testing dataset (Using web scrapping technique from Twitter [https://apify.com/quacker/twitter-scraper]):
  1. Covid Tweets: The dataset consists of 290 rows of testing tweets with sentiment labels positive, neutral and negative. Neutral labelled consists of 102 rows, positive labelled consists of 88 rows, negative 
labelled consists of 100 rows. Neutral labelled consists of 102 rows, positive labelled consists of 88 rows, negative
labelled consists of 100 rows.
  2. iPhone Tweets: The dataset consists of 310 rows of testing tweets with sentiment labels positive, neutral and negative. Neutral labelled consists of 77 rows, positive labelled consists of 107 rows, negative 
labelled consists of 126 rows. Neutral labelled consists of 77 rows, positive labelled consists of 107 rows, negative
labelled consists of 126 rows

![image](https://github.com/user-attachments/assets/19e7566a-b2f4-4e54-ab6e-70067d9f9ece)

------------------------------------------------------------------------------------------------------------------------------

Proposed Frameworks:
1. Machine Learning
   - Individual Models: Using 8 classifiers: SVM, LR, Multinomial Naive Bayes (MNB), Decision Tree (DT), KNN, Random Forest (RF), Gradient Boosting Classifiers, Extremely Randomized Trees
   - Ensemble Models: Voting and Stacking perform on (SVC, LR, MNB and DT with LR) and (SVC, LR, MNB and RF with LR); Bagging (DT, RF)
   
   ![image](https://github.com/user-attachments/assets/26c1392e-21fe-49a7-811c-69563b80afed)

3. Deep Learning
   - Individual Models: CNN, BiLSTM, RNN, LSTM, GRU
   - Ensemble Models: Stacked RNN-LSTM-GRU with SVM, Stacked RNN-LSTM-GRU with LR
   - Hybrid: CNN-BiLSTM
   
   ![image](https://github.com/user-attachments/assets/a18d0df2-93c3-4483-9ce4-a80874a10244)

Results
1. Generat Tweets as Training and Testing
   ![image](https://github.com/user-attachments/assets/87971d8c-b39a-4381-8b8b-81a7fb644501)
   ![image](https://github.com/user-attachments/assets/4584127b-65ac-4f55-9483-79f77951f34b)

3. Covid Dataset Using Individual and Ensemble Model
   ![image](https://github.com/user-attachments/assets/d9b79173-df14-486a-b626-5ea8418e333d)
   ![image](https://github.com/user-attachments/assets/6a178a5c-76f8-473f-a670-afdb463e4fed)

   Deep Learning Model
   ![image](https://github.com/user-attachments/assets/ffc33b3c-b813-40a9-b9ce-3fc285bee63f)
   ![image](https://github.com/user-attachments/assets/bfac2261-62d6-4dae-b6b8-582d19151c7e)

   Deep Learning Hybrid Model
   ![image](https://github.com/user-attachments/assets/ed19c6ed-6c27-4ed2-9a82-ca3810aee4fe)
   ![image](https://github.com/user-attachments/assets/1ecef24c-e10c-440b-9d39-fd54b0cdb2b3)


Conclusion: Stacked RNN-LSTM-GRU with SVM has the best performance compared to the other two models on average
