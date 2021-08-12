# Machine-Learning-Challenge
## Exoplanet Exploration

In 2009, NASA launched the Kepler Space Observatory.  The satellite's goal is to discover hidden, habitable planets outside of our solar system.  The original mission ended in 2013, but the telescope is still active and continues to collect new data on its extended mission.

The dataset used is a CSV file containing records of all observed Kepler "objects of interest" which is approximately 10,000 exoplanet candidates.  The dataset includes candidate characteristics, observations and results.  You can find the dataset [here](https://www.kaggle.com/nasa/kepler-exoplanet-search-results).  Data column definitions can be found [here](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html).

Unecessary columns and null entries were removed from the dataset.  It was then split into testing and training sets and scaled accordingly.  Machine learning models were created to classify identified exoplanets from this dataset. Hyperparameter tuning was done with GridSearch to find the best parameters and create a tuned model.  Models examined were Logistic Regression, Support Vector Machines, and Random Forests.  

The objective of model evaluation is to estimate the accuracy of a model on unseen data.  Accuracy is a common evaulation metric to look at when tackling classifications.  It is the ratio of correctly predicted observations to the total number of observations.  The Random Forest model far outperformed with an accuracy of .89 and the poorest model was Support Vector Machine.

With all three models the training score was better than the testing score.  This is expected because the model was trained on the training dataset.  When conducting the hyperparameter tuning the Random Forest model took the longest time to execute.  

The preformance of 

1. compares each of the models’ performances and predictions
2. summarizes the findings and makes assumptions based on the data and their models.
3. discusses the predictions of the possible exoplanets with their models.



Logistic Regression - 

Set Significant Features
Training Data Score: 0.8037383177570093
Testing Data Score: 0.8032036613272311

Hyperparameter Tuning (75 fits)
{'C': 100, 'max_iter': 500, 'penalty': 'l2', 'solver': 'newton-cg'}
0.8107949046347303

Support Vector Machines -

Set Significant Features
Training Data Score: 0.6580202174327675
Testing Data Score: 0.6493135011441648

Hyperparameter Tuning (45 fits)
{'C': 10, 'gamma': 0.0001}
0.6770935969552972

Random Forest
* Set Significant Features
- Training Data Score: 1.0
- Testing Data Score: 0.8924485125858124

* Hyperparameter Tuning (20 fits)
- {'max_features': 'sqrt', 'min_samples_split': 2, 'n_estimators': 400}
- 0.8909000938734819

---
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.