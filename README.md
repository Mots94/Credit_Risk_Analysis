# Credit_Risk_Analysis

## Overview
Determining the risk of granting a loan can be a challenging task for many reasons.  One of those reasons is that there is much more data related to good loans as opposed to bad loans.  If a machine learning model needs to accurately predict a risky loan decision, not having as much data on bad loan decisions makes it difficult to teach the model what features are most often predict a bad loan.  However, there are algorithms that can be used to resample target variable data, which may aid in creating a model that more accurately predicts risky loans.  Six algorithms which either resampled data reduced data bias were evaluated to determine if any of them could predict risky loan outcomes.

## Results
* The first model utilized a simple naive random oversampling approach. This model had a balanced accuracy score of 66%.  Of all the high risk loans in the resampled dataset, 71% were actually predicted to be high risk.  This seems pretty impressive, considering a model is needed to identify high risk loans so that loans are not given out in those situations.  However, the precision of predicting high risk loans is quite low at 1%.  Though the recall of this model is high, loans are likely to be predicted as high risk when in actuality they are not.  This could lead to denying more loans than is necessary and losing out on business.

![n_oversample]()
