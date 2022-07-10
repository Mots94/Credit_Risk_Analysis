# Credit_Risk_Analysis

## Overview
Determining the risk of granting a loan can be a challenging task for many reasons.  One of those reasons is that there is much more data related to good loans as opposed to bad loans.  If a machine learning model needs to accurately predict a risky loan decision, not having as much data on bad loan decisions makes it difficult to teach the model what features are most often predict a bad loan.  However, there are algorithms that can be used to resample target variable data, which may aid in creating a model that more accurately predicts risky loans.  Six algorithms which either resampled data reduced data bias were evaluated to determine if any of them could predict risky loan outcomes.

## Results
* The first model utilized a simple naive random oversampling approach. This model had a balanced accuracy score of 66%.  Of all the high risk loans in the resampled dataset, 71% were actually predicted to be high risk.  This seems pretty impressive, considering a model is needed to identify high risk loans so that loans are not given out in those situations.  However, the precision of predicting high risk loans is quite low at 1%.  Though the recall of this model is high, loans are likely to be predicted as high risk when in actuality they are not.  This could lead to denying more loans than is necessary and losing out on business.

![n_oversample](https://github.com/Mots94/Credit_Risk_Analysis/blob/main/Images/naive_resample.png)

---
* A second model used the SMOTE approach, which synthesizes new data from existing data.  These data points are sampled based on their proximity to existing data points, rather than being randomly chosen.  Though this is the case, the predicitve capability for this model was similar to the previous model.  The balanced accuracy score was again 66%, meaning that 66% of all predictions were predicted accuractly.  The precision of high risk loan predictions is again low at 1%.

![SMOTE](https://github.com/Mots94/Credit_Risk_Analysis/blob/main/Images/SMOTE_oversample.png)

---
* The third model used in this analysis was an undersampling model.  In this case, the balanced accuracy score decreased to 52%.  The precision scores for high and low risk predictions did not change compared to previous models.  

![under](https://github.com/Mots94/Credit_Risk_Analysis/blob/main/Images/undersample.png)

---
* A combination of under and oversampling was completed using the SMOTEENN resampling method.  In this case, the recall of the model was quite high at 72%, and the balanced accuracy score was 64%.  Though there have been higher recall scores for high risk loans, precision for high risk loan predictions has stayed low across all of these models at 1%.  It may be better to have a balance of precision and accuracy to determine credit risk determination.  Two more alogrithms were used to in this case to see if that is possible.

![SMOTEENN](https://github.com/Mots94/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)

---
* In the final two sampling algorithms, some greater consideration was given to the large imbalance seen in this dataset related to the target variable.  Rather than simple under or oversampling the target variable groups.  The first model, Random Forest for Imbalanced Classification, used bootstrap sampling of features at random, and within these samples not all features are sampled.  These samples are what is used to fit a decision tree that ultimately yields the predictive values.  In the this first model, precision for high risk loan predictions increased to 23%.  However, there was a balanced accuracy score of 1.00.  The second model used, Easy Ensemble for Imbalanced Classification, also utilizes bootstrap samples.  However, this model randomly undersamples data rather than oversampling.  The results of this algorithm were simlar to the previous.  Precision for high risk loans was 0.11 and the balanced accuracy score was 0.99.  

![](https://github.com/Mots94/Credit_Risk_Analysis/blob/main/Images/balanced_rf.png)

![](https://github.com/Mots94/Credit_Risk_Analysis/blob/main/Images/easy_ensemble.png)
