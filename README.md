# UROP-ABCD

During this IAP, I have self-learned a lot of material and achieved a decent understanding of decision trees, some understanding of RandomForest and XGboost, and a variety of other concepts like pruning, parameter tuning, and interpreting different evaluation metrics (precision, recall, f1, accuracy, roc_auc).

In the following files, I have attempted to train a Decision Tree model using the ABCD data on suicide attempts. 

## Load Data + Data Separation
I loaded in the data, separated into training and validation set (80/20) using the stratify method in attempt to mediate data imbalance.

## Preliminary Model
I created a decision tree classifier with class_weight='balanced' to control data imbalance. I printed some metrics to establish a baseline of what the model would do without any parameter changes.

## Cost Complexity Pruning + AUC ROC
I extracted all possible values of alpha available for each tree, then build a pruned tree for each value. I plotted Accuracy vs alpha to visualize the general trend. Then, I utilized GridSearch and scored based on recall, f1, and roc_auc to find the most optimal alpha value. Finally, I built a pruned tree using the best alpha and evaluated its metrics.

## Questionaire + fMRI
Similar steps were taken to achieve the same results for psychosocial responses and fMRI data for both rsfMRI and sstfMRI.

![image](https://github.com/user-attachments/assets/81f4d5c4-6a6f-436b-a35c-0e10df7f30ce)

![image](https://github.com/user-attachments/assets/6eb733e7-1f0b-4955-bf75-d8120e8615e9)



