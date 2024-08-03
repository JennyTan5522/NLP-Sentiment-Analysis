About:
- Sentiment analysis is one of the techniques that aims to classify textual data into positive, neutral, and negative labels. The study developed a predictive model that can be used to perform sentiment analysis predictions in various fields.  
- This project works on sentiment analysis on Covid **Twitter** tweets and **iPhone** Twitter tweets by training on **General Tweets** from Twitter.
- Based on product review sentiment analysis, companies are able to understand the sentiment of the customers towards their products or services.
- Covid review can be used to determine a human's emotional state and stability during the pandemic so that the government can determine the mental health of the people and take precautions if needed.
 
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

------------------------------------------------------------------------------------------------------------------------------

Parameters:
1. The parameter values of the SVC Classifier are tuned as : C=0.1, kernel= ‘linear’, random_state = 1
2. The parameter values of the Logistic Regression Classifier are tuned as : multi_class= ‘multinomial’, random_state = 1, solver= ‘saga’
3. The parameter values of the Multinomial Naive Bayes Classifier are tuned as : alpha =20
4. The parameter values of the KNN Classifier are tuned as : n_neighbors=13
5. The parameter values of the Decision Tree Classifier are tuned as: random_state =1, max_leaf_nodes=65, max_depth=100
6. The parameter values of the Random Forest Classifier are tuned as: random_state = 1, max_leaf_nodes=65, max_depth=100
7. The parameter values of the Gradient Boosting Classifier are tuned as: random_state = 1, max_depth=3 , max_leaf_nodes=40
8. The parameter values of the Extremely Randomized Trees Classifier are tuned as: random_state = 1, max_depth=80, max_leaf_nodes=100.

------------------------------------------------------------------------------------------------------------------------------

Results
1. Generat Tweets as Training and Testing
   ![image](https://github.com/user-attachments/assets/87971d8c-b39a-4381-8b8b-81a7fb644501)
   ![image](https://github.com/user-attachments/assets/4584127b-65ac-4f55-9483-79f77951f34b)

2. Covid Individual Model Testing Result
   -  Extremely Randomized Trees is selected as the best individual sentiment classifier (Highest accuracy with the least training time)
   -  Ensemble Voting model with SVC, Logistic Regression, Multinomial Naive Bayes and Decision Tree as the base learners and Logistic Regression as the meta-classifier has high training accuracy with an accuracy of 71.94%.
   -  Although Stacking has a higher training accuracy, but from the overall testing accuracy performance and training time, it does not perform well. The results state that Voting has a higher testing accuracy with 62.00% as compared to Stacking with the accuracy of 60.00%, it increase overall performance by 2%.

   ![image](https://github.com/user-attachments/assets/987bd00e-9d45-4921-bd69-c70a3abcf1fe)

   ![image](https://github.com/user-attachments/assets/3fc8e3ef-8ced-4c98-a71b-266ba4d8c16c)

   ![image](https://github.com/user-attachments/assets/e4709bfd-9823-4dbd-b051-739a24347583)

4. Iphone Individual Model Testing Result
   - The testing accuracy for all the models have a huge difference with the training accuracy. Mostly due to the unstructured and contains lots of noisy data as well as weak sentiment constraints, hence this makes machine difficult to analze and gain valuable pattern from the data, e.g. emoji ambiguity, uncertainty of word meaning, negation words. 

    ![image](https://github.com/user-attachments/assets/bf11b8de-9cb5-4965-be1f-908877f184a8)

   ![image](https://github.com/user-attachments/assets/80a9bc3d-f1d6-4858-baf3-93cf8e0b3f36)

6. Covid Dataset Using Individual and Ensemble Model
   - Voting model and Bagging model have the same testing accuracy but a slight difference in terms of the training accuracy and training time. Since the training time of Bagging model is shorter than the Voting model, the training time performance of Bagging model is better than Voting model.

   ![image](https://github.com/user-attachments/assets/d9b79173-df14-486a-b626-5ea8418e333d)
   ![image](https://github.com/user-attachments/assets/6a178a5c-76f8-473f-a670-afdb463e4fed)

   Deep Learning Model
   ![image](https://github.com/user-attachments/assets/ffc33b3c-b813-40a9-b9ce-3fc285bee63f)
   ![image](https://github.com/user-attachments/assets/bfac2261-62d6-4dae-b6b8-582d19151c7e)

   Deep Learning Hybrid Model
   ![image](https://github.com/user-attachments/assets/ed19c6ed-6c27-4ed2-9a82-ca3810aee4fe)
   ![image](https://github.com/user-attachments/assets/1ecef24c-e10c-440b-9d39-fd54b0cdb2b3)


Conclusion: Stacked RNN-LSTM-GRU with SVM has the best performance compared to the other two models on average
