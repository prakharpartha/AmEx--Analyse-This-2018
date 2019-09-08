# AmEx--Analyse-This-2018

PROBLEM DESCRIPTION: Predict credit worthiness(will default or not) of an individual using the past credit history of the individuals.
Also create a order in which the application should be processed to min the chances of prediction going wrong.

LOOPHOLE: The bank is heavily penalized if he makes a wrong prediction and the individual defaults. 

MAIN CHALLENGES TACKLED: 
> Presence of large no. of features (47), with all features containing missing values.
> Optimizing the threshold by deciding a trade-off between precision and recall.

FINAL RANK: 64 out of 1028 teams

MODELING PHASE :
I applied PCA after removing the features with many missing values(>40%) and showing a high correlation (VIF>6). I used a no. of classification algorithms to train the final data, starting with Logistic regression, Random Forest, SVM and using ensebling by XGBoost and LightGBM classifier. LightGB Classifier gave best results, both by Cross Validation and Train Test spliting. Final order for processing the test set was made based on the confidence of prediction(by considering the difference between the predicted probability and the threshold probability).

Language : Python
IDE : Spyder
