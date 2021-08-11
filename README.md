# Machine-Learning-Challenge
## Exoplanet Exploration

In 2009, NASA launched the Kepler Space Observatory.  The satellite's goal is to discover hidden, habitable planets outside of our solar system.  The original mission ended in 2013, but the telescope is still active and continues to collect new data on its extended mission.

The dataset used is a CSV file containing records of all observed Kepler "objects of interest" which is approximately 10,000 exoplanet candidates.  The dataset includes candidate characteristics, observations and results.  You can find the dataset [here](https://www.kaggle.com/nasa/kepler-exoplanet-search-results).  Data column definitions can be found [here](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html).

Unecessary columns and null entries were removed from the dataset.  It was then split into testing and training sets and scaled accordingly.  Machine learning models were created to classify identified exoplanets from this dataset.  Models examined were Logistic Regression, Support Vector Machines, and Random Forests.  Hyperparameter tuning was done with GridSearch to find the best parameters and create a tuned model.

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

Random Forest -

Set Significant Features
Training Data Score: 1.0
Testing Data Score: 0.8924485125858124
Hyperparameter Tuning (20 fits)
Training Data Score: 1.0
Testing Data Score: 0.8930205949656751


---
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.