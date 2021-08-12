# Machine-Learning-Challenge
## Exoplanet Exploration

In 2009, NASA launched the Kepler Space Observatory.  The satellite's goal is to discover hidden, habitable planets outside of our solar system.  The original mission ended in 2013, but the telescope is still active and continues to collect new data on its extended mission.

The dataset used is a CSV file containing records of all observed Kepler "objects of interest" which is approximately 10,000 exoplanet candidates.  The dataset includes candidate characteristics, observations and results.  You can find the dataset [here](https://www.kaggle.com/nasa/kepler-exoplanet-search-results).  Data column definitions can be found [here](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html).

Unecessary columns and null entries were removed from the dataset.  It was then split into testing and training sets and scaled accordingly.  Machine learning models were created to classify identified exoplanets from this dataset. Hyperparameter tuning was done with GridSearch to find the best parameters and create a tuned model.  Models examined were Logistic Regression, Support Vector Machines, and Random Forests.  

The objective of model evaluation is to estimate the accuracy of a model on unseen data.  Accuracy is a common evaulation metric to look at when tackling classifications.  It is the ratio of correctly predicted observations to the total number of observations.  Another metric is precision which is a ratio of correctly predicted positive observations to the total of those observations.  Recall is the ratio of correctly predicted positive observations to the total predicted positive observations.  The final metric is F1 which is an average of the precision and recall.  Where 1 is it's best value and it's worst is 0.  The Random Forest model beat or met all the metrics of the other two models.

With all three models the training score was better than the testing score.  This is expected because the model was trained on the training dataset.  When conducting the hyperparameter tuning the Random Forest model took the longest time to execute.  Therefore, less fits were conducted.

The assumption that more variables make a better model and a more complex model makes a better prediction are not always true.  If you can achieve accuracy with a simple model then use that model.  More unnecessary variables can create noise.  Also, overfitting the model can be a mistake.  The finer you tune the model to the training dataset, the higher the possibility of getting an unwanted result from your testing dataset becomes.

Four significant variables were used in all three models are koi_period, koi_teq, koi_model_snr, koi_fpflag_nt.  These factors probably most contribute to the outcomes.  

1. Random Forest Model
* Training Data Score: 1.0
* Testing Data Score: 0.8924
* Grid Best Score: 0.8909

2. Logical Regression Model
* Training Data Score: 0.8037
* Testing Data Score: 0.8032
* Grid Best Score: 0.8108

3. Support Vector Machine Model
* Training Data Score: 0.6580
* Testing Data Score: 0.6493
* Grid Best Score: 0.6771

---
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.