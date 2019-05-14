# Project Description
In the following paper, we discuss the data, featuring engineering, and machine learning techniques we used to answer the following two questions: 

-  Is a user likely to make a purchase in the next 7 days? 
-  Is a user likely to make a purchase in the next 14 days? 

For this problem, we used a dataset provided by Leanplum containing information about users’ interactions with a single mobile app during the course of three months.

## Methods

Our first task was to create labels from the Events table that indicated whether a user made a purchase within the last week/two weeks of our training data. Once we had our labels, we began our featuring engineering. The final models used a little over 70 numerical features calculated over specific weeks leading up to the testing period. From there we experimented with different Machine Learning models, keeping the seven-day and fourteen-day problems separate. We assessed the performance (AUC score) of Random Forest, LightGBM, Logistic Regression, and XGBoost models using K-fold Cross Validation. In the end, we blended our two best models, XGBoost and RF with equal weights for 7-day prediction. Similarly, for fourteen-day prediction we blended equally XGBoost, LightGBM, and RF. Our final models gave us an AUC score of 0.98672 on the test values.

## Team Responsibilities

- Zack: Featuring engineering, modeling, Machine Learning section of the paper
- Xinke: EDA and Experimental Results sections of Paper
- Nicole: Created labels for training, Abstract and Feature Engineering/Appendix
sections of the paper
