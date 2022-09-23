# Credit_Risk_Analysis
## Overview of the analysis:
---The analysis done is on predicting credit risk. The known factors are there is a huge data imbalance between good credit reports and risky credit reports. 
After using several sampling methods we will determine if any particular method yields a considerably improved result. 

## Results: 
---Below we see the first sampling method showing poorly on the precision score and 63 percent on recall. The balance is also low at 71 percent. Indicates the sensitivity is not that great and the data captured is not going to accuraately predicte high risk loans 
* Balanced Score: 0.6463970560994359
![Random_Oversampling](https://github.com/jobloom79/Credit_Risk_Analysis/blob/main/Resource/random_oversample.PNG)
#### SMOTE Oversampling
---Using SMOTE we see a decrease in the recall values on high risk loans, although the balanced score increases
* Balanced Score: 0.6586230769943224
![SMOTE_Oversampling](https://github.com/jobloom79/Credit_Risk_Analysis/blob/main/Resource/smote_oversample.PNG)
#### Undersampling
---Undersampling degradates the balanced score significantly and does not yield the highest recall percentage. This sampling yields the least favorable results
* Balanced Score: 0.5442369453268994
![Random_Undersampling](https://github.com/jobloom79/Credit_Risk_Analysis/blob/main/Resource/undersampling.PNG)
#### Combination Sampling
---Combination sampling altnough better output than undersampling also has not improved over some of the othe sampling
* Balanced Score: 0.6281241606387018
![Combination_Sampling](https://github.com/jobloom79/Credit_Risk_Analysis/blob/main/Resource/combo_oversample_undersample.PNG)
#### Random Forest Classifier
---Using the new method of balanced forest classifer the is an overall increase in all the values, but also yields higher low risk recall values that is not necessarily the number we need to increase
* Balanced Score: 0.7885466545953005
![Forest_Classifier](https://github.com/jobloom79/Credit_Risk_Analysis/blob/main/Resource/balanced_forest.PNG)
#### Adaboot Classifier
---Adaboost provide the best value giving recall value above 90% as well as the balanced score indicating a balancing of the dataset and yielding the most output on the target info
* Balanced Score: 0.9316600714093861
![Adaboost_Classifier](https://github.com/jobloom79/Credit_Risk_Analysis/blob/main/Resource/adaboost.PNG)

# Summary: 
---In summary we see that using the Adaboost Classifier allows for a well balanced dataset and makes it more favorable to increasing sensitivity in order to yield the most results of high risk loans while improving the percentage of the high risk loans captured in the data to be accurately predicted as a True positive result. Unfortunately the percentage is still low despite being the highest in this dataset. One recommendation would be to possibly iterate through the adaboost classifer providing a combo oversampling and adaboost method to raise the results.