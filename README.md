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

![image](https://github.com/user-attachments/assets/3de24e58-a213-41fe-850c-51b15fb5c7d8)
![image](https://github.com/user-attachments/assets/a379745d-9455-4a74-9c43-73e8b6bb37ba)

![image](https://github.com/user-attachments/assets/66eb7099-6358-4e4e-89b1-bb8c08c7a058)
![image](https://github.com/user-attachments/assets/1e19a664-4b1d-47ac-8811-ecd706fb5695)

